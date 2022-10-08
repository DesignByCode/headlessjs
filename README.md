# Vanilla Headless
[![npm version](https://badge.fury.io/js/vanilla-headless.svg)](https://badge.fury.io/js/vanilla-headless)
![npm](https://img.shields.io/npm/dt/vanilla-headless)
[![GitHub stars](https://img.shields.io/github/stars/DesignByCode/vanilla-headless?style=social)](https://github.com/DesignByCode/vanilla-headless/stargazers)


[![NPM](https://nodei.co/npm/vanilla-headless.png)](https://nodei.co/npm/vanilla-headless/)

![](./img/git-banner.jpg)

- [Install](#install)
- [Import](#import)
- [Web Components](#web-components)
  - [Popover](#popover-with-aria-keyboard-navigation)
  - [Dropdown Menu](#dropdown-with-aria-keyboard-navigation)
  - [Disclosure](#disclosure-with-aria-keyboard-navigation)
  - [Mobile Navigation]()
- [Use with PopperJs](#popperjs)

### Install

```bash
npm i vanilla-headless
```
```bash
yarn add vanilla-headless
```

```bash
yarn add vanilla-headless
```

### Import

```typescript
import "vanilla-headless"
```
<blockquote style="background-color: #2dd4bf; color: #134e4a; border-left-color: #134e4a; border-left-width: 5px; 
border-radius: 3px;">
<small style="font-size: 12px; font-style: italic">
That's all, no other javascript required. Just wrap you aria compliant markup with the appropriate tag.
</small>
</blockquote>  




## Web Components

- [popover](#popover-with-aria-keyboard-navigation)
- [dropdown menu](#dropdown-with-aria-keyboard-navigation)
- [disclosure](#disclosure-with-aria-keyboard-navigation)

### Popover with aria keyboard navigation

#### Requirements:

- Button:
  - must be typeof ``button``
  - must have attributes of ``aria-haspopup`` and ``aria-expanded``
  - ``ID`` must have same value as dropdown labelledby
- Dropdown
  - must have attributes of ``aria-labelledby``

![](./img/popover.gif)

```html
<!-- require tailwindcss for example -->
<headless-popover class="relative" offsets="0 10" placement="bottom-end bottom" popper>
  <button
    aria-expanded="true"
    aria-haspopup="true"
    class="inline-flex justify-center w-full rounded-md border border-gray-300 shadow-sm px-4 py-2 bg-white text-sm font-medium text-gray-700 hover:bg-gray-50 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-offset-gray-100 focus:ring-sky-500"
    id="popover"
    type="button"
  >
    Popover
    <!-- Heroicon name: solid/chevron-down -->
    <svg aria-hidden="true" class="-mr-1 ml-2 h-5 w-5" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
      <path clip-rule="evenodd" d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z" fill-rule="evenodd" />
    </svg>
  </button>
  <div aria-labelledby="popover" class="absolute z-10 w-screen max-w-sm  transform px-4 sm:px-0">
    <div class="overflow-hidden rounded-lg shadow-lg ring-1 ring-black ring-opacity-5">
      <div class="relative grid gap-8 bg-white p-7">
        <a
          class="-m-3 flex items-center rounded-lg p-2 transition duration-150 ease-in-out hover:bg-gray-50 focus:outline-none focus-visible:ring focus-visible:ring-sky-500 focus-visible:ring-opacity-50"
          href="#"
        >
          <span>
            <svg aria-hidden="true" fill="none" height="48" viewBox="0 0 48 48" width="48" xmlns="http://www.w3.org/2000/svg">
              <rect fill="#e0f2fe" height="48" rx="8" width="48"></rect>
              <path d="M24 11L35.2583 17.5V30.5L24 37L12.7417 30.5V17.5L24 11Z" stroke="#0ea5e9" stroke-width="2"></path>
              <path
                clip-rule="evenodd"
                d="M16.7417 19.8094V28.1906L24 32.3812L31.2584 28.1906V19.8094L24 15.6188L16.7417 19.8094Z"
                fill-rule="evenodd"
                stroke="#0284c7"
                stroke-width="2"
              ></path>
              <path
                clip-rule="evenodd"
                d="M20.7417 22.1196V25.882L24 27.7632L27.2584 25.882V22.1196L24 20.2384L20.7417 22.1196Z"
                fill-rule="evenodd"
                stroke="#0284c7"
                stroke-width="2"
              ></path>
            </svg>
          </span>
          <span class="ml-2"> Lorem ipsum dolor sit amet, consectetur. </span>
        </a>
        <a
          class="-m-3 flex items-center rounded-lg p-2 transition duration-150 ease-in-out hover:bg-gray-50 focus:outline-none focus-visible:ring focus-visible:ring-sky-500 focus-visible:ring-opacity-50"
          href="#"
        >
          <span>
            <svg aria-hidden="true" fill="none" height="48" viewBox="0 0 48 48" width="48" xmlns="http://www.w3.org/2000/svg">
              <rect fill="#e0f2fe" height="48" rx="8" width="48"></rect>
              <path d="M24 11L35.2583 17.5V30.5L24 37L12.7417 30.5V17.5L24 11Z" stroke="#0ea5e9" stroke-width="2"></path>
              <path
                clip-rule="evenodd"
                d="M16.7417 19.8094V28.1906L24 32.3812L31.2584 28.1906V19.8094L24 15.6188L16.7417 19.8094Z"
                fill-rule="evenodd"
                stroke="#0284c7"
                stroke-width="2"
              ></path>
              <path
                clip-rule="evenodd"
                d="M20.7417 22.1196V25.882L24 27.7632L27.2584 25.882V22.1196L24 20.2384L20.7417 22.1196Z"
                fill-rule="evenodd"
                stroke="#0284c7"
                stroke-width="2"
              ></path>
            </svg>
          </span>
          <span class="ml-2"> Lorem ipsum dolor sit amet, consectetur. </span>
        </a>
        <a
          class="-m-3 flex items-center rounded-lg p-2 transition duration-150 ease-in-out hover:bg-gray-50 focus:outline-none focus-visible:ring focus-visible:ring-sky-500 focus-visible:ring-opacity-50"
          href="#"
        >
          <span>
            <svg aria-hidden="true" fill="none" height="48" viewBox="0 0 48 48" width="48" xmlns="http://www.w3.org/2000/svg">
              <rect fill="#e0f2fe" height="48" rx="8" width="48"></rect>
              <path d="M24 11L35.2583 17.5V30.5L24 37L12.7417 30.5V17.5L24 11Z" stroke="#0ea5e9" stroke-width="2"></path>
              <path
                clip-rule="evenodd"
                d="M16.7417 19.8094V28.1906L24 32.3812L31.2584 28.1906V19.8094L24 15.6188L16.7417 19.8094Z"
                fill-rule="evenodd"
                stroke="#0284c7"
                stroke-width="2"
              ></path>
              <path
                clip-rule="evenodd"
                d="M20.7417 22.1196V25.882L24 27.7632L27.2584 25.882V22.1196L24 20.2384L20.7417 22.1196Z"
                fill-rule="evenodd"
                stroke="#0284c7"
                stroke-width="2"
              ></path>
            </svg>
          </span>
          <span class="ml-2"> Lorem ipsum dolor sit amet, consectetur. </span>
        </a>
      </div>
    </div>
  </div>
</headless-popover>
```

### Dropdown with aria keyboard navigation

#### Requirements:

- Button:
  - must be typeof ``button``
  - must have attributes of ``aria-haspopup`` and ``aria-expanded``
  - ``ID`` must have same value as dropdown ``labelledby``
- Dropdown
  - must have attributes of ``aria-labelledby``
  - dropdown require at least 1 anchor or button tag with attribute `role="menuitem"`

![](./img/dropdown.gif)

```html
<!-- require tailwindcss for example -->
<headless-dropdown class="relative inline-block text-left" placement="bottom-end bottom" popper>
  <div>
    <button
      aria-expanded="true"
      aria-haspopup="true"
      class="inline-flex justify-center w-full rounded-md border border-gray-300 shadow-sm px-4 py-2 bg-white text-sm font-medium text-gray-700 hover:bg-gray-50 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-offset-gray-100 focus:ring-indigo-500"
      id="menu-button"
      type="button"
    >
      Dropdown
      <!-- Heroicon name: solid/chevron-down -->
      <svg aria-hidden="true" class="-mr-1 ml-2 h-5 w-5" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
        <path clip-rule="evenodd" d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z" fill-rule="evenodd" />
      </svg>
    </button>
  </div>

  <div
    aria-labelledby="menu-button"
    aria-orientation="vertical"
    class="origin-top-right absolute w-56 rounded-md shadow-lg bg-white ring-1 ring-black ring-opacity-5 focus:outline-none"
    role="menu"
    tabindex="-1"
  >
    <div class="py-1" role="none">
      <a class="text-gray-700 block px-4 py-2 text-sm hover:bg-gray-100 focus:bg-gray-100 focus:outline-none" href="#account" id="menu-item-0" role="menuitem" tabindex="-1"
        >Account settings</a
      >
      <a class="text-gray-700 block px-4 py-2 text-sm hover:bg-gray-100 focus:bg-gray-100 focus:outline-none" href="#support" id="menu-item-1" role="menuitem" tabindex="-1"
        >Support</a
      >
      <a class="text-gray-700 block px-4 py-2 text-sm hover:bg-gray-100 focus:bg-gray-100 focus:outline-none" href="#license" id="menu-item-2" role="menuitem" tabindex="-1"
        >License</a
      >
      <form action="#test" method="POST" role="none">
        <button
          class="text-gray-700 block w-full text-left px-4 py-2 text-sm hover:bg-gray-100 focus:bg-gray-100 focus:outline-none"
          id="menu-item-3"
          role="menuitem"
          tabindex="-1"
          type="submit"
        >
          Sign out
        </button>
      </form>
    </div>
  </div>
</headless-dropdown>
```

### Disclosure with aria keyboard navigation

#### Requirements:

- Button:
  - must be typeof ``button``
  - must have attributes of `aria-controls` and `aria-expanded`
- Dropdown
  - must have a `ID` matching `aria-controls`

![](./img/discosure.gif)

```html
<!-- require tailwindcss for example -->
<headless-disclosure class="mx-auto w-full max-w-md rounded-md bg-white p-2">
  <dl class="faq">
    <dt>
      <button
        aria-controls="faq1_desc"
        aria-expanded="true"
        class="flex w-full rounded-md bg-blue-100 px-4 py-2 text-left text-sm font-medium text-blue-900 hover:bg-blue-200 focus:outline-none focus-visible:ring focus-visible:ring-blue-500 focus-visible:ring-opacity-75 mb-2"
        type="button"
      >
        What do I do if I have a permit for an assigned lot, but can't find a space there?
      </button>
    </dt>
    <dd>
      <div class="px-4 pt-4 pb-2 text-sm text-gray-500" id="faq1_desc">
        Park at the nearest available parking meter without paying the meter and call 999-999-9999 to report the problem. We will note and approve your alternate location and will
        investigate the cause of the shortage in your assigned facility.
      </div>
    </dd>
    <dt>
      <button
        aria-controls="faq2_desc"
        aria-expanded="false"
        class="flex w-full rounded-md bg-blue-100 px-4 py-2 text-left text-sm font-medium text-blue-900 hover:bg-blue-200 focus:outline-none focus-visible:ring focus-visible:ring-blue-500 focus-visible:ring-opacity-75 mb-2"
        type="button"
      >
        What do I do if I lose my permit or if my permit is stolen?
      </button>
    </dt>
    <dd>
      <div class="px-4 pt-4 pb-2 text-sm text-gray-500" id="faq2_desc">
        You should come to the Parking office and report the loss. There is a fee to replace your lost permit. However, if your permit was stolen, a copy of a police report needs
        to be submitted along with a stolen parking permit form for a fee replacement exemption.
      </div>
    </dd>
    <dt>
      <button
        aria-controls="faq3_desc"
        aria-expanded="false"
        class="flex w-full rounded-md bg-blue-100 px-4 py-2 text-left text-sm font-medium text-blue-900 hover:bg-blue-200 focus:outline-none focus-visible:ring focus-visible:ring-blue-500 focus-visible:ring-opacity-75 mb-2"
        type="button"
      >
        Is there free parking on holidays?
      </button>
    </dt>
    <dd>
      <div class="px-4 pt-4 pb-2 text-sm text-gray-500" id="faq3_desc">
        All facilities are restricted from 2:00 am - 6:00 am on all days. No exceptions are made for any holiday or recess except those officially listed as a
        <q> Holidays </q>
        in the calendar. Please note: 24-hour rental spaces, 24-hour rental lots, and disabled parking is enforced at all times.
      </div>
    </dd>
    <dt>
      <button
        aria-controls="faq4_desc"
        aria-expanded="false"
        class="flex w-full rounded-md bg-blue-100 px-4 py-2 text-left text-sm font-medium text-blue-900 hover:bg-blue-200 focus:outline-none focus-visible:ring focus-visible:ring-blue-500 focus-visible:ring-opacity-75 mb-2"
        type="button"
      >
        Do all parking facilities have the same enforcement rules?
      </button>
    </dt>
    <dd>
      <div class="px-4 pt-4 pb-2 text-sm text-gray-500" id="faq4_desc">
        Some parking facility restrictions differ from others. Be sure to take note of the signs at each lot entrance.
      </div>
    </dd>
  </dl>
</headless-disclosure>
```

### PopperJs

PopperJs is already bundle in and only require a attribute of `popper` to work.

#### Optional

- Popper.js
  - <u>**Required:**</u> Add attribute of `popper` or `popper="true"` to enable popper.js
  - Change placement with attribute `placement="bottom-end bottom-start"`
  - Change offset with attribute `offset="0 20"`

#### Use with PopperJs

<small><i>Attribute can be seperated by comma or empty space</i></small>

```html

<headless-dropdown popper placement="bottom-end bottom-start" ....
<headless-dropdown popper="true" placement="bottom-end,bottom-start" ....
<headless-dropdown popper offset="0 20" ....
<headless-dropdown popper="true" offset="0,20" ....
```
