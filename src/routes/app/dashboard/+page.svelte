<script>
	import {
		Dialog,
		DialogOverlay,
		DialogTitle,
		DialogDescription
	} from '@rgossiaux/svelte-headlessui';
	let sendDialogIsOpen = false;
</script>

<Dialog
	open={sendDialogIsOpen}
	on:close={() => (sendDialogIsOpen = false)}
	class="relative z-10"
	aria-labelledby="modal-title"
	role="dialog"
	aria-modal="true"
>
	<DialogOverlay class="fixed inset-0 bg-gray-500 bg-opacity-75 transition-opacity" />

	<div class="fixed inset-0 z-10 w-screen overflow-y-auto">
		<div class="flex min-h-full items-end justify-center p-4 text-center sm:items-center sm:p-0">
			<!--
            Modal panel, show/hide based on modal state.
    
            Entering: "ease-out duration-300"
              From: "opacity-0 translate-y-4 sm:translate-y-0 sm:scale-95"
              To: "opacity-100 translate-y-0 sm:scale-100"
            Leaving: "ease-in duration-200"
              From: "opacity-100 translate-y-0 sm:scale-100"
              To: "opacity-0 translate-y-4 sm:translate-y-0 sm:scale-95"
          -->
			<div
				class="relative transform overflow-hidden rounded-lg bg-white px-4 pb-4 pt-5 text-left shadow-xl transition-all sm:my-8 sm:w-full sm:max-w-lg sm:p-6"
			>
				<div>
					<!-- elusiv -->
					<div class=" bg-white mx-auto w-full flex flex-col justify-start p-5">
						<h3 class="text-base font-semibold leading-6 text-gray-900" id="modal-title">Send</h3>

						<div class="flex flex-col">
							<div>
								<div class="relative inline-flex" />
								<div
									class="border-gray-100 bg-white dark:text-neutral-400 focus:border-elusiv-purple-400 hover:border-elusiv-purple-400 flex rounded-[5px] w-full px-2 mx-auto border shadow-sm dark:shadow-none items-center py-1 transition-all duration-150 ease-in justify-between"
								>
									<div class="h-full items-center">
										<input
											type="text"
											name="amount"
											id="amount"
											class=" bg-transparent block w-full text-base border-none rounded-[5px] focus:outline-none focus:ring-0 placeholder:text-gray-400 dark:placeholder:text-neutral-600"
											placeholder="0"
											autocomplete="off"
											value="0"
										/>
									</div>
									<div class="w-5 h-5" />
									<div class="h-full items-center flex flex-col justify-center px-2">
										<button
											disabled=""
											class="bg-gray-100 text-gray-500 hover:text-gray-600 hover:bg-gray-200 dark:bg-neutral-400 dark:hover:bg-neutral-300 dark:text-neutral-800 dark:hover:text-neutral-700 inline-flex items-center px-2 py-0.5 rounded text-xs font-medium uppercase cursor-pointer transition-all ease-in duration-150 disabled:opacity-50 disabled:cursor-not-allowed"
											>max</button
										>
									</div>
									<div class="h-full items-center w-32">
										<div>
											<div class="relative">
												<div class="flex items-center">
													<img
														src="/img/tokens/usdc.svg"
														alt=""
														class="h-5 w-5 flex-shrink-0 absolute ml-2"
													/><input
														class="w-full rounded-md bg-transparent py-2 pl-10 focus:outline-none active:outline-none border-none focus:ring-0 sm:text-sm"
														role="combobox"
														type="text"
														aria-expanded="false"
														aria-autocomplete="list"
														value=""
													/>
													<button
														class="absolute inset-y-0 right-0 flex items-center rounded-r-md focus:outline-none"
														id="headlessui-combobox-button-:r6:"
														type="button"
														tabindex="-1"
														aria-haspopup="listbox"
														aria-expanded="false"
														><svg
															xmlns="http://www.w3.org/2000/svg"
															viewBox="0 0 24 24"
															fill="currentColor"
															aria-hidden="true"
															class="h-5 w-5 text-gray-600 dark:text-neutral-400"
															><path
																fill-rule="evenodd"
																d="M12.53 16.28a.75.75 0 01-1.06 0l-7.5-7.5a.75.75 0 011.06-1.06L12 14.69l6.97-6.97a.75.75 0 111.06 1.06l-7.5 7.5z"
																clip-rule="evenodd"
															/></svg
														></button
													>
												</div>
											</div>
										</div>
									</div>
								</div>
							</div>
						</div>
						<div class="relative inline-flex mt-4 mb-4">
							<div
								class=" flex justify-between rounded-[5px] w-full mx-auto px-2 bg-white border border-gray-100 shadow-sm dark:shadow-none items-center py-1 hover:border-elusiv-purple-400 transition-all duration-150 ease-in"
							>
								<div class="h-full items-center w-4/5">
									<input
										type="text"
										name="text"
										id="text"
										class="bg-transparent block w-full text-base border-none rounded-[5px] focus:outline-none focus:ring-0
								placeholder:text-gray-400 dark:placeholder:text-neutral-600 animate-none"
										placeholder="Recipient's address"
										autocomplete="off"
										data-lpignore="true"
										value=""
									/>
								</div>
								<div class=" items-center w-1/5">
									<div
										class="flex justify-end items-center pr-3 text-white cursor-pointer hover:opacity-75 transition-all duration-150 ease-in"
									>
										<svg
											xmlns="http://www.w3.org/2000/svg"
											viewBox="0 0 24 24"
											fill="currentColor"
											aria-hidden="true"
											class="w-6 h-6 text-gray-800 dark:text-neutral-100"
											><path
												fill-rule="evenodd"
												d="M3 4.875C3 3.839 3.84 3 4.875 3h4.5c1.036 0 1.875.84 1.875 1.875v4.5c0 1.036-.84 1.875-1.875 1.875h-4.5A1.875 1.875 0 013 9.375v-4.5zM4.875 4.5a.375.375 0 00-.375.375v4.5c0 .207.168.375.375.375h4.5a.375.375 0 00.375-.375v-4.5a.375.375 0 00-.375-.375h-4.5zm7.875.375c0-1.036.84-1.875 1.875-1.875h4.5C20.16 3 21 3.84 21 4.875v4.5c0 1.036-.84 1.875-1.875 1.875h-4.5a1.875 1.875 0 01-1.875-1.875v-4.5zm1.875-.375a.375.375 0 00-.375.375v4.5c0 .207.168.375.375.375h4.5a.375.375 0 00.375-.375v-4.5a.375.375 0 00-.375-.375h-4.5zM6 6.75A.75.75 0 016.75 6h.75a.75.75 0 01.75.75v.75a.75.75 0 01-.75.75h-.75A.75.75 0 016 7.5v-.75zm9.75 0A.75.75 0 0116.5 6h.75a.75.75 0 01.75.75v.75a.75.75 0 01-.75.75h-.75a.75.75 0 01-.75-.75v-.75zM3 14.625c0-1.036.84-1.875 1.875-1.875h4.5c1.036 0 1.875.84 1.875 1.875v4.5c0 1.035-.84 1.875-1.875 1.875h-4.5A1.875 1.875 0 013 19.125v-4.5zm1.875-.375a.375.375 0 00-.375.375v4.5c0 .207.168.375.375.375h4.5a.375.375 0 00.375-.375v-4.5a.375.375 0 00-.375-.375h-4.5zm7.875-.75a.75.75 0 01.75-.75h.75a.75.75 0 01.75.75v.75a.75.75 0 01-.75.75h-.75a.75.75 0 01-.75-.75v-.75zm6 0a.75.75 0 01.75-.75h.75a.75.75 0 01.75.75v.75a.75.75 0 01-.75.75h-.75a.75.75 0 01-.75-.75v-.75zM6 16.5a.75.75 0 01.75-.75h.75a.75.75 0 01.75.75v.75a.75.75 0 01-.75.75h-.75a.75.75 0 01-.75-.75v-.75zm9.75 0a.75.75 0 01.75-.75h.75a.75.75 0 01.75.75v.75a.75.75 0 01-.75.75h-.75a.75.75 0 01-.75-.75v-.75zm-3 3a.75.75 0 01.75-.75h.75a.75.75 0 01.75.75v.75a.75.75 0 01-.75.75h-.75a.75.75 0 01-.75-.75v-.75zm6 0a.75.75 0 01.75-.75h.75a.75.75 0 01.75.75v.75a.75.75 0 01-.75.75h-.75a.75.75 0 01-.75-.75v-.75z"
												clip-rule="evenodd"
											/></svg
										>
									</div>
								</div>
							</div>
						</div>
						<div class="text-xs mb-4 z-40 max-w-sm mx-auto w-full">
							<div class="font-normal">
								<button
									class="my-2 outline-offset-2 flex justify-between w-fulltext-gray-500 dark:text-neutral-400focus:outline-gray-200 duration-150 ease-in transition-all items-center h-4"
									id="headlessui-disclosure-button-:r8:"
									type="button"
									aria-expanded="false"
									><span class="">Total fees</span>
									<div class="space-x-2 flex items-center">
										<div class="items-center space-x-2 flex h-[20px]"><span>~$0.0000</span></div>
										<svg
											xmlns="http://www.w3.org/2000/svg"
											viewBox="0 0 20 20"
											fill="currentColor"
											aria-hidden="true"
											class="ui-open:rotate-180 ui-open:transform h-4 w-4 transition-all duration-150 delay-300"
											><path
												fill-rule="evenodd"
												d="M5.23 7.21a.75.75 0 011.06.02L10 11.168l3.71-3.938a.75.75 0 111.08 1.04l-4.25 4.5a.75.75 0 01-1.08 0l-4.25-4.5a.75.75 0 01.02-1.06z"
												clip-rule="evenodd"
											/></svg
										>
									</div></button
								>
							</div>
						</div>
					</div>
				</div>
				<div class="mt-5 sm:mt-6 sm:grid sm:grid-flow-row-dense sm:grid-cols-2 sm:gap-3">
					<button
						on:click={() => (sendDialogIsOpen = false)}
						type="button"
						class="inline-flex w-full justify-center rounded-md bg-indigo-600 px-3 py-2 text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600 sm:col-start-2"
						>Confirm</button
					>
					<button
						on:click={() => (sendDialogIsOpen = false)}
						type="button"
						class="mt-3 inline-flex w-full justify-center rounded-md bg-white px-3 py-2 text-sm font-semibold text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 hover:bg-gray-50 sm:col-start-1 sm:mt-0"
						>Cancel</button
					>
				</div>
			</div>
		</div>
	</div>
</Dialog>

<main>
	<div class="mx-auto max-w-7xl sm:px-6 lg:px-8">
		<header class="pb-4 pt-6 sm:pb-6">
			<div class="mx-auto flex max-w-7xl flex-wrap items-center gap-6 sm:flex-nowrap px-6">
				<h1 class="text-base font-semibold leading-7 text-gray-900">Dashboard</h1>

				<button
					on:click={() => (sendDialogIsOpen = true)}
					class="ml-auto flex items-center gap-x-1 rounded-md bg-indigo-600 px-3 py-2 text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600"
				>
					<svg class="-ml-1.5 h-5 w-5" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true">
						<path
							d="M10.75 6.75a.75.75 0 00-1.5 0v2.5h-2.5a.75.75 0 000 1.5h2.5v2.5a.75.75 0 001.5 0v-2.5h2.5a.75.75 0 000-1.5h-2.5v-2.5z"
						/>
					</svg>
					Send
				</button>
			</div>
		</header>

		<div class="relative isolate overflow-hidden bg-white">
			<!-- Stats -->
			<div class="border-b border-b-gray-900/10 lg:border-t lg:border-t-gray-900/5">
				<dl
					class="mx-auto grid max-w-7xl grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 lg:px-2 xl:px-0"
				>
					<div
						class="flex items-baseline flex-wrap justify-between gap-y-2 gap-x-4 border-t border-gray-900/5 px-4 py-10 sm:px-6 lg:border-t-0 xl:px-8"
					>
						<dt class="text-sm font-medium leading-6 text-gray-500">Revenue</dt>
						<dd class="text-xs font-medium text-gray-700">+4.75%</dd>
						<dd
							class="w-full flex-none text-3xl font-medium leading-10 tracking-tight text-gray-900"
						>
							$405,091.00
						</dd>
					</div>
					<div
						class="flex items-baseline flex-wrap justify-between gap-y-2 gap-x-4 border-t border-gray-900/5 px-4 py-10 sm:px-6 lg:border-t-0 xl:px-8 sm:border-l"
					>
						<dt class="text-sm font-medium leading-6 text-gray-500">Overdue invoices</dt>
						<dd class="text-xs font-medium text-rose-600">+54.02%</dd>
						<dd
							class="w-full flex-none text-3xl font-medium leading-10 tracking-tight text-gray-900"
						>
							$12,787.00
						</dd>
					</div>
					<div
						class="flex items-baseline flex-wrap justify-between gap-y-2 gap-x-4 border-t border-gray-900/5 px-4 py-10 sm:px-6 lg:border-t-0 xl:px-8 lg:border-l"
					>
						<dt class="text-sm font-medium leading-6 text-gray-500">Outstanding invoices</dt>
						<dd class="text-xs font-medium text-gray-700">-1.39%</dd>
						<dd
							class="w-full flex-none text-3xl font-medium leading-10 tracking-tight text-gray-900"
						>
							$245,988.00
						</dd>
					</div>
					<div
						class="flex items-baseline flex-wrap justify-between gap-y-2 gap-x-4 border-t border-gray-900/5 px-4 py-10 sm:px-6 lg:border-t-0 xl:px-8 sm:border-l"
					>
						<dt class="text-sm font-medium leading-6 text-gray-500">Expenses</dt>
						<dd class="text-xs font-medium text-rose-600">+10.18%</dd>
						<dd
							class="w-full flex-none text-3xl font-medium leading-10 tracking-tight text-gray-900"
						>
							$30,156.00
						</dd>
					</div>
				</dl>
			</div>

			<div
				class="absolute left-0 top-full -z-10 mt-96 origin-top-left translate-y-40 -rotate-90 transform-gpu opacity-20 blur-3xl sm:left-1/2 sm:-ml-96 sm:-mt-10 sm:translate-y-0 sm:rotate-0 sm:transform-gpu sm:opacity-50"
				aria-hidden="true"
			>
				<div
					class="aspect-[1154/678] w-[72.125rem] bg-gradient-to-br from-[#FF80B5] to-[#9089FC]"
					style="clip-path: polygon(100% 38.5%, 82.6% 100%, 60.2% 37.7%, 52.4% 32.1%, 47.5% 41.8%, 45.2% 65.6%, 27.5% 23.4%, 0.1% 35.3%, 17.9% 0%, 27.7% 23.4%, 76.2% 2.5%, 74.2% 56%, 100% 38.5%)"
				/>
			</div>
		</div>

		<div class="space-y-16 xl:space-y-20 bg-white">
			<!-- Recent activity table -->
			<div>
				<div class="overflow-hidden border-t border-gray-100">
					<div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
						<div class="mx-auto max-w-2xl lg:mx-0 lg:max-w-none">
							<table class="w-full text-left">
								<thead class="sr-only">
									<tr>
										<th>Amount</th>
										<th class="hidden sm:table-cell">Client</th>
										<th>More details</th>
									</tr>
								</thead>
								<tbody>
									<tr class="text-sm leading-6 text-gray-900">
										<th scope="colgroup" colspan="3" class="relative isolate py-2 font-semibold">
											<time datetime="2023-03-22">Today</time>
											<div
												class="absolute inset-y-0 right-full -z-10 w-screen border-b border-gray-200 bg-gray-100"
											/>
											<div
												class="absolute inset-y-0 left-0 -z-10 w-screen border-b border-gray-200 bg-gray-100"
											/>
										</th>
									</tr>
									<tr>
										<td class="relative py-5 pr-6">
											<div class="flex gap-x-6">
												<svg
													class="hidden h-6 w-5 flex-none text-gray-400 sm:block"
													viewBox="0 0 20 20"
													fill="currentColor"
													aria-hidden="true"
												>
													<path
														fill-rule="evenodd"
														d="M10 18a8 8 0 100-16 8 8 0 000 16zm-.75-4.75a.75.75 0 001.5 0V8.66l1.95 2.1a.75.75 0 101.1-1.02l-3.25-3.5a.75.75 0 00-1.1 0L6.2 9.74a.75.75 0 101.1 1.02l1.95-2.1v4.59z"
														clip-rule="evenodd"
													/>
												</svg>
												<div class="flex-auto">
													<div class="flex items-start gap-x-3">
														<div class="text-sm font-medium leading-6 text-gray-900">
															$7,600.00 USD
														</div>
														<div
															class="rounded-md py-1 px-2 text-xs font-medium ring-1 ring-inset text-green-700 bg-green-50 ring-green-600/20"
														>
															Paid
														</div>
													</div>
													<div class="mt-1 text-xs leading-5 text-gray-500">$500.00 tax</div>
												</div>
											</div>
											<div class="absolute bottom-0 right-full h-px w-screen bg-gray-100" />
											<div class="absolute bottom-0 left-0 h-px w-screen bg-gray-100" />
										</td>
										<td class="hidden py-5 pr-6 sm:table-cell">
											<div class="text-sm leading-6 text-gray-900">Reform</div>
											<div class="mt-1 text-xs leading-5 text-gray-500">Website redesign</div>
										</td>
										<td class="py-5 text-right">
											<div class="flex justify-end">
												<a
													href="/app/transactions/a1"
													class="text-sm font-medium leading-6 text-indigo-600 hover:text-indigo-500"
													>View<span class="hidden sm:inline"> transaction</span><span
														class="sr-only">, invoice #00012, Reform</span
													></a
												>
											</div>
											<div class="mt-1 text-xs leading-5 text-gray-500">
												Invoice <span class="text-gray-900">#00012</span>
											</div>
										</td>
									</tr>
									<tr>
										<td class="relative py-5 pr-6">
											<div class="flex gap-x-6">
												<svg
													class="hidden h-6 w-5 flex-none text-gray-400 sm:block"
													viewBox="0 0 20 20"
													fill="currentColor"
													aria-hidden="true"
												>
													<path
														fill-rule="evenodd"
														d="M10 18a8 8 0 100-16 8 8 0 000 16zm.75-11.25a.75.75 0 00-1.5 0v4.59L7.3 9.24a.75.75 0 00-1.1 1.02l3.25 3.5a.75.75 0 001.1 0l3.25-3.5a.75.75 0 10-1.1-1.02l-1.95 2.1V6.75z"
														clip-rule="evenodd"
													/>
												</svg>
												<div class="flex-auto">
													<div class="flex items-start gap-x-3">
														<div class="text-sm font-medium leading-6 text-gray-900">
															$10,000.00 USD
														</div>
														<div
															class="rounded-md py-1 px-2 text-xs font-medium ring-1 ring-inset text-gray-600 bg-gray-50 ring-gray-500/10"
														>
															Withdraw
														</div>
													</div>
												</div>
											</div>
											<div class="absolute bottom-0 right-full h-px w-screen bg-gray-100" />
											<div class="absolute bottom-0 left-0 h-px w-screen bg-gray-100" />
										</td>
										<td class="hidden py-5 pr-6 sm:table-cell">
											<div class="text-sm leading-6 text-gray-900">Tom Cook</div>
											<div class="mt-1 text-xs leading-5 text-gray-500">Salary</div>
										</td>
										<td class="py-5 text-right">
											<div class="flex justify-end">
												<a
													href="/app/transactions/a1"
													class="text-sm font-medium leading-6 text-indigo-600 hover:text-indigo-500"
													>View<span class="hidden sm:inline"> transaction</span><span
														class="sr-only">, invoice #00011, Tom Cook</span
													></a
												>
											</div>
											<div class="mt-1 text-xs leading-5 text-gray-500">
												Invoice <span class="text-gray-900">#00011</span>
											</div>
										</td>
									</tr>
									<tr>
										<td class="relative py-5 pr-6">
											<div class="flex gap-x-6">
												<svg
													class="hidden h-6 w-5 flex-none text-gray-400 sm:block"
													viewBox="0 0 20 20"
													fill="currentColor"
													aria-hidden="true"
												>
													<path
														fill-rule="evenodd"
														d="M15.312 11.424a5.5 5.5 0 01-9.201 2.466l-.312-.311h2.433a.75.75 0 000-1.5H3.989a.75.75 0 00-.75.75v4.242a.75.75 0 001.5 0v-2.43l.31.31a7 7 0 0011.712-3.138.75.75 0 00-1.449-.39zm1.23-3.723a.75.75 0 00.219-.53V2.929a.75.75 0 00-1.5 0V5.36l-.31-.31A7 7 0 003.239 8.188a.75.75 0 101.448.389A5.5 5.5 0 0113.89 6.11l.311.31h-2.432a.75.75 0 000 1.5h4.243a.75.75 0 00.53-.219z"
														clip-rule="evenodd"
													/>
												</svg>
												<div class="flex-auto">
													<div class="flex items-start gap-x-3">
														<div class="text-sm font-medium leading-6 text-gray-900">
															$2,000.00 USD
														</div>
														<div
															class="rounded-md py-1 px-2 text-xs font-medium ring-1 ring-inset text-red-700 bg-red-50 ring-red-600/10"
														>
															Overdue
														</div>
													</div>
													<div class="mt-1 text-xs leading-5 text-gray-500">$130.00 tax</div>
												</div>
											</div>
											<div class="absolute bottom-0 right-full h-px w-screen bg-gray-100" />
											<div class="absolute bottom-0 left-0 h-px w-screen bg-gray-100" />
										</td>
										<td class="hidden py-5 pr-6 sm:table-cell">
											<div class="text-sm leading-6 text-gray-900">Tuple</div>
											<div class="mt-1 text-xs leading-5 text-gray-500">Logo design</div>
										</td>
										<td class="py-5 text-right">
											<div class="flex justify-end">
												<a
													href="/app/transactions/a1"
													class="text-sm font-medium leading-6 text-indigo-600 hover:text-indigo-500"
													>View<span class="hidden sm:inline"> transaction</span><span
														class="sr-only">, invoice #00009, Tuple</span
													></a
												>
											</div>
											<div class="mt-1 text-xs leading-5 text-gray-500">
												Invoice <span class="text-gray-900">#00009</span>
											</div>
										</td>
									</tr>

									<tr class="text-sm leading-6 text-gray-900">
										<th scope="colgroup" colspan="3" class="relative isolate py-2 font-semibold">
											<time datetime="2023-03-21">Yesterday</time>
											<div
												class="absolute inset-y-0 right-full -z-10 w-screen border-b border-gray-200 bg-gray-100"
											/>
											<div
												class="absolute inset-y-0 left-0 -z-10 w-screen border-b border-gray-200 bg-gray-100"
											/>
										</th>
									</tr>
									<tr>
										<td class="relative py-5 pr-6">
											<div class="flex gap-x-6">
												<svg
													class="hidden h-6 w-5 flex-none text-gray-400 sm:block"
													viewBox="0 0 20 20"
													fill="currentColor"
													aria-hidden="true"
												>
													<path
														fill-rule="evenodd"
														d="M10 18a8 8 0 100-16 8 8 0 000 16zm-.75-4.75a.75.75 0 001.5 0V8.66l1.95 2.1a.75.75 0 101.1-1.02l-3.25-3.5a.75.75 0 00-1.1 0L6.2 9.74a.75.75 0 101.1 1.02l1.95-2.1v4.59z"
														clip-rule="evenodd"
													/>
												</svg>
												<div class="flex-auto">
													<div class="flex items-start gap-x-3">
														<div class="text-sm font-medium leading-6 text-gray-900">
															$14,000.00 USD
														</div>
														<div
															class="rounded-md py-1 px-2 text-xs font-medium ring-1 ring-inset text-green-700 bg-green-50 ring-green-600/20"
														>
															Paid
														</div>
													</div>
													<div class="mt-1 text-xs leading-5 text-gray-500">$900.00 tax</div>
												</div>
											</div>
											<div class="absolute bottom-0 right-full h-px w-screen bg-gray-100" />
											<div class="absolute bottom-0 left-0 h-px w-screen bg-gray-100" />
										</td>
										<td class="hidden py-5 pr-6 sm:table-cell">
											<div class="text-sm leading-6 text-gray-900">SavvyCal</div>
											<div class="mt-1 text-xs leading-5 text-gray-500">Website redesign</div>
										</td>
										<td class="py-5 text-right">
											<div class="flex justify-end">
												<a
													href="/app/transactions/a1"
													class="text-sm font-medium leading-6 text-indigo-600 hover:text-indigo-500"
													>View<span class="hidden sm:inline"> transaction</span><span
														class="sr-only">, invoice #00010, SavvyCal</span
													></a
												>
											</div>
											<div class="mt-1 text-xs leading-5 text-gray-500">
												Invoice <span class="text-gray-900">#00010</span>
											</div>
										</td>
									</tr>
								</tbody>
							</table>
						</div>
					</div>
				</div>
			</div>

			<!-- Recent client list-->
			<div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8 pb-4 sm:pb-6 lg:pb-8">
				<div class="mx-auto max-w-2xl lg:mx-0 lg:max-w-none">
					<div class="flex items-center justify-between">
						<h2 class="text-base font-semibold leading-7 text-gray-900">Recent clients</h2>
						<a
							href="#"
							class="text-sm font-semibold leading-6 text-indigo-600 hover:text-indigo-500"
							>View all<span class="sr-only">, clients</span></a
						>
					</div>
					<ul role="list" class="mt-6 grid grid-cols-1 gap-x-6 gap-y-8 lg:grid-cols-3 xl:gap-x-8">
						<li class="overflow-hidden rounded-xl border border-gray-200">
							<div class="flex items-center gap-x-4 border-b border-gray-900/5 bg-gray-50 p-6">
								<img
									src="https://tailwindui.com/img/logos/48x48/tuple.svg"
									alt="Tuple"
									class="h-12 w-12 flex-none rounded-lg bg-white object-cover ring-1 ring-gray-900/10"
								/>
								<div class="text-sm font-medium leading-6 text-gray-900">Tuple</div>
								<div class="relative ml-auto">
									<button
										type="button"
										class="-m-2.5 block p-2.5 text-gray-400 hover:text-gray-500"
										id="options-menu-0-button"
										aria-expanded="false"
										aria-haspopup="true"
									>
										<span class="sr-only">Open options</span>
										<svg class="h-5 w-5" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true">
											<path
												d="M3 10a1.5 1.5 0 113 0 1.5 1.5 0 01-3 0zM8.5 10a1.5 1.5 0 113 0 1.5 1.5 0 01-3 0zM15.5 8.5a1.5 1.5 0 100 3 1.5 1.5 0 000-3z"
											/>
										</svg>
									</button>

									<!--
                        Dropdown menu, show/hide based on menu state.
      
                        Entering: "transition ease-out duration-100"
                          From: "transform opacity-0 scale-95"
                          To: "transform opacity-100 scale-100"
                        Leaving: "transition ease-in duration-75"
                          From: "transform opacity-100 scale-100"
                          To: "transform opacity-0 scale-95"
                      -->
									<!-- HeadlessUI -->
									<!-- <div
										class="absolute right-0 z-10 mt-0.5 w-32 origin-top-right rounded-md bg-white py-2 shadow-lg ring-1 ring-gray-900/5 focus:outline-none"
										role="menu"
										aria-orientation="vertical"
										aria-labelledby="options-menu-0-button"
										tabindex="-1"
									> -->
									<!-- Active: "bg-gray-50", Not Active: "" -->
									<!-- <a
											href="#"
											class="block px-3 py-1 text-sm leading-6 text-gray-900"
											role="menuitem"
											tabindex="-1"
											id="options-menu-0-item-0">View<span class="sr-only">, Tuple</span></a
										>
										<a
											href="#"
											class="block px-3 py-1 text-sm leading-6 text-gray-900"
											role="menuitem"
											tabindex="-1"
											id="options-menu-0-item-1">Edit<span class="sr-only">, Tuple</span></a
										> -->
									<!-- </div> -->
								</div>
							</div>
							<dl class="-my-3 divide-y divide-gray-100 px-6 py-4 text-sm leading-6">
								<div class="flex justify-between gap-x-4 py-3">
									<dt class="text-gray-500">Last invoice</dt>
									<dd class="text-gray-700">
										<time datetime="2022-12-13">December 13, 2022</time>
									</dd>
								</div>
								<div class="flex justify-between gap-x-4 py-3">
									<dt class="text-gray-500">Amount</dt>
									<dd class="flex items-start gap-x-2">
										<div class="font-medium text-gray-900">$2,000.00</div>
										<div
											class="rounded-md py-1 px-2 text-xs font-medium ring-1 ring-inset text-red-700 bg-red-50 ring-red-600/10"
										>
											Overdue
										</div>
									</dd>
								</div>
							</dl>
						</li>
						<li class="overflow-hidden rounded-xl border border-gray-200">
							<div class="flex items-center gap-x-4 border-b border-gray-900/5 bg-gray-50 p-6">
								<img
									src="https://tailwindui.com/img/logos/48x48/savvycal.svg"
									alt="SavvyCal"
									class="h-12 w-12 flex-none rounded-lg bg-white object-cover ring-1 ring-gray-900/10"
								/>
								<div class="text-sm font-medium leading-6 text-gray-900">SavvyCal</div>
								<div class="relative ml-auto">
									<button
										type="button"
										class="-m-2.5 block p-2.5 text-gray-400 hover:text-gray-500"
										id="options-menu-1-button"
										aria-expanded="false"
										aria-haspopup="true"
									>
										<span class="sr-only">Open options</span>
										<svg class="h-5 w-5" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true">
											<path
												d="M3 10a1.5 1.5 0 113 0 1.5 1.5 0 01-3 0zM8.5 10a1.5 1.5 0 113 0 1.5 1.5 0 01-3 0zM15.5 8.5a1.5 1.5 0 100 3 1.5 1.5 0 000-3z"
											/>
										</svg>
									</button>

									<!--
                        Dropdown menu, show/hide based on menu state.
      
                        Entering: "transition ease-out duration-100"
                          From: "transform opacity-0 scale-95"
                          To: "transform opacity-100 scale-100"
                        Leaving: "transition ease-in duration-75"
                          From: "transform opacity-100 scale-100"
                          To: "transform opacity-0 scale-95"
                      -->
									<!-- HeadlessUI -->
									<!-- <div
										class="absolute right-0 z-10 mt-0.5 w-32 origin-top-right rounded-md bg-white py-2 shadow-lg ring-1 ring-gray-900/5 focus:outline-none"
										role="menu"
										aria-orientation="vertical"
										aria-labelledby="options-menu-1-button"
										tabindex="-1"
									> -->
									<!-- Active: "bg-gray-50", Not Active: "" -->
									<!-- <a
											href="#"
											class="block px-3 py-1 text-sm leading-6 text-gray-900"
											role="menuitem"
											tabindex="-1"
											id="options-menu-1-item-0">View<span class="sr-only">, SavvyCal</span></a
										>
										<a
											href="#"
											class="block px-3 py-1 text-sm leading-6 text-gray-900"
											role="menuitem"
											tabindex="-1"
											id="options-menu-1-item-1">Edit<span class="sr-only">, SavvyCal</span></a
										> -->
									<!-- </div> -->
								</div>
							</div>
							<dl class="-my-3 divide-y divide-gray-100 px-6 py-4 text-sm leading-6">
								<div class="flex justify-between gap-x-4 py-3">
									<dt class="text-gray-500">Last invoice</dt>
									<dd class="text-gray-700"><time datetime="2023-01-22">January 22, 2023</time></dd>
								</div>
								<div class="flex justify-between gap-x-4 py-3">
									<dt class="text-gray-500">Amount</dt>
									<dd class="flex items-start gap-x-2">
										<div class="font-medium text-gray-900">$14,000.00</div>
										<div
											class="rounded-md py-1 px-2 text-xs font-medium ring-1 ring-inset text-green-700 bg-green-50 ring-green-600/20"
										>
											Paid
										</div>
									</dd>
								</div>
							</dl>
						</li>
						<li class="overflow-hidden rounded-xl border border-gray-200">
							<div class="flex items-center gap-x-4 border-b border-gray-900/5 bg-gray-50 p-6">
								<img
									src="https://tailwindui.com/img/logos/48x48/reform.svg"
									alt="Reform"
									class="h-12 w-12 flex-none rounded-lg bg-white object-cover ring-1 ring-gray-900/10"
								/>
								<div class="text-sm font-medium leading-6 text-gray-900">Reform</div>
								<div class="relative ml-auto">
									<button
										type="button"
										class="-m-2.5 block p-2.5 text-gray-400 hover:text-gray-500"
										id="options-menu-2-button"
										aria-expanded="false"
										aria-haspopup="true"
									>
										<span class="sr-only">Open options</span>
										<svg class="h-5 w-5" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true">
											<path
												d="M3 10a1.5 1.5 0 113 0 1.5 1.5 0 01-3 0zM8.5 10a1.5 1.5 0 113 0 1.5 1.5 0 01-3 0zM15.5 8.5a1.5 1.5 0 100 3 1.5 1.5 0 000-3z"
											/>
										</svg>
									</button>

									<!--
                        Dropdown menu, show/hide based on menu state.
      
                        Entering: "transition ease-out duration-100"
                          From: "transform opacity-0 scale-95"
                          To: "transform opacity-100 scale-100"
                        Leaving: "transition ease-in duration-75"
                          From: "transform opacity-100 scale-100"
                          To: "transform opacity-0 scale-95"
                      -->
									<!-- HeadlessUI -->
									<!-- <div
										class="absolute right-0 z-10 mt-0.5 w-32 origin-top-right rounded-md bg-white py-2 shadow-lg ring-1 ring-gray-900/5 focus:outline-none"
										role="menu"
										aria-orientation="vertical"
										aria-labelledby="options-menu-2-button"
										tabindex="-1"
									> -->
									<!-- Active: "bg-gray-50", Not Active: "" -->
									<!-- <a
											href="#"
											class="block px-3 py-1 text-sm leading-6 text-gray-900"
											role="menuitem"
											tabindex="-1"
											id="options-menu-2-item-0">View<span class="sr-only">, Reform</span></a
										>
										<a
											href="#"
											class="block px-3 py-1 text-sm leading-6 text-gray-900"
											role="menuitem"
											tabindex="-1"
											id="options-menu-2-item-1">Edit<span class="sr-only">, Reform</span></a
										> -->
									<!-- </div> -->
								</div>
							</div>
							<dl class="-my-3 divide-y divide-gray-100 px-6 py-4 text-sm leading-6">
								<div class="flex justify-between gap-x-4 py-3">
									<dt class="text-gray-500">Last invoice</dt>
									<dd class="text-gray-700"><time datetime="2023-01-23">January 23, 2023</time></dd>
								</div>
								<div class="flex justify-between gap-x-4 py-3">
									<dt class="text-gray-500">Amount</dt>
									<dd class="flex items-start gap-x-2">
										<div class="font-medium text-gray-900">$7,600.00</div>
										<div
											class="rounded-md py-1 px-2 text-xs font-medium ring-1 ring-inset text-green-700 bg-green-50 ring-green-600/20"
										>
											Paid
										</div>
									</dd>
								</div>
							</dl>
						</li>
					</ul>
				</div>
			</div>
		</div>
	</div>
</main>
