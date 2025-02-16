# Перегляд запитів на отримання

Цей документ описує процес перевірки змін вмісту у веб-документах MDN і призначений для використання тими, кому доручено переглядати PR вмісту MDN.

## Процес перевірки змін вмісту

Зміни вмісту, які ми отримуємо на MDN, стосуються, наприклад, різноманітних робочих потоків:

- Повсякденна робота над покращенням вмісту — нові API, нові властивості CSS та інші важливі оновлення платформи та доповнення вмісту, як правило, виконується персоналом MDN, який працює на Mozilla, Google, Open Web Docs, Samsung тощо,
   але також іноді волонтерами громади.
- «Виправлення» — невеликі оновлення сайту для виправлення помилок, граматичних проблем і технічних неточностей, як правило, коли їх знаходять користувачі MDN.
— Виправлення помилок у вмісті MDN, які зазвичай виконуються волонтерами для вирішення проблем у цьому репозиторі\.

Незалежно від способу зміни вмісту, вони будуть подані як
[pull requests](https://github.com/mdn/content/pulls) on this repo, which will
вимагають швидкого перегляду та об’єднання, щоб переконатися, що сайт не застарів. Це обробляється наступним чином:

1. Різні співробітники та волонтери MDN були призначені як «власники тематичного
   огляду", що означає, що коли надходить запит на отримання, пов’язаний з 
   певна тематична область сайту (наприклад, посилання на CSS або навчання),
   його буде призначено власникам(ам) огляду теми цієї області та вони
   отримають сповіщення електронною поштою з проханням переглянути. Це буде
   оброблятися за допомогою [CODEOWNERS](https://github.com/mdn/content/blob/main/.github/CODEOWNERS)
   файл, у якому певні каталоги вмісту призначено темам на ім'я користувача GitHub власника огляду.
2. Once the review has been done and the pull request has been approved, the
   reviewer should also merge the pull request.
3. The site will be rebuilt once every 24 hours to ensure that the content
   does not get too stale.

## Рекомендації з огляду 

If you are reviewing MDN content changes, read through the following
guidelines. There's quite a lot here, but don't worry if you don't review
perfectly in accordance with all of these points immediately. It is more
important to make sure the content is readable, useful, correct, and not
inappropriate, than it is to follow every guideline to the letter.

1. Familiarize yourself with the [MDN Code example guidelines][]
   and make sure that code examples follow the guidelines. You'll get used to
   them eventually, and we are intending to automatically lint against our
   guidelines at some point in the future.
2. Familiarize yourself with the [MDN Writing style guide][],
   and use it to inform your reviews of new text content.
3. Familiarize yourself with the MDN [pull request guidelines](https://github.com/mdn/content/blob/main/README.md#pull-request-etiquette).
   The key points here are
   - You have the right to request more information to help your review if the
     submitter has not explained why they are making this change.
   - You have the right to close a pull request if it is too complex and/or
     contains multiple unrelated changes and ask the submitter to submit their
     changes in smaller atomic chunks.
4. When reviewing a pull request, use the [GitHub review tools](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/reviewing-changes-in-pull-requests/about-pull-request-reviews).
   Use "Request changes" when submitting a review that will require the
   submitter to do some more work, or "Approve" if the submission is ready to
   add and you want to merge it. [Reviewing proposed changes in a pull request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/reviewing-changes-in-pull-requests/reviewing-proposed-changes-in-a-pull-request)
   is also useful if you want more information.
5. Be polite and constructive at all times when writing review comments, or
   otherwise interacting with the submitter and other community members. We are
   all bound by [our Code of Conduct](CODE_OF_CONDUCT.md) when contributing to
   MDN, which means adhering to Mozilla's [Community Participation Guidelines](https://www.mozilla.org/en-US/about/governance/policies/participation/).
   If anyone has engaged in behavior that is potentially illegal or makes
   you or someone else feel unsafe, unwelcome, or uncomfortable, you are
   encouraged to [report it](https://www.mozilla.org/en-US/about/governance/policies/participation/reporting/).
   We want MDN to be a welcoming, friendly community that we can all be
   proud of.
6. If a pull request is fine apart from a small typo or some other minor
   issue, you might want to just fix the issue yourself rather than ask the
   submitter to change it. You can do this provided the PR has been set up
   to allow changes (see [Allowing changes to a pull request branch created from a fork](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/allowing-changes-to-a-pull-request-branch-created-from-a-fork)
   for more details). If you are not sure how to make changes to someone
   else's pull request, [@vkWeb](https://github.com/vkWeb/) wrote some nice
   simple instructions on how to do this on the command line; see
   [ReviewPRCommands](https://gist.github.com/vkWeb/dcec82b079f1edc19478ddb58b0ffc5e).
   - Alternatively, you can edit files using the GitHub UI — go to the pull
     request's "Files changed" tab, find the file you want to edit, and
     choose "three dot" menu (...) > Edit file.
7. If a pull request is fine in itself, is a clear improvement to the content,
   and makes the change it claims to make in the description, you should as a
   rule merge it, even if you can see other improvements that could be made in
   the same file. If you want to ensure that these other improvements will
   be taken care of, file a follow-up issue or pull request of your own to
   address them.
8. If you don't understand a content change that you've been selected to
   review, or feel that it is too large and complex for you to deal with,
   don't panic! Feel free to reach out to someone else to ask for help,
   like a colleague, or someone else in your group of topic review owners
   (if you know who they are). If you are not sure who to approach for help,
   then ping our `@core-yari-content` group to ask for help.
9. Related to the above point, it is rare that you'll be required to review
   a large, complex content change with no warning, like a complete page
   rewrite, or the addition of several new reference pages or tutorials.
   Usually such changes are done as part of specific work streams where
   the content has been approved for addition, and reviewer(s) have been
   assigned already. In such cases, the PR should be linked to an issue
   that explains all these details. If you are not sure, ask the submitter
   if they need a review of the content, and where the rationale behind the
   change is explained. Ping our team in the [MDN Web Docs chat rooms][] to ask for help if you are still not sure, or
   if you think the content is suspicious.

Note: You may encounter merge conflicts as you review pull requests, if another
pull request that touches some of the same files got merged before
the one you are reviewing.
[Addressing merge conflicts](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/addressing-merge-conflicts)
is a useful resource to help you. Feel free also to ask your team(s) for help
if you need it.

## Спеціальний рецензент замінює запити на отримання

Some of the pull requests submitted on the `content` repo relate to specific
workstreams being undertaken by browser vendors or other organizations that
have a defined set of writers and reviewers. In these cases, the submitter
of the PR will include the username of the reviewer in a line at the bottom
of the pull request description, for example:

`reviewer: @jpmedley`

Upon submitting the pull request, they will request a review from the reviewer
specified in the pull request description. Once that reviewer has approved
the new content, they will then ask you for an approval as required by the
CODEOWNERS system for the pull request to be mergeable.

Therefore, if you receive a pull request review request and then see that
you have been overridden with another reviewer in the manner described above,
then don't review the pull request — just wait for an approval request.

## Власники огляду теми

Наступні конкретні тематичні області розглядаються добрими душами, перерахованими під ними.
BБудьте добрі до них і подякуйте їм за всю допомогу, яку вони надають цьому проекту.
Якщо ви хочете допомогти з переглядом вмісту MDN, [get in touch with us][].

Зауважте, що зміни в будь-яких областях вмісту, які явно не перелічені нижче, будуть оброблені
[@core-yari-content](https://github.com/orgs/mdn/teams/core-yari-content)
команда, яка нині складається з [@Rumyra](https://github.com/Rumyra/).

- [Web accessibility content](https://github.com/mdn/content/tree/main/files/en-us/web/accessibility):
  - [@ericwbailey](https://github.com/ericwbailey)
- [General learning content](https://github.com/mdn/content/tree/main/files/en-us/learn):
  - [@chrisdavidmills](https://github.com/chrisdavidmills/)
- [CSS learning content](https://github.com/mdn/content/tree/main/files/en-us/learn/css):
  - [@rachelandrew](https://github.com/rachelandrew)
- [Server-side learning content](https://github.com/mdn/content/tree/main/files/en-us/learn/server-side):
  - [@hamishwillee](https://github.com/hamishwillee)
- [MDN meta docs](https://github.com/mdn/content/tree/main/files/en-us/mdn)
  — [@yari-content-mdn](https://github.com/orgs/mdn/teams/yari-content-mdn)
  команда, яка складається:
  - [@Rumyra](https://github.com/Rumyra/)
  - [@Elchi3](https://github.com/Elchi3)
- [Firefox Developer Tools content](https://github.com/mdn/content/tree/main/files/en-us/tools):
  - [@hamishwillee](https://github.com/hamishwillee)
- [Mozilla Add-ons reference content](https://github.com/mdn/content/tree/main/files/en-us/mozilla/add-ons)
  — [@yari-content-mozilla-add-ons](https://github.com/orgs/mdn/teams/yari-content-mozilla-add-ons)
  команда, яка складається:
  - [@caitmuenster](https://github.com/caitmuenster)
  - [@rpl](https://github.com/rpl)
  - [@Rob--W](https://github.com/Rob--W)
  - [@zombie](https://github.com/zombie)
  - [@mixedpuppy](https://github.com/mixedpuppy)
- [HTTP reference content](https://github.com/mdn/content/tree/main/files/en-us/web/http)
  — [@yari-content-http](https://github.com/orgs/mdn/teams/yari-content-http)
  команда, яка складається :
  - [@hamishwillee](https://github.com/hamishwillee)
  - [@Elchi3](https://github.com/Elchi3)
  - [@mirunacurtean](https://github.com/mirunacurtean)
- [CSS reference content](https://github.com/mdn/content/tree/main/files/en-us/web/css)
  — [@yari-content-css](https://github.com/orgs/mdn/teams/yari-content-css)
  команда, яка складається f:
  - [@rachelandrew](https://github.com/rachelandrew)
  - [@ericwbailey](https://github.com/ericwbailey)
  - [@mirunacurtean](https://github.com/mirunacurtean)
- [HTML reference content](https://github.com/mdn/content/tree/main/files/en-us/web/html)
  — the [@yari-content-html](https://github.com/orgs/mdn/teams/yari-content-html)
  команда, яка складається :
  - [@rachelandrew](https://github.com/rachelandrew)
  - [@ericwbailey](https://github.com/ericwbailey)
  - [@mirunacurtean](https://github.com/mirunacurtean)
- [JavaScript reference content](https://github.com/mdn/content/tree/main/files/en-us/web/javascript)
  — [@yari-content-javascript](https://github.com/orgs/mdn/teams/yari-content-javascript)
  команда, яка складається :
  - [@Rumyra](https://github.com/Rumyra)
  - [@sideshowbarker](https://github.com/sideshowbarker)
  - [@Elchi3](https://github.com/Elchi3)
- [Web API reference content](https://github.com/mdn/content/tree/main/files/en-us/web/api)
  — [@yari-content-web-api](https://github.com/orgs/mdn/teams/yari-content-web-api)
  команда, яка складається :
  - [@Rumyra](https://github.com/Rumyra)
  - [@sideshowbarker](https://github.com/sideshowbarker)
  - [@Elchi3](https://github.com/Elchi3)
  - [@jpmedley](https://github.com/jpmedley)
- [SVG reference content](https://github.com/mdn/content/tree/main/files/en-us/web/svg)
  — [@yari-content-svg](https://github.com/orgs/mdn/teams/yari-content-svg)
  команда, яка складається з:
  - [@Ryuno-Ki](https://github.com/Ryuno-Ki)

### Рецензент випускників

Наступні люди раніше були в одній або кількох наших групах перевірки, але більше не мають часу робити внески; ми хочемо висловити їм нашу щиру подяку за всю їхню допомогу.

- [@vkWeb](https://github.com/vkWeb/)

[get in touch with us]: https://developer.mozilla.org/en-US/docs/MDN/Community/Contributing/Getting_started#what_can_i_do_to_help
[mdn code example guidelines]: https://developer.mozilla.org/en-US/docs/MDN/Writing_guidelines/Writing_style_guide/Code_style_guide
[mdn writing style guide]: https://developer.mozilla.org/en-US/docs/MDN/Guidelines/Writing_style_guide
[MDN Web Docs chat rooms]: https://developer.mozilla.org/en-US/docs/MDN/Community/Communication_channels
