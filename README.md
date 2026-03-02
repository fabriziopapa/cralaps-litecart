
# LiteCart Cralaps.it

Questo è il progetto per il sito **Cralaps.it**, sviluppato utilizzando il framework **LiteCart**. L'applicazione gestisce un **G.A.S.** (Gruppo Acquisto Solidale) con funzionalità di gestione ordini e gestione degli utenti. Questo repository contiene il codice sorgente e tutte le modifiche personalizzate per il sito.

## Contenuti del progetto

- **LiteCart**: Framework per e-commerce utilizzato per la gestione delle vendite.
- **Cralaps.it**: Personalizzazioni e funzionalità specifiche per il sito web Cralaps.it
- **GitHub Repository**: Il codice sorgente è ospitato su GitHub.

## Funzionalità

- **Gestione Vendite**: Gestione avanzata delle vendite, inclusi report e statistiche.
- **Impostazioni Regionali**: Supporto per la selezione della lingua, valuta e paese (con possibilità di personalizzare il sistema di selezione).
- **Sistema di Autenticazione**: Login sicuro per gli utenti.
- **Modifiche Personalizzate**: Modifiche specifiche per il progetto, inclusi cambiamenti di design e funzionalità.

## Installazione

1. **Clone del Repository**

   Per iniziare, clona il repository usando il comando:
   
   ```bash
   git clone https://github.com/fabriziopapa/cralaps-litecart.git
   cd cralaps-litecart



# Requisiti

- Assicurati di avere i seguenti requisiti installati sul server:
- PHP 7.4 o superiore
- MySQL 5.7 o superiore
- Nginx o Apache (preferibile Nginx)
 - Composer (per la gestione delle dipendenze)

# Configurazione

Configura il file .env o le impostazioni del database nel tuo server web per abilitare l'accesso corretto.

Modifica il file includes/config.inc.php per configurare il database e altre impostazioni locali.

Avvio del progetto

Avvia il server web con Nginx o Apache

Accedi al tuo sito tramite il browser per completare l'installazione.

# Personalizzazioni
Selezione Regionale

La selezione della lingua, valuta e paese è stata personalizzata per Cralaps.it. Il box di selezione si trova nel menu in alto a destra, con la possibilità di cambiare le impostazioni regionali. Ecco il codice che gestisce la visualizzazione del box nel front-end:
```php
<div class="quick-access">
  <a class="regional-setting text-center" href="<?php echo document::href_ilink('regional_settings'); ?>#box-regional-settings" data-toggle="lightbox" data-seamless="true">
    <div class="navbar-icon"><?php echo functions::draw_fonticon('fa-globe'); ?></div>
    <small class="hidden-xs"><?php echo language::$selected['code']; ?> / <?php echo customer::$data['country_code']; ?> / <?php echo currency::$selected['code']; ?></small>
  </a>
</div>
```
Modifiche alla struttura dei template

Sono stati effettuati dei cambiamenti nel layout e nei file CSS/JS. Ad esempio, sono stati aggiornati i file CSS e JS nel template per una migliore gestione del front-end, inclusi gli aggiornamenti a app.min.css, checkout.min.css, framework.min.css, e relativi file .map.

# Disclaimer

Il presente sito è realizzato **senza scopo di lucro** e ha come unica finalità la gestione di **domanda e offerta** di prodotti e servizi nell'ottica di **ridurre i prezzi per coloro che aderiscono al G.A.S. (Gruppo di Acquisto Solidale)**.

Non sono previsti **costi di adesione** né commissioni sulle transazioni tra i membri del G.A.S.  

La normativa che permette la creazione di iniziative di questo tipo è prevista principalmente dal **Codice Civile italiano**, in particolare dagli articoli relativi alle **associazioni senza scopo di lucro** (artt. 36 e seguenti c.c.) e dal **D.Lgs. n. 460/1997** che disciplina le organizzazioni non lucrative di utilità sociale (ONLUS).  

Inoltre, la gestione dei gruppi di acquisto solidale rientra nelle attività di promozione della **solidarietà tra consumatori** e della **riduzione dei costi attraverso la cooperazione**, attività riconosciute e non soggette ad IVA secondo la normativa fiscale vigente per le associazioni non lucrative.

**Importante:** Il sito non costituisce piattaforma di vendita diretta né intermediario commerciale; ogni transazione avviene tra i membri del G.A.S. in maniera autonoma.
