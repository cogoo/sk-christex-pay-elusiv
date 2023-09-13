<!--
  This example requires some changes to your config:
  
  ```
  // tailwind.config.js
  module.exports = {
    // ...
    plugins: [
      // ...
      require('@tailwindcss/forms'),
    ],
  }
  ```
-->

<main class="">
	<header class="relative isolate">
		<div class="absolute inset-0 -z-10 overflow-hidden" aria-hidden="true">
			<div
				class="absolute left-16 top-full -mt-16 transform-gpu opacity-50 blur-3xl xl:left-1/2 xl:-ml-80"
			>
				<div
					class="aspect-[1154/678] w-[72.125rem] bg-gradient-to-br from-[#FF80B5] to-[#9089FC]"
					style="clip-path: polygon(100% 38.5%, 82.6% 100%, 60.2% 37.7%, 52.4% 32.1%, 47.5% 41.8%, 45.2% 65.6%, 27.5% 23.4%, 0.1% 35.3%, 17.9% 0%, 27.7% 23.4%, 76.2% 2.5%, 74.2% 56%, 100% 38.5%)"
				/>
			</div>
			<div class="absolute inset-x-0 bottom-0 h-px bg-gray-900/5" />
		</div>

		<div class="mx-auto max-w-7xl px-4 py-10 sm:px-6 lg:px-8">
			<div
				class="mx-auto flex max-w-2xl items-center justify-between gap-x-8 lg:mx-0 lg:max-w-none"
			>
				<div class="flex items-center gap-x-6">
					<img
						src="https://tailwindui.com/img/logos/48x48/tuple.svg"
						alt=""
						class="h-16 w-16 flex-none rounded-full ring-1 ring-gray-900/10"
					/>
					<h1>
						<div class="text-sm leading-6 text-gray-500">
							Invoice <span class="text-gray-700">#00011</span>
						</div>
						<div class="mt-1 text-base font-semibold leading-6 text-gray-900">Tuple, Inc</div>
					</h1>
				</div>
				<div class="flex items-center gap-x-4 sm:gap-x-6">
					<button
						type="button"
						class="hidden text-sm font-semibold leading-6 text-gray-900 sm:block">Copy URL</button
					>
					<a
						href="#"
						class="rounded-md bg-indigo-600 px-3 py-2 text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600"
						>Send</a
					>

					<div class="relative sm:hidden">
						<button
							type="button"
							class="-m-3 block p-3"
							id="more-menu-button"
							aria-expanded="false"
							aria-haspopup="true"
						>
							<span class="sr-only">More</span>
							<svg
								class="h-5 w-5 text-gray-500"
								viewBox="0 0 20 20"
								fill="currentColor"
								aria-hidden="true"
							>
								<path
									d="M10 3a1.5 1.5 0 110 3 1.5 1.5 0 010-3zM10 8.5a1.5 1.5 0 110 3 1.5 1.5 0 010-3zM11.5 15.5a1.5 1.5 0 10-3 0 1.5 1.5 0 003 0z"
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
						<div
							class="absolute right-0 z-10 mt-0.5 w-32 origin-top-right rounded-md bg-white py-2 shadow-lg ring-1 ring-gray-900/5 focus:outline-none"
							role="menu"
							aria-orientation="vertical"
							aria-labelledby="more-menu-button"
							tabindex="-1"
						>
							<!-- Active: "bg-gray-50", Not Active: "" -->
							<button
								type="button"
								class="block w-full px-3 py-1 text-left text-sm leading-6 text-gray-900"
								role="menuitem"
								tabindex="-1"
								id="more-menu-item-0">Copy URL</button
							>
							<a
								href="#"
								class="block px-3 py-1 text-sm leading-6 text-gray-900"
								role="menuitem"
								tabindex="-1"
								id="more-menu-item-1">Edit</a
							>
						</div>
					</div>
				</div>
			</div>
		</div>
	</header>

	<div class="mx-auto max-w-7xl px-4 py-16 sm:px-6 lg:px-8">
		<div
			class="mx-auto grid max-w-2xl grid-cols-1 grid-rows-1 items-start gap-x-8 gap-y-8 lg:mx-0 lg:max-w-none lg:grid-cols-3"
		>
			<!-- Invoice summary -->
			<div class="lg:col-start-3 lg:row-end-1">
				<h2 class="sr-only">Summary</h2>
				<div class="rounded-lg bg-gray-50 shadow-sm ring-1 ring-gray-900/5">
					<dl class="flex flex-wrap">
						<div class="flex-auto pl-6 pt-6">
							<dt class="text-sm font-semibold leading-6 text-gray-900">Amount</dt>
							<dd class="mt-1 text-base font-semibold leading-6 text-gray-900">$10,560.00</dd>
						</div>
						<div class="flex-none self-end px-6 pt-4">
							<dt class="sr-only">Status</dt>
							<dd
								class="rounded-md bg-green-50 px-2 py-1 text-xs font-medium text-green-600 ring-1 ring-inset ring-green-600/20"
							>
								Paid
							</dd>
						</div>
						<div class="mt-6 flex w-full flex-none gap-x-4 border-t border-gray-900/5 px-6 pt-6">
							<dt class="flex-none">
								<span class="sr-only">Client</span>
								<svg
									class="h-6 w-5 text-gray-400"
									viewBox="0 0 20 20"
									fill="currentColor"
									aria-hidden="true"
								>
									<path
										fill-rule="evenodd"
										d="M18 10a8 8 0 11-16 0 8 8 0 0116 0zm-5.5-2.5a2.5 2.5 0 11-5 0 2.5 2.5 0 015 0zM10 12a5.99 5.99 0 00-4.793 2.39A6.483 6.483 0 0010 16.5a6.483 6.483 0 004.793-2.11A5.99 5.99 0 0010 12z"
										clip-rule="evenodd"
									/>
								</svg>
							</dt>
							<dd class="text-sm font-medium leading-6 text-gray-900">Alex Curren</dd>
						</div>
						<div class="mt-4 flex w-full flex-none gap-x-4 px-6">
							<dt class="flex-none">
								<span class="sr-only">Due date</span>
								<svg
									class="h-6 w-5 text-gray-400"
									viewBox="0 0 20 20"
									fill="currentColor"
									aria-hidden="true"
								>
									<path
										d="M5.25 12a.75.75 0 01.75-.75h.01a.75.75 0 01.75.75v.01a.75.75 0 01-.75.75H6a.75.75 0 01-.75-.75V12zM6 13.25a.75.75 0 00-.75.75v.01c0 .414.336.75.75.75h.01a.75.75 0 00.75-.75V14a.75.75 0 00-.75-.75H6zM7.25 12a.75.75 0 01.75-.75h.01a.75.75 0 01.75.75v.01a.75.75 0 01-.75.75H8a.75.75 0 01-.75-.75V12zM8 13.25a.75.75 0 00-.75.75v.01c0 .414.336.75.75.75h.01a.75.75 0 00.75-.75V14a.75.75 0 00-.75-.75H8zM9.25 10a.75.75 0 01.75-.75h.01a.75.75 0 01.75.75v.01a.75.75 0 01-.75.75H10a.75.75 0 01-.75-.75V10zM10 11.25a.75.75 0 00-.75.75v.01c0 .414.336.75.75.75h.01a.75.75 0 00.75-.75V12a.75.75 0 00-.75-.75H10zM9.25 14a.75.75 0 01.75-.75h.01a.75.75 0 01.75.75v.01a.75.75 0 01-.75.75H10a.75.75 0 01-.75-.75V14zM12 9.25a.75.75 0 00-.75.75v.01c0 .414.336.75.75.75h.01a.75.75 0 00.75-.75V10a.75.75 0 00-.75-.75H12zM11.25 12a.75.75 0 01.75-.75h.01a.75.75 0 01.75.75v.01a.75.75 0 01-.75.75H12a.75.75 0 01-.75-.75V12zM12 13.25a.75.75 0 00-.75.75v.01c0 .414.336.75.75.75h.01a.75.75 0 00.75-.75V14a.75.75 0 00-.75-.75H12zM13.25 10a.75.75 0 01.75-.75h.01a.75.75 0 01.75.75v.01a.75.75 0 01-.75.75H14a.75.75 0 01-.75-.75V10zM14 11.25a.75.75 0 00-.75.75v.01c0 .414.336.75.75.75h.01a.75.75 0 00.75-.75V12a.75.75 0 00-.75-.75H14z"
									/>
									<path
										fill-rule="evenodd"
										d="M5.75 2a.75.75 0 01.75.75V4h7V2.75a.75.75 0 011.5 0V4h.25A2.75 2.75 0 0118 6.75v8.5A2.75 2.75 0 0115.25 18H4.75A2.75 2.75 0 012 15.25v-8.5A2.75 2.75 0 014.75 4H5V2.75A.75.75 0 015.75 2zm-1 5.5c-.69 0-1.25.56-1.25 1.25v6.5c0 .69.56 1.25 1.25 1.25h10.5c.69 0 1.25-.56 1.25-1.25v-6.5c0-.69-.56-1.25-1.25-1.25H4.75z"
										clip-rule="evenodd"
									/>
								</svg>
							</dt>
							<dd class="text-sm leading-6 text-gray-500">
								<time datetime="2023-01-31">January 31, 2023</time>
							</dd>
						</div>
						<div class="mt-4 flex w-full flex-none gap-x-4 px-6">
							<dt class="flex-none">
								<span class="sr-only">Status</span>
								<svg
									class="h-6 w-5 text-gray-400"
									viewBox="0 0 20 20"
									fill="currentColor"
									aria-hidden="true"
								>
									<path
										fill-rule="evenodd"
										d="M2.5 4A1.5 1.5 0 001 5.5V6h18v-.5A1.5 1.5 0 0017.5 4h-15zM19 8.5H1v6A1.5 1.5 0 002.5 16h15a1.5 1.5 0 001.5-1.5v-6zM3 13.25a.75.75 0 01.75-.75h1.5a.75.75 0 010 1.5h-1.5a.75.75 0 01-.75-.75zm4.75-.75a.75.75 0 000 1.5h3.5a.75.75 0 000-1.5h-3.5z"
										clip-rule="evenodd"
									/>
								</svg>
							</dt>
							<dd class="text-sm leading-6 text-gray-500">Paid with MasterCard</dd>
						</div>
					</dl>
					<div class="mt-6 border-t border-gray-900/5 px-6 py-6">
						<a href="#" class="text-sm font-semibold leading-6 text-gray-900"
							>Download receipt <span aria-hidden="true">&rarr;</span></a
						>
					</div>
				</div>
			</div>

			<!-- Invoice -->
			<div
				class="-mx-4 px-4 py-8 shadow-sm ring-1 ring-gray-900/5 sm:mx-0 sm:rounded-lg sm:px-8 sm:pb-14 lg:col-span-2 lg:row-span-2 lg:row-end-2 xl:px-16 xl:pb-20 xl:pt-16 bg-white"
			>
				<h2 class="text-base font-semibold leading-6 text-gray-900">Invoice</h2>
				<dl class="mt-6 grid grid-cols-1 text-sm leading-6 sm:grid-cols-2">
					<div class="sm:pr-4">
						<dt class="inline text-gray-500">Issued on</dt>
						<dd class="inline text-gray-700">
							<time datetime="2023-23-01">January 23, 2023</time>
						</dd>
					</div>
					<div class="mt-2 sm:mt-0 sm:pl-4">
						<dt class="inline text-gray-500">Due on</dt>
						<dd class="inline text-gray-700">
							<time datetime="2023-31-01">January 31, 2023</time>
						</dd>
					</div>
					<div class="mt-6 border-t border-gray-900/5 pt-6 sm:pr-4">
						<dt class="font-semibold text-gray-900">From</dt>
						<dd class="mt-2 text-gray-500">
							<span class="font-medium text-gray-900">Acme, Inc.</span><br />7363 Cynthia Pass<br
							/>Toronto, ON N3Y 4H8
						</dd>
					</div>
					<div class="mt-8 sm:mt-6 sm:border-t sm:border-gray-900/5 sm:pl-4 sm:pt-6">
						<dt class="font-semibold text-gray-900">To</dt>
						<dd class="mt-2 text-gray-500">
							<span class="font-medium text-gray-900">Tuple, Inc</span><br />886 Walter Street<br
							/>New York, NY 12345
						</dd>
					</div>
				</dl>
				<table class="mt-16 w-full whitespace-nowrap text-left text-sm leading-6">
					<colgroup>
						<col class="w-full" />
						<col />
						<col />
						<col />
					</colgroup>
					<thead class="border-b border-gray-200 text-gray-900">
						<tr>
							<th scope="col" class="px-0 py-3 font-semibold">Projects</th>
							<th scope="col" class="hidden py-3 pl-8 pr-0 text-right font-semibold sm:table-cell"
								>Hours</th
							>
							<th scope="col" class="hidden py-3 pl-8 pr-0 text-right font-semibold sm:table-cell"
								>Rate</th
							>
							<th scope="col" class="py-3 pl-8 pr-0 text-right font-semibold">Price</th>
						</tr>
					</thead>
					<tbody>
						<tr class="border-b border-gray-100">
							<td class="max-w-0 px-0 py-5 align-top">
								<div class="truncate font-medium text-gray-900">Logo redesign</div>
								<div class="truncate text-gray-500">New logo and digital asset playbook.</div>
							</td>
							<td
								class="hidden py-5 pl-8 pr-0 text-right align-top tabular-nums text-gray-700 sm:table-cell"
								>20.0</td
							>
							<td
								class="hidden py-5 pl-8 pr-0 text-right align-top tabular-nums text-gray-700 sm:table-cell"
								>$100.00</td
							>
							<td class="py-5 pl-8 pr-0 text-right align-top tabular-nums text-gray-700"
								>$2,000.00</td
							>
						</tr>
						<tr class="border-b border-gray-100">
							<td class="max-w-0 px-0 py-5 align-top">
								<div class="truncate font-medium text-gray-900">Website redesign</div>
								<div class="truncate text-gray-500">Design and program new company website.</div>
							</td>
							<td
								class="hidden py-5 pl-8 pr-0 text-right align-top tabular-nums text-gray-700 sm:table-cell"
								>52.0</td
							>
							<td
								class="hidden py-5 pl-8 pr-0 text-right align-top tabular-nums text-gray-700 sm:table-cell"
								>$100.00</td
							>
							<td class="py-5 pl-8 pr-0 text-right align-top tabular-nums text-gray-700"
								>$5,200.00</td
							>
						</tr>
						<tr class="border-b border-gray-100">
							<td class="max-w-0 px-0 py-5 align-top">
								<div class="truncate font-medium text-gray-900">Business cards</div>
								<div class="truncate text-gray-500">
									Design and production of 3.5&quot; x 2.0&quot; business cards.
								</div>
							</td>
							<td
								class="hidden py-5 pl-8 pr-0 text-right align-top tabular-nums text-gray-700 sm:table-cell"
								>12.0</td
							>
							<td
								class="hidden py-5 pl-8 pr-0 text-right align-top tabular-nums text-gray-700 sm:table-cell"
								>$100.00</td
							>
							<td class="py-5 pl-8 pr-0 text-right align-top tabular-nums text-gray-700"
								>$1,200.00</td
							>
						</tr>
						<tr class="border-b border-gray-100">
							<td class="max-w-0 px-0 py-5 align-top">
								<div class="truncate font-medium text-gray-900">T-shirt design</div>
								<div class="truncate text-gray-500">Three t-shirt design concepts.</div>
							</td>
							<td
								class="hidden py-5 pl-8 pr-0 text-right align-top tabular-nums text-gray-700 sm:table-cell"
								>4.0</td
							>
							<td
								class="hidden py-5 pl-8 pr-0 text-right align-top tabular-nums text-gray-700 sm:table-cell"
								>$100.00</td
							>
							<td class="py-5 pl-8 pr-0 text-right align-top tabular-nums text-gray-700">$400.00</td
							>
						</tr>
					</tbody>
					<tfoot>
						<tr>
							<th scope="row" class="px-0 pb-0 pt-6 font-normal text-gray-700 sm:hidden"
								>Subtotal</th
							>
							<th
								scope="row"
								colspan="3"
								class="hidden px-0 pb-0 pt-6 text-right font-normal text-gray-700 sm:table-cell"
								>Subtotal</th
							>
							<td class="pb-0 pl-8 pr-0 pt-6 text-right tabular-nums text-gray-900">$8,800.00</td>
						</tr>
						<tr>
							<th scope="row" class="pt-4 font-normal text-gray-700 sm:hidden">Tax</th>
							<th
								scope="row"
								colspan="3"
								class="hidden pt-4 text-right font-normal text-gray-700 sm:table-cell">Tax</th
							>
							<td class="pb-0 pl-8 pr-0 pt-4 text-right tabular-nums text-gray-900">$1,760.00</td>
						</tr>
						<tr>
							<th scope="row" class="pt-4 font-semibold text-gray-900 sm:hidden">Total</th>
							<th
								scope="row"
								colspan="3"
								class="hidden pt-4 text-right font-semibold text-gray-900 sm:table-cell">Total</th
							>
							<td class="pb-0 pl-8 pr-0 pt-4 text-right font-semibold tabular-nums text-gray-900"
								>$10,560.00</td
							>
						</tr>
					</tfoot>
				</table>
			</div>

			<div class="lg:col-start-3">
				<!-- Activity feed -->
				<h2 class="text-sm font-semibold leading-6 text-gray-900">Activity</h2>
				<ul role="list" class="mt-6 space-y-6">
					<li class="relative flex gap-x-4">
						<div class="absolute left-0 top-0 flex w-6 justify-center -bottom-6">
							<div class="w-px bg-gray-200" />
						</div>
						<div class="relative flex h-6 w-6 flex-none items-center justify-center bg-white">
							<div class="h-1.5 w-1.5 rounded-full bg-gray-100 ring-1 ring-gray-300" />
						</div>
						<p class="flex-auto py-0.5 text-xs leading-5 text-gray-500">
							<span class="font-medium text-gray-900">Chelsea Hagon</span> created the invoice.
						</p>
						<time
							datetime="2023-01-23T10:32"
							class="flex-none py-0.5 text-xs leading-5 text-gray-500">7d ago</time
						>
					</li>
					<li class="relative flex gap-x-4">
						<div class="absolute left-0 top-0 flex w-6 justify-center -bottom-6">
							<div class="w-px bg-gray-200" />
						</div>
						<div class="relative flex h-6 w-6 flex-none items-center justify-center bg-white">
							<div class="h-1.5 w-1.5 rounded-full bg-gray-100 ring-1 ring-gray-300" />
						</div>
						<p class="flex-auto py-0.5 text-xs leading-5 text-gray-500">
							<span class="font-medium text-gray-900">Chelsea Hagon</span> edited the invoice.
						</p>
						<time
							datetime="2023-01-23T11:03"
							class="flex-none py-0.5 text-xs leading-5 text-gray-500">6d ago</time
						>
					</li>
					<li class="relative flex gap-x-4">
						<div class="absolute left-0 top-0 flex w-6 justify-center -bottom-6">
							<div class="w-px bg-gray-200" />
						</div>
						<div class="relative flex h-6 w-6 flex-none items-center justify-center bg-white">
							<div class="h-1.5 w-1.5 rounded-full bg-gray-100 ring-1 ring-gray-300" />
						</div>
						<p class="flex-auto py-0.5 text-xs leading-5 text-gray-500">
							<span class="font-medium text-gray-900">Chelsea Hagon</span> sent the invoice.
						</p>
						<time
							datetime="2023-01-23T11:24"
							class="flex-none py-0.5 text-xs leading-5 text-gray-500">6d ago</time
						>
					</li>
					<li class="relative flex gap-x-4">
						<div class="absolute left-0 top-0 flex w-6 justify-center -bottom-6">
							<div class="w-px bg-gray-200" />
						</div>
						<img
							src="https://images.unsplash.com/photo-1550525811-e5869dd03032?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
							alt=""
							class="relative mt-3 h-6 w-6 flex-none rounded-full bg-gray-50"
						/>
						<div class="flex-auto rounded-md p-3 ring-1 ring-inset ring-gray-200">
							<div class="flex justify-between gap-x-4">
								<div class="py-0.5 text-xs leading-5 text-gray-500">
									<span class="font-medium text-gray-900">Chelsea Hagon</span> commented
								</div>
								<time
									datetime="2023-01-23T15:56"
									class="flex-none py-0.5 text-xs leading-5 text-gray-500">3d ago</time
								>
							</div>
							<p class="text-sm leading-6 text-gray-500">
								Called client, they reassured me the invoice would be paid by the 25th.
							</p>
						</div>
					</li>
					<li class="relative flex gap-x-4">
						<div class="absolute left-0 top-0 flex w-6 justify-center -bottom-6">
							<div class="w-px bg-gray-200" />
						</div>
						<div class="relative flex h-6 w-6 flex-none items-center justify-center bg-white">
							<div class="h-1.5 w-1.5 rounded-full bg-gray-100 ring-1 ring-gray-300" />
						</div>
						<p class="flex-auto py-0.5 text-xs leading-5 text-gray-500">
							<span class="font-medium text-gray-900">Alex Curren</span> viewed the invoice.
						</p>
						<time
							datetime="2023-01-24T09:12"
							class="flex-none py-0.5 text-xs leading-5 text-gray-500">2d ago</time
						>
					</li>
					<li class="relative flex gap-x-4">
						<div class="absolute left-0 top-0 flex w-6 justify-center h-6">
							<div class="w-px bg-gray-200" />
						</div>
						<div class="relative flex h-6 w-6 flex-none items-center justify-center bg-white">
							<svg
								class="h-6 w-6 text-indigo-600"
								viewBox="0 0 24 24"
								fill="currentColor"
								aria-hidden="true"
							>
								<path
									fill-rule="evenodd"
									d="M2.25 12c0-5.385 4.365-9.75 9.75-9.75s9.75 4.365 9.75 9.75-4.365 9.75-9.75 9.75S2.25 17.385 2.25 12zm13.36-1.814a.75.75 0 10-1.22-.872l-3.236 4.53L9.53 12.22a.75.75 0 00-1.06 1.06l2.25 2.25a.75.75 0 001.14-.094l3.75-5.25z"
									clip-rule="evenodd"
								/>
							</svg>
						</div>
						<p class="flex-auto py-0.5 text-xs leading-5 text-gray-500">
							<span class="font-medium text-gray-900">Alex Curren</span> paid the invoice.
						</p>
						<time
							datetime="2023-01-24T09:20"
							class="flex-none py-0.5 text-xs leading-5 text-gray-500">1d ago</time
						>
					</li>
				</ul>
			</div>
		</div>
	</div>
</main>
