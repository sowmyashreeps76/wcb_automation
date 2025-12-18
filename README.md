// wait until Finish button appears
await finishBtn().waitFor({
  state: 'visible',
  timeout: 20000,
});

// ensure enabled
await expect(finishBtn()).toBeEnabled({ timeout: 20000 });

// scroll if needed
await finishBtn().scrollIntoViewIfNeeded();

// click
await finishBtn().click({ timeout: 20000 });

// optional wait for next page / loader
await page.waitForLoadState('networkidle');





// wait until Finish button is visible in DOM
await finishBtn().waitFor({
  state: 'visible',
  timeout: 20000,
});

// wait until enabled (your existing util)
await expectElementToBeEnabled(finishBtn(), { timeout: 20000 });

// scroll into view (important for hidden buttons)
await finishBtn().scrollIntoViewIfNeeded();

// click Finish
await finishBtn().click({ timeout: 20000 });

// keep your wait (optional)
await wait(5000);
