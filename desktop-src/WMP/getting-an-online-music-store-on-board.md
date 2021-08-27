---
title: Ottenere un'on board Musica Store online
description: Ottenere un'on board Musica Store online
ms.assetid: f7eff687-9832-41bc-8f3d-a2ab11917eb0
keywords:
- Windows Media Player Negozi online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcff5aeed04ff2e60b03e7b546de23f1d0d747b9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477207"
---
# <a name="getting-an-online-music-store-on-board"></a>Ottenere un'on board Musica Store online

Questo argomento descrive il processo di importazione di un archivio multimediale digitale online per Windows Media Player. Il tempo necessario per il processo di on boarding dall'inizio alla fine è di circa 45-60 giorni lavorativi. Le due fasi del processo di on boarding sono descritte nella tabella seguente.




| Fase | Descrizione | 
|-------|-------------|
| In sospeso | <ul><li>Si inviano a Microsoft le informazioni di contatto, le informazioni di avvio e gli account di convalida necessari.</li><li>Microsoft invia una chiave di test e una chiave di produzione.</li><li>Testare lo store online con Windows Media Player.</li><li>Si inviano contratti e contratti firmati a Microsoft.</li></ul> | 
| Convalida | Microsoft convalida lo store online. | 




 

Dopo aver completato le fasi di convalida e in sospeso, Microsoft pubblicherà lo store online.

## <a name="pending-stage"></a>Fase in sospeso

La fase in sospeso offre la possibilità di testare lo store online in Windows Media Player. È anche il momento di assicurarsi che tutti i contratti e i contratti necessari siano firmati. Per iniziare, inviare a Microsoft le informazioni seguenti, come definito più avanti in questo argomento:

-   Informazioni contatto
-   Informazioni di avvio
-   Account di convalida

Al momento della ricezione delle informazioni di contatto e di avvio, Microsoft invierà una chiave di test e una chiave di produzione. Dopo aver aggiunto la chiave di test al registro e aver riavviato Player, lo store online verrà visualizzato nel lettore e sarà possibile testarlo. Per informazioni su dove inserire la chiave di test nel Registro di sistema, vedere Chiavi e voci del Registro di sistema per un negozio online di tipo [1](registry-keys-and-entries-for-a-type-1-online-store.md) o Chiavi e voci del Registro di sistema per un negozio online di tipo [2.](registry-keys-and-entries-for-a-type-2-online-store.md)

È consigliabile testare tutti gli aspetti dello store online, inclusa l'interfaccia utente e il plug-in. Come parte del processo di test, è necessario eseguire i test descritti in Test di convalida per il tipo [2 online Musica store](validation-tests-for-type-2-online-music-stores.md).

> [!Note]  
> Gli archivi di tipo 1 devono superare tutti i test di convalida per gli archivi di tipo 2, oltre ad alcuni test aggiuntivi specifici dell'esperienza di tipo 1. Per informazioni sui test di convalida di tipo 1, contattare il team virtuale Windows Media Player Services all'indirizzo mpsvctm@microsoft.com .

 

## <a name="contact-information"></a>Informazioni sul contatto

La tabella seguente mostra le informazioni di contatto richieste da Microsoft per il negozio online. Compilare il [modulo Contact Information (Informazioni di](contact-information-form-for-an-online-music-store.md) contatto) e inviarlo al team virtuale Windows Media Player Services all'indirizzo mpsvctm@microsoft.com .



| Elemento                     | Descrizione                                                                               |
|--------------------------|-------------------------------------------------------------------------------------------|
| Nome del negozio               | Nome del negozio                                                            |
| Provider Name            | Nome dell'azienda di provider/white label (se diversa)                               |
| Impostazioni locali dello Store             | Le Windows impostazioni locali dell'utente presenti nello Store devono essere visualizzate in                                |
| Categoria store           | Musica, Radio, Film, TV, Sport, Notizie, Audio Intrattenimento e/o Altro (descrivere) |
| Modello di acquisto           | Acquisto, noleggio, sottoscrizione e/o altro (descrizione)                            |
| Store Language           |                                                                                           |
| Store Contact Name(s)    |                                                                                           |
| Messaggi di posta elettronica di contatto del punto vendita  |                                                                                           |
| Account Passport MSFT | Questo è per possibili candidature future nei programmi di sviluppo beta e partner.         |
| Indirizzo di spedizione         | Nessuna P.O. Scatole                                                                             |
| City                     |                                                                                           |
| State                    |                                                                                           |
| CAP              |                                                                                           |
| Paese/Area geografica           |                                                                                           |
| Telephone                |                                                                                           |
| Fax                      |                                                                                           |
| Contatto sondaggio           | È possibile contattare l'utente in caso di esperienza con il programma in futuro?        |



 

## <a name="startup-information"></a>Informazioni di avvio

Per ogni area geografica che verrà servita dal negozio, inviare a Microsoft un set di informazioni di avvio per l'archivio di test, un set di informazioni di avvio per l'archivio di produzione e un set di account di convalida.

L'argomento Modulo informazioni di avvio per un archivio [online Musica contiene](startup-information-form-for-an-online-music-store.md) due copie del modulo Informazioni di avvio e una copia del modulo Account di convalida. Compilare i moduli e inviarli al team virtuale Windows Media Player Services all'indirizzo mpsvctm@microsoft.com .

La tabella seguente descrive le informazioni di avvio richieste da Microsoft per il negozio online.



| Elemento                                                                                                     | Descrizione                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| URL XML informazioni servizio (limite di 2048 caratteri)                                                              | URL in cui Windows Media Player il documento [XML ServiceInfo.](serviceinfo-document.md)                                                                                                                                         |
| Chiave servizio (ID univoco)                                                                                  | Stringa che identifica in modo univoco il negozio online. È necessario crearne uno per la produzione e uno per il test, ad esempio "MyStore" e "MyStoreTest". Si noti che una chiave del servizio non corrisponde a una chiave di test.                        |
| Nome descrittivo (limite di 30 caratteri)                                                                       | Nome dello store visualizzato nel selettore Windows Media Player servizio di archiviazione.                                                                                                                                                        |
| URL immagine menu (limite di 2048 caratteri)                                                                    | URL in cui Windows Media Player recupera il logo da 15 x 15 pixel visualizzato nel selettore del servizio.                                                                                                                                 |
| Acquistare Musica URL (limite di 2048 caratteri)<br/> (solo store di musica integrati)<br/>                | URL usato dai collegamenti "Buy CD" (Acquista CD) e "Shop for Musica Online" (Acquista CD) del lettore.                                                                                                                                                              |
| URL di acquisto dell'interfaccia utente di 10 ft (limite di 2048 caratteri)<br/> (Solo store di musica integrati -- Facoltativo)<br/> | L'URL usato dai collegamenti "Acquista CD" e "Acquista CD" del lettore per Musica Online in Windows XP Media Center Edition e in Windows Media Center in Windows Vista.                                                                              |
| Logo dello Store (130 x 30h)<br/> Allegare il file PNG separatamente.<br/>                              | Logo dello Store visualizzato nella descrizione comando visualizzata quando il mouse viene spostato sull'immagine browse-all. Questo logo deve essere un file in formato PNG e preferibilmente con alpha blended, in modo da poter essere adattato alle variazioni di colore Windows Media Player. |
| Browse-all Image (108w x 108h)<br/> Allegare il file PNG separatamente.<br/>                       | Breve descrizione nella descrizione comando visualizzata quando il mouse si trova sopra l'immagine browse-all.                                                                                                                                               |
| Testo della descrizione dell'archivio (limite di 110 caratteri)                                                             | Testo visualizzato nella descrizione comando sotto il testo della descrizione del negozio.                                                                                                                                                                        |
| Testo per il collegamento ipertestuale (limite di 45 caratteri)                                                                  | Logo dello Store visualizzato nella pagina Esplora tutti i negozi online. Deve essere un file in formato PNG e preferibilmente con alpha blended in modo da poter essere adattato alle modifiche del colore in Windows Media Player.                                           |



 

> [!Note]  
> L'immagine browse-all da 108 x 108 pixel è un requisito per Windows Media Player 11 e versioni successive.

 

> [!Note]  
> In Windows Media Player 11 e versioni successive, gli elementi ServiceTask2 e ServiceTask3 del documento XML ServiceInfo vengono ignorati. Per informazioni dettagliate sul documento XML ServiceInfo, vedere [Documento ServiceInfo](serviceinfo-document.md).

 

## <a name="validation-accounts"></a>Account di convalida

Per completare il processo di convalida descritto nella sezione Fase di convalida seguente, Microsoft richiede cinque (5) account di convalida per ogni tipo di account offerta dal negozio online. Ad esempio, se si offrono account che differenziano funzionalità e funzionalità, ad esempio Basic e Premium, Microsoft avrà bisogno di cinque (5) account di convalida per ogni tipo, per un totale di dieci (10) account.

Inviare il nome utente e la password per ogni account di convalida a mpsvctm@microsoft.com . Includere anche il nome di una persona che Microsoft può contattare per gli account di convalida. Questi account verranno usati per la convalida mensile in corso, quindi includere un processo per "ricaricare" gli account. Uno dei problemi più comuni si verifica quando un negozio online non riesce a fornire un credito di acquisto sufficiente per Microsoft per convalidare tutti gli scenari di acquisto. Gli account devono rimanere attivi al termine del processo di on boarding.

## <a name="validation-stage"></a>Fase di convalida

Durante la fase di convalida, Microsoft verifica che le funzionalità principali del negozio online funzionino correttamente. Per tutti i negozi (tipo 1 e tipo 2), Microsoft esegue i test di verifica dettagliati in Test di convalida per il tipo [2 Online Musica Stores](validation-tests-for-type-2-online-music-stores.md). Microsoft esegue anche alcuni test di convalida aggiuntivi per gli archivi di tipo 1. In caso di domande sulla fase di convalida per i negozi di tipo 1, inviare un messaggio di posta elettronica a mpsvctm@microsoft.com .

Durante la fase di convalida, Microsoft esegue due passaggi di convalida. Il primo passaggio si applica alla versione finale candidata 1 (RC1) dello store online. Se l'archivio supera la convalida RC1, è necessario bloccarlo e non apportare altre modifiche. Microsoft eserciterà un secondo passaggio di convalida nell'archivio anche se supera la convalida RC1.

Se l'archivio non supera una parte del passaggio di convalida RC1, saranno disponibili due settimane per creare una seconda versione finale candidata (RC2), che Verrà convalidata da Microsoft durante il passaggio di convalida RC2.

Se l'archivio non supera una parte della convalida RC2, è necessario attendere l'avvio seguente.

## <a name="test-and-production-keys"></a>Chiavi di test e di produzione

Si ricordi che, durante la fase in sospeso, sono stati inviati a Microsoft due set di informazioni di avvio: uno per l'archivio di test e uno per l'archivio di produzione. Ricordare anche che Microsoft ha inviato due chiavi: una chiave di test e una chiave di produzione.

La chiave di test è interamente per uso personale. Quando la chiave di test si trova nel registro, Windows Media Player usa l'URL ServiceInfo inviato per l'archivio di test.

Quando la chiave di produzione si trova nel registro, Windows Media Player usa l'URL ServiceInfo inviato per l'archivio di produzione. Microsoft usa la chiave di produzione durante la fase di convalida. Microsoft non usa mai la chiave di test per la convalida.

Quando lo store è live, Windows Media Player usa l'URL ServiceInfo inviato per l'archivio di produzione.

Come regola generale, l'archivio test deve essere la posizione in cui si sviluppa il servizio e si apportano modifiche giornaliere. L'archivio di produzione deve essere la posizione in cui mantenere una versione stabile del servizio.

## <a name="common-on-boarding-problems"></a>Problemi comuni di on-boarding

Di seguito sono riportati alcuni problemi comuni che possono causare l'esito negativo dei test di convalida nell'archivio.

-   Non è possibile eseguire la transizione dai server di test ai server di produzione. Ciò comporta molti problemi, ad esempio pagine mancanti, IIS non valido e impostazioni di sicurezza e account di test che non funzionano più.
-   Il collegamento Acquista (o il collegamento Acquista) nell'area Attualmente in riproduzione non è valido. Ciò può causare la mancata convalida dell'archivio anche quando tutto il resto funziona.
-   Il team di convalida di Microsoft testerà diversi scenari di acquisto, da piccoli acquisti ad acquisti di grandi dimensioni. È necessario fornire un modo per consentire loro di agire come consumer all'interno del negozio. Il negozio non può essere convalidato se il team di convalida non dispone di crediti di acquisto sufficienti per convalidare tutti questi scenari.

Per un elenco più completo dei problemi di on-boarding comuni e delle domande frequenti compilate dal team virtuale di Windows Media Player Services, vedere Problemi comuni di [on-boarding](common-on-boarding-problems-for-online-music-stores.md)per online Musica Stores.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Kit di benvenuto per negozi online](online-stores-welcome-kit.md)
</dt> </dl>

 

 





