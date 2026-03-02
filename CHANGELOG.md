# CHANGELOG

## [Unreleased] - 2026-03-01
### Modifiche al frontend
- Disabilitata la visualizzazione della selezione rapida `Lingua / Paese / Valuta` nella barra superiore del frontend.
- File interessati:
  - `includes/templates/default.catalog/views/quick_access.inc.php` (o file equivalente in cui si trovava il blocco `<div class="quick-access">`)
- Dettagli della modifica:
  - Commentata o rimossa la porzione di codice:
    ```php
    <small class="hidden-xs"><?php echo language::$selected['code']; ?> / <?php echo customer::$data['country_code']; ?> / <?php echo currency::$selected['code']; ?></small>
    ```
  - Il link alla pagina di `regional_settings` è rimasto intatto, ma non viene più mostrato il codice lingua, paese e valuta.

### Motivazione
- Pulizia della UI per evitare confusione agli utenti.  
- Gestione della localizzazione rimane centralizzata nella pagina dedicata `/regional_settings`.

---

## [2026-02-28] - Importazione iniziale LiteCart Cralaps.it
- Backup e commit iniziale del progetto su repository Git.
