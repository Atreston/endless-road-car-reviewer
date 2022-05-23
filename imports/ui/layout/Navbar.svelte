<script>
  import Dropdown from './Dropdown.svelte';
</script>

<nav class="flex flex-col md:flex-row items-center md:justify-between md:h-18 max-w-screen-2xl mx-auto px-6 py-4 border-b border-b-gray-60 bg-white dark:bg-black dark:text-white  shadow-sm">
  <!-- Logo -->
  <div>
    <h2 class="text-3xl font-bold">
      <a>Test <span class="text-red-600">D</span>rive</a>
    </h2>
  </div>
  <!-- /End Logo -->
  <div class="mt-5 md:mt-0">
    <ul class="flex flex-col md:flex-row md:space-x-5 w-full items-center">
      <li>
        <a href="https://google.com" class="font-semibold tracking-tight block cursor-pointer p-2 hover:text-blue-500 transition-colors duration-300">Products</a>
      </li>
      <li>
        <a href="https://google.com" class="font-semibold tracking-tight block cursor-pointer p-2 hover:text-blue-500 transition-colors duration-300">Company</a>
      </li>
      <li>
        <a href="https://google.com" class="font-semibold tracking-tight block cursor-pointer p-2 hover:text-blue-500 transition-colors duration-300">Partners</a>
      </li>
      <li>
        <a href="https://google.com" class="font-semibold tracking-tight block cursor-pointer p-2 hover:text-blue-500 transition-colors duration-300">News</a>
      </li>
      <li>
        <a href="https://google.com" class="font-semibold tracking-tight block cursor-pointer p-2 hover:text-blue-500 transition-colors duration-300">Contact Us</a>
      </li>
      <li>
        <Dropdown/>
      </li>
    </ul>
  </div>
</nav>

