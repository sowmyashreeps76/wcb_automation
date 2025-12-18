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
