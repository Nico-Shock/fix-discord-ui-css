```
@import url("https://scattagain.github.io/VencordStuff/css/GuildbarRevert.css");
@import url('https://raw.githubusercontent.com/surgedevs/visual-refresh-compact-title-bar/refs/heads/main/desktop.css');

:root {
    /* Only include this part if you wish to change these variables */
    /* You can change the size but only to be less than 48px, you must change the blob scale too */
    --guildbar-avatar-size: 42px;
    --blob-scale: 42;

    --guildbar-folder-size: var(--guildbar-avatar-size);
    --folder-blob-scale: var(--blob-scale);
}

.visual-refresh section[aria-label="User area"] {
    width: calc(var(--custom-guild-sidebar-width) - var(--custom-guild-list-width) + 1px);;
    left: var(--custom-guild-list-width);
    bottom: 0px;
    border-radius: 0px;
    border: none;
}

.visual-refresh nav:has([data-list-id="guildsnav"]) {
  margin-bottom: unset;
}

span[class*="timestampInline_"] time::before {
  content: attr(aria-label);
  font-size: 12px;
}

span[class*="timestampInline_"] {
  font-size: 0px !important;
}

/* Hide nameplates */
[style^="background: linear-gradient(90deg"]:has([src*="/nameplates/"]) { display: none; }
[class*="dm_"]:has([class*="linkPlated_"]) {
    & [class*="linkPlated_"] { padding-right: var(--space-16); }
    & [class*="closeButtonPlated_"] {
        opacity: 0.7;
        &:hover { opacity: 1; }
        & [class^="innerCloseButtonPlated"] {
            opacity: unset; 
            background: none;
            & svg {
                color: inherit;
                &:is(:hover, :focus-within) { color: var(--interactive-hover); }
            }
        }
    }
}

:root {
  /* Show the `New Server` and `Explore Server` buttons while the folder sidebar is expanded
    Options: 0 - Disable buttons or 1 - Enable buttons */
  --bf-sidebar-show-extra-buttons: 0
}
.container_c48ade > div:not(.base_c48ade) {
  position: absolute;
  z-index: 1000;
  height: 50vh;
  transform: translateY(50vh);
  > nav {
    padding-top: 10px;
  }
  & + .base_c48ade .wrapper_ef3116.guilds_c48ade .stack_dbd263 .stack_dbd263 {
    height: calc(32.5vh - (var(--bf-sidebar-show-extra-buttons)) * 10.5vh);
    overflow-y: scroll;
    overflow-x: hidden;
    &::-webkit-scrollbar {
      display: none
    }
  }
}

/* REMOVE QUICK REACT BAR */
.button_f7ecac.hoverBarButton_f84418:nth-of-type(1),
.button_f7ecac.hoverBarButton_f84418:nth-of-type(2),
.button_f7ecac.hoverBarButton_f84418:nth-of-type(3),
.separator_f84418 {
   display: none;
}
```
