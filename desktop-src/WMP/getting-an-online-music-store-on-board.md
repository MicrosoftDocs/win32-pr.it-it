---
title: Ottenere un negozio online per musica online
description: Ottenere un negozio online per musica online
ms.assetid: f7eff687-9832-41bc-8f3d-a2ab11917eb0
keywords:
- Windows Media Player Online Stores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e50c5d13e14e95e88e83d42fd7d5cd00551bb507
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955679"
---
# <a name="getting-an-online-music-store-on-board"></a>Ottenere un negozio online per musica online

In questo argomento viene descritto il processo di introduzione di un archivio multimediale digitale online per Windows Media Player. Il tempo necessario per il processo di onboarding dall'inizio alla fine è di circa 45-60 giorni LAVORAtivi. Nella tabella seguente sono descritte le due fasi del processo di caricamento.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Fase</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>In sospeso</td>
<td><ul>
<li>Si invia a Microsoft le informazioni di contatto, le informazioni di avvio e gli account di convalida necessari.</li>
<li>Microsoft invia una chiave di test e una chiave di produzione.</li>
<li>Il negozio online viene testato con Windows Media Player.</li>
<li>Si inviano contratti e contratti firmati a Microsoft.</li>
</ul></td>
</tr>
<tr class="even">
<td>Convalida</td>
<td>Microsoft convalida il negozio online.</td>
</tr>
</tbody>
</table>



 

Dopo aver completato le fasi di convalida e in sospeso, Microsoft pubblicherà il proprio negozio online.

## <a name="pending-stage"></a>Fase in sospeso

La fase in sospeso ti offre la possibilità di testare il tuo negozio online in Windows Media Player. È anche opportuno assicurarsi che tutti i contratti e i contratti richiesti siano firmati. Per iniziare, inviare a Microsoft le informazioni riportate di seguito, come definito più avanti in questo argomento:

-   Informazioni contatto
-   Informazioni di avvio
-   Account di convalida

Al ricevimento del contatto e delle informazioni di avvio, Microsoft invierà una chiave di test e una chiave di produzione. Dopo aver aggiunto la chiave di test al registro di sistema e aver riavviato il lettore, il negozio online verrà visualizzato nel lettore e sarà possibile eseguirne il test. Per informazioni sulla posizione in cui inserire la chiave di test nel registro di sistema, vedere [chiavi e voci del registro di sistema per un archivio online di tipo 1](registry-keys-and-entries-for-a-type-1-online-store.md) oppure [chiavi e voci del registro di sistema per un archivio di tipo 2 online](registry-keys-and-entries-for-a-type-2-online-store.md).

È necessario testare tutti gli aspetti del negozio online, inclusi l'interfaccia utente e il plug-in. Come parte del processo di test, è necessario eseguire i test descritti nei [test di convalida per i negozi di musica online di tipo 2](validation-tests-for-type-2-online-music-stores.md).

> [!Note]  
> Gli archivi di tipo 1 devono superare tutti i test di convalida per i negozi di tipo 2, oltre ad alcuni test aggiuntivi specifici dell'esperienza di tipo 1. Per informazioni sui test di convalida di tipo 1, contattare il team virtuale di Windows Media Player Services all'indirizzo mpsvctm@microsoft.com .

 

## <a name="contact-information"></a>Informazioni sul contatto

Nella tabella seguente vengono illustrate le informazioni di contatto richieste da Microsoft per il negozio online. Compilare il [modulo informazioni di contatto](contact-information-form-for-an-online-music-store.md) e inviarlo al team virtuale di Windows Media Player Services all'indirizzo mpsvctm@microsoft.com .



| Elemento                     | Descrizione                                                                               |
|--------------------------|-------------------------------------------------------------------------------------------|
| Nome del negozio               | Nome personalizzato dell'archivio                                                            |
| Provider Name            | Nome della società del provider/etichetta bianca (se diversa)                               |
| Archivia impostazioni locali             | Le impostazioni locali dell'utente di Windows in cui deve essere visualizzato l'archivio                                |
| Categoria Archivio           | Musica, Radio, film, TV, sport, notizie, intrattenimento audio e/o altro (descrivere) |
| Modello di acquisto           | Acquisto, noleggio, sottoscrizione e/o altro (descrivere)                            |
| Lingua archivio           |                                                                                           |
| Nome/i contatto archivio    |                                                                                           |
| Invia messaggi di posta elettronica di contatto  |                                                                                           |
| Account Passport di MSFT | Questa operazione è destinata a possibili candidature future nei programmi di sviluppo di partner e beta.         |
| Indirizzo di spedizione         | Nessun P.O. Caselle                                                                             |
| City                     |                                                                                           |
| State                    |                                                                                           |
| CAP              |                                                                                           |
| Paese/Area geografica           |                                                                                           |
| Telephone                |                                                                                           |
| Fax                      |                                                                                           |
| Contatto del sondaggio           | Se ti contatteremo per la tua esperienza con il programma in futuro,        |



 

## <a name="startup-information"></a>Informazioni di avvio

Per ogni area geografica che viene utilizzata dal negozio, inviare a Microsoft un set di informazioni di avvio per l'archivio di test, un set di informazioni di avvio per l'archivio di produzione e un set di account di convalida.

Il [modulo informazioni di avvio per un archivio musicale online](startup-information-form-for-an-online-music-store.md) contiene due copie del modulo informazioni di avvio e una copia del modulo account di convalida. Compilare i moduli e inviarli al team virtuale di Windows Media Player Services all'indirizzo mpsvctm@microsoft.com .

Nella tabella seguente vengono descritte le informazioni di avvio richieste da Microsoft per il negozio online.



| Elemento                                                                                                     | Descrizione                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| URL XML informazioni servizio (limite di 2048 caratteri)                                                              | URL in cui Windows Media Player ottiene il [documento XML ServiceInfo](serviceinfo-document.md).                                                                                                                                         |
| Chiave del servizio (ID univoco)                                                                                  | Stringa che identifica in modo univoco l'archivio online. È necessario crearne uno per la produzione e uno per il testing (ad esempio, "My Store" e "MyStoreTest"). Si noti che una chiave del servizio non è la stessa di una chiave di test.                        |
| Nome descrittivo (limite di 30 caratteri)                                                                       | Nome dell'archivio visualizzato nel selettore del servizio Windows Media Player.                                                                                                                                                        |
| URL dell'immagine del menu (limite di 2048 caratteri)                                                                    | URL in cui Windows Media Player Recupera il logo 15 x 15 pixel visualizzato nel selettore del servizio.                                                                                                                                 |
| Acquista URL musica (limite di 2048 caratteri)<br/> (Solo archivi musicali integrati)<br/>                | URL usato dai collegamenti "Buy CD" e "Shop for Music online" del lettore.                                                                                                                                                              |
| URL di acquisto dell'interfaccia utente di 10 ft (limite di 2048 caratteri)<br/> (Solo archivi musicali integrati-facoltativo)<br/> | URL utilizzato dai collegamenti "Buy CD" e "Shop for Music online" del lettore in Windows XP Media Center Edition e Windows Media Center in Windows Vista.                                                                              |
| Logo dello Store (130W x 30h)<br/> (Alleghi il file PNG separatamente).<br/>                              | Logo dello Store visualizzato nella descrizione comando visualizzata quando il mouse si trova sull'immagine Sfoglia-tutto. Questo logo deve essere un file in formato PNG e preferibilmente con alpha blending, in modo che possa adattarsi alle modifiche del colore in Windows Media Player. |
| Browse-all image (108W x 108H)<br/> (Alleghi il file PNG separatamente).<br/>                       | Breve descrizione nella descrizione comando visualizzata quando il mouse si trova sull'immagine browse-all.                                                                                                                                               |
| Testo descrizione archivio (limite di 110 caratteri)                                                             | Testo visualizzato nella descrizione comando sotto il testo della descrizione dell'archivio.                                                                                                                                                                        |
| Testo per collegamento ipertestuale (limite di 45 caratteri)                                                                  | Logo dello Store visualizzato nella pagina Sfoglia tutti i negozi online. Deve essere un file in formato PNG e preferibilmente con alpha blending, in modo che possa adattarsi alle modifiche del colore in Windows Media Player.                                           |



 

> [!Note]  
> Il 108 x 108 pixel browse-all image è un requisito per Windows Media Player 11 e versioni successive.

 

> [!Note]  
> In Windows Media Player 11 e versioni successive, gli elementi ServiceTask2 e ServiceTask3 del documento XML ServiceInfo vengono ignorati. Per informazioni dettagliate sul documento XML ServiceInfo, vedere il [documento ServiceInfo](serviceinfo-document.md).

 

## <a name="validation-accounts"></a>Account di convalida

Per completare il processo di convalida descritto nella sezione relativa alla fase di convalida, Microsoft richiede cinque (5) account di convalida per ogni tipo di account offerto dallo Store online. Se, ad esempio, si offrono account che consentono di distinguere caratteristiche e funzionalità, ad esempio Basic e Premium, Microsoft dovrà avere cinque (5) account di convalida per ogni tipo, per un totale di dieci (10) account.

Inviare il nome utente e la password per ogni account di convalida a mpsvctm@microsoft.com . Includere anche il nome di una persona che Microsoft può contattare per gli account di convalida. Questi account verranno usati per la convalida mensile continua, quindi è necessario includere un processo per "ricarica" degli account. Uno dei problemi più comuni si verifica quando un negozio online non riesce a fornire un credito di acquisto sufficiente a Microsoft per convalidare tutti gli scenari di acquisto. Gli account devono rimanere attivi dopo il completamento del processo di onboarding.

## <a name="validation-stage"></a>Fase di convalida

Durante la fase di convalida, Microsoft verifica che le funzionalità primarie dello Store online funzionino correttamente. Per tutti i punti vendita (tipo 1 e tipo 2), Microsoft esegue i test di verifica descritti in dettaglio nei [test di convalida per gli archivi di musica online di tipo 2](validation-tests-for-type-2-online-music-stores.md). Microsoft esegue anche alcuni test di convalida aggiuntivi per gli archivi di tipo 1. In caso di domande sulla fase di convalida per gli archivi di tipo 1, inviare un messaggio di posta elettronica a mpsvctm@microsoft.com .

Durante la fase di convalida, Microsoft esegue due passaggi di convalida. Il primo passaggio si applica a Release Candidate 1 (RC1) del negozio online. Se l'archivio supera la convalida RC1, è consigliabile bloccarla e apportare ulteriori modifiche. Microsoft eseguirà un secondo passaggio di convalida nell'archivio anche se l'archivio supera la convalida RC1.

Se l'archivio ha esito negativo per qualsiasi parte del passaggio di convalida RC1, si avranno due settimane per creare una seconda versione candidata (RC2), che verrà convalidata da Microsoft durante il passaggio di convalida RC2.

Se l'archivio ha esito negativo per qualsiasi parte della convalida RC2, è necessario attendere fino all'avvio seguente.

## <a name="test-and-production-keys"></a>Chiavi di test e di produzione

Tenere presente che, durante la fase in sospeso, sono stati inviati Microsoft due set di informazioni di avvio: uno per l'archivio di test e uno per l'archivio di produzione. Si ricordi anche che Microsoft ha inviato due chiavi: una chiave di test e una chiave di produzione.

La chiave del test è interamente per uso personale. Quando la chiave di test si trova nel registro di sistema, Windows Media Player usa l'URL ServiceInfo inviato per l'archivio di test.

Quando la chiave di produzione si trova nel registro di sistema, Windows Media Player usa l'URL ServiceInfo inviato per l'archivio di produzione. Microsoft usa la chiave di produzione durante la fase di convalida. Microsoft non usa mai la chiave di test per la convalida.

Quando l'archivio è Live, Windows Media Player usa l'URL ServiceInfo inviato per l'archivio di produzione.

Come regola generale, l'archivio di test deve essere il punto di sviluppo del servizio e apportare modifiche giornaliere. L'archivio di produzione deve essere il posto in cui si mantiene una versione stabile del servizio.

## <a name="common-on-boarding-problems"></a>Problemi comuni di onboarding

Di seguito sono riportati alcuni problemi comuni che possono causare la mancata esecuzione del test di convalida da parte dell'archivio.

-   Errore di transizione dai server di prova ai server di produzione. Questo comporta molti problemi, ad esempio pagine mancanti, impostazioni di sicurezza e IIS non valide e account di test che non funzionano più.
-   Il collegamento di acquisto (o collegamento a negozio) nell'area di riproduzione ora non è valido. Questo può causare un errore di convalida dell'archivio anche quando tutto il resto funziona.
-   Il team di convalida di Microsoft testerà diversi scenari di acquisto che variano da piccoli acquisti a acquisti di dimensioni molto elevate. È necessario fornire un metodo ricaricabile che funga da consumer all'interno del negozio. Non è possibile convalidare l'archivio se il team di convalida non dispone di crediti di acquisto sufficienti per convalidare tutti questi scenari.

Per un elenco più completo dei problemi di caricamento comuni e delle domande frequenti compilate dal team virtuale di Windows Media Player Services, vedere [problemi di caricamento comuni per gli archivi musicali online](common-on-boarding-problems-for-online-music-stores.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Kit di benvenuto per gli archivi online](online-stores-welcome-kit.md)
</dt> </dl>

 

 





