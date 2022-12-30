<script>
	import { page } from '$app/stores';
	$: isActive = $page.url.pathname === $$props.href;
	export let href;
</script>

<a
	class="hidden rounded-lg p-1 text-gray-800 transition-all hover:bg-slate-400 hover:text-white dark:text-gray-200 dark:hover:bg-indigo-400 sm:px-3 sm:py-2 md:inline-block"
	class:font-semibold={isActive}
	{href}
	><span class="capsize"><slot /> </span>
</a>
