
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

Il presente sito è realizzato senza scopo di lucro e ha come unica finalità la gestione di domanda e offerta di prodotti e servizi nell'ottica di ridurre i prezzi per coloro che aderiscono al G.A.S. (Gruppo di Acquisto Solidale).

Non sono previsti costi di adesione né commissioni sulle transazioni tra i membri del G.A.S.

Il sito non costituisce piattaforma di vendita diretta né intermediario commerciale; ogni transazione avviene tra i membri del G.A.S. in maniera autonoma.

Disclaimer per gli utenti

1. Natura dell’attività  

Il Gruppo di Acquisto Solidale (GAS) è un’attività svolta dall’Associazione di promozione sociale Ente del Terzo Settore ai sensi del d.lgs. 3 luglio 2017 n. 117, senza scopo di lucro e nel perseguimento delle finalità statutarie di solidarietà sociale, ambientale e culturale.

2. Riferimenti normativi  

Il GAS opera nel rispetto dell’art. 1, commi 266–267, della legge 24 dicembre 2007 n. 244, che disciplina i gruppi di acquisto solidale quali soggetti associativi senza scopo di lucro, che effettuano acquisti collettivi di beni distribuendoli esclusivamente agli aderenti, senza applicazione di alcun ricarico e senza svolgere attività di somministrazione o vendita al pubblico.

3. Assenza di scopo di lucro e modalità economiche  

Tutte le attività connesse al GAS sono svolte senza alcun fine di lucro.

• Non viene applicato alcun ricarico sui prezzi concordati con i fornitori.

• Eventuali contributi richiesti agli aderenti (es. spese di gestione, logistica, piattaforma) hanno natura esclusivamente di rimborso costi e non costituiscono corrispettivo commerciale.

• Non si realizza vendita al dettaglio verso il pubblico, ma mera organizzazione e coordinamento di acquisti collettivi tra fornitori e aderenti.

4. Destinatari del servizio  

L’accesso al GAS è riservato esclusivamente agli associati/aderenti regolarmente iscritti  secondo le modalità previste dallo statuto e dai regolamenti interni.  

La partecipazione al GAS presuppone la presa visione e l’accettazione del presente disclaimer e delle regole di funzionamento comunicate dall’associazione.

5. Ruolo dell’associazione e responsabilità  

L’associazione svolge un ruolo di mero intermediario organizzativo tra fornitori e aderenti, curando la raccolta delle adesioni agli ordini, il coordinamento logistico e la distribuzione dei prodotti.

• Il contratto di compravendita dei beni si intende sostanzialmente concluso tra il produttore/fornitore e il singolo aderente.

• L’associazione non assume la qualifica di venditore professionale, né svolge attività di intermediazione commerciale in senso proprio.

• L’associazione non risponde, se non nei limiti inderogabili di legge, di difetti, vizi o non conformità dei prodotti, né di eventuali danni derivanti dal loro uso improprio; ogni eventuale reclamo sulla qualità o conformità dei prodotti va indirizzato al fornitore/produttore.

6. Informazioni su prodotti e fornitori  

Le informazioni relative a prodotti, provenienza, modalità di produzione (es. biologico, a km 0, ecc.) sono fornite dai produttori/fornitori e diffuse dall’associazione agli aderenti con finalità meramente informative.  

L’associazione si impegna, per quanto ragionevolmente possibile, a selezionare fornitori coerenti con i principi etici e solidali del GAS, senza tuttavia poter garantire in via assoluta l’assenza di errori, inesattezze o aggiornamenti mancanti nelle informazioni ricevute.

7. Aspetti fiscali e limiti d’uso  

L’attività del GAS, svolta alle condizioni sopra descritte (assenza di ricarico, esclusività a favore degli aderenti, assenza di somministrazione e vendita al pubblico), è qualificata come non commerciale ai fini fiscali, secondo la disciplina vigente.  

Qualsiasi utilizzo del GAS per finalità diverse da quelle associative, solidali e non lucrative (ad esempio rivendita a terzi, attività professionale o imprenditoriale) è vietato e ricade sotto la responsabilità esclusiva dell’aderente che lo realizzi.

8. Modifiche al disclaimer  

L’associazione si riserva la facoltà di aggiornare o modificare il presente disclaimer in qualsiasi momento, anche per adeguarlo a eventuali novità normative o interpretative. Le versioni aggiornate saranno rese disponibili agli aderenti con idonei mezzi di comunicazione interna.

