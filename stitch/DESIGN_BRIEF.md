# SETFARM_STITCH_V3_GENERATION_CONTRACT

contract_schema: setfarm.design-generation-targets.v1
product_spec_hash: 6d3dd22f56e43cbd22eea26c979c4ef458e7aecc7d4b652b79c85490d2de1bd6
stage_id: all-targets-preview
Generate exactly 1 screens and no others in this response.
Target device type: DESKTOP.
All visible user-facing text must be in tr.

## EXACT_SCREEN_TARGETS
SCREEN_TARGET_1:
- target_ref: TARGET_TERCIH_PAGE
- surface_ref: SURF_TERCIH_PAGE
- exact_screen_title: Tercih Sayfası - Tercih Hazır Aracı
- surface_kind: page
- exact_actions:
  - action_ref: ACT_HAZIR_BUTTON_CLICK
    visible_intent: Hazır Düğmesi Tıklaması
    exact_action_attribute: data-action="ACT_HAZIR_BUTTON_CLICK"
    exact_input_mappings: none
    exact_observable_selectors: [{"observableRef":"OBS_BTN_ENABLED","selector":{"actionRef":"ACT_HAZIR_BUTTON_CLICK","kind":"accessibility","name":"Hazır","role":"button","surfaceRef":"SURF_TERCIH_PAGE"}},{"observableRef":"OBS_BTN_VISIBLE","selector":{"actionRef":"ACT_HAZIR_BUTTON_CLICK","kind":"accessibility","name":"Hazır","role":"button","surfaceRef":"SURF_TERCIH_PAGE"}},{"observableRef":"OBS_STATUS_AFTER_RELOAD","selector":{"kind":"surface","surfaceRef":"SURF_TERCIH_PAGE"}},{"observableRef":"OBS_STATUS_DISPLAYED","selector":{"kind":"surface","surfaceRef":"SURF_TERCIH_PAGE"}},{"observableRef":"OBS_STAYS_ON_TERCIH","selector":{"kind":"surface","surfaceRef":"SURF_TERCIH_PAGE"}}]

## MACHINE_READABLE_COMPLETENESS_RULES
- The returned screen title must equal exact_screen_title byte-for-byte. Do not abbreviate, translate, normalize, decorate, or rename it.
- Return exactly one screen for each SCREEN_TARGET and no style-guide, assistant, summary, moodboard, PRD, or extra canvas.
- For every exact_actions entry, render exactly one actionable HTML element and preserve the exact data-action="ACT_*" attribute on that same button, link, or input element.
- Do not put ACT_* only in prose, labels, nearby wrappers, comments, scripts, or a different DOM element; the actionable element itself owns data-action.
- For every exact_input_mappings entry, exactly one value-providing element must preserve data-action-input="ACT_*.field". A checkbox/action element may carry both data-action and data-action-input when it supplies its own value.
- For every exact_observable_selectors entry, preserve the exact selector contract: control selectors bind the same data-action element, surface selectors require one wrapper with data-surface-id equal to the exact SURF_* ref, and accessibility selectors require the exact role plus an explicit aria-label equal to the declared name byte-for-byte on one element. The Setfarm converter assigns semantic observable IDs only after this exact match.
- Do not emit any button, link, input, textarea, select, checkbox, tab, menu item, or other actionable control that is not declared by exact_actions or exact_input_mappings.
- Disabled-looking, placeholder, icon-only, overflow, breadcrumb, navigation, and decorative controls are still controls and are forbidden unless declared above.
- Custom data-action and data-action-input attributes are contractual source, not visual copy. Preserve their exact case and spelling in exported HTML.

## PRODUCT_SCOPE
Product: Tercih Hazır Aracı
Goals: /tercih sayfasındaki Hazır düğmesi uygulama durumunu hazır olarak işaretler; hazır değerini yerel depolamada sayfa yenilemelerinden sonra korur; Durum hazır metnini ve hazır değerini görüntüler; düğme görünür ve etkin kalır; kullanıcı /tercih yolunda kalır.
Do not invent product behavior outside the typed targets above.