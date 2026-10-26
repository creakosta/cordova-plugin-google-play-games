# Change Log
All notable changes to this project will be documented in this file.

# Unreleased

#### Added
* `login()` now falls back to the manual Play Games sign-in dialog (`GamesSignInClient.signIn()`) when automatic sign-in fails.
* `login({ silent: true })` only checks automatic sign-in and never shows the dialog.

#### Fixed
* Crash `RuntimeExecutionException` in `login()`: `getCurrentPlayer()` result was read without checking `Task#isSuccessful()`. The error is now returned to JS.
* `loadGameSave()`: task results are checked before `getResult()`, no NPE on missing snapshot data; failures are reported to JS.

#### Removed
* Legacy support libraries `com.android.support:support-v4` and `recyclerview-v7` (not used; conflict with AndroidX).

# Version 1.0.0

#### Added
* Added achievements, leaderboards and game savings. Initial commit.
