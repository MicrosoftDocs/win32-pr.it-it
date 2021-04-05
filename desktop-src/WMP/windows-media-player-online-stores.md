---
title: Windows Media Player Online Stores
description: Windows Media Player Online Stores
ms.assetid: 81009d7b-5c2a-4447-a85e-138ab7834b7a
keywords:
- Windows Media Player Online Stores, informazioni
- negozi online, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55046508b1e3a4d0a3a254fd294e5f271a2802f5
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "103724076"
---
# <a name="windows-media-player-online-stores"></a>Windows Media Player Online Stores

> [!Note]  
> In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

Windows Media Player fornisce funzionalità che consentono ai provider di contenuti multimediali digitali di integrare i propri servizi con Windows Media Player. L'integrazione tra il lettore e un archivio multimediale digitale online offre un'esperienza piacevole e completa per l'utente, tra cui la possibilità di individuare contenuto, scaricare e gestire file, riprodurre contenuto e copiare contenuto in CDs o dispositivi.

## <a name="contacting-microsoft"></a>Contatti con Microsoft

Se si vuole che l'archivio multimediale digitale online sia integrato con Windows Media Player, ma non è ancora stato fatto contatto con Microsoft, è possibile iniziare inviando un messaggio di posta elettronica al team virtuale di Windows Media Player Services. L'indirizzo di posta elettronica del team è mpsvctm@microsoft.com .

## <a name="for-more-information"></a>Ulteriori informazioni

Per istruzioni tecniche sull'utilizzo di un'ampia gamma di SDK per Windows Media per creare un servizio che offra contenuti multimediali digitali con licenza, visitare il [centro per sviluppatori Microsoft Windows Media](https://msdn.microsoft.com/windowsmedia/default.aspx) e cercare "creazione di un Windows Media Player 10 sottoscrizione online store".

## <a name="online-stores-in-windows-media-player-9-series"></a>Archivi online nella serie Windows Media Player 9

Nella serie Windows Media Player 9 è stato introdotto il concetto di negozi online. Nella serie Windows Media Player 9 i provider di negozi online possono integrare i propri servizi nella funzionalità **Servizi Premium** di Windows Media Player.

## <a name="online-stores-in-windows-media-player-10"></a>Archivi online in Windows Media Player 10

In Windows Media Player 10, i servizi Premium sono stati rinominati negozi online e sono state aggiunte le nuove funzionalità seguenti:

-   Windows Media Player fornisce fino a tre riquadri attività utilizzabili dal negozio online.
-   Quando un utente sceglie, nell'interfaccia utente del lettore, per visualizzare altre informazioni sul contenuto multimediale digitale, Windows Media Player chiama sull'archivio online per fornire le informazioni.
-   Quando l'utente sceglie, nell'interfaccia utente del lettore, per acquistare un elemento multimediale, Windows Media Player chiamare lo Store online per gestire l'acquisto.
-   Il negozio online può fornire un plug-in che Windows Media Player richiede assistenza con Digital Rights Management e la tempistica di elaborazione in background.
-   Gli archivi online possono essere integrati con il programma di installazione di Windows Media Player.

## <a name="online-stores-in-windows-media-player-11"></a>Archivi online in Windows Media Player 11

Windows Media Player 11 introduce un nuovo tipo di Music Store online, che è integrato in maniera più approfondita nell'interfaccia utente del lettore. In Windows Media Player 11 sono state aggiunte le nuove funzionalità seguenti per supportare questo nuovo tipo di archivio online.

-   Windows Media Player Scarica il catalogo multimediale del negozio online, in modo che l'utente possa esplorare rapidamente il contenuto del negozio online.
-   Windows Media Player Visualizza il contenuto musicale del negozio online nel controllo di visualizzazione albero della libreria.
-   Quando l'utente naviga nell'interfaccia utente del lettore, il lettore chiama lo Store online per fornire pagine Web che migliorano l'esperienza dell'utente.
-   Il negozio online fornisce un plug-in che gestisce tutti gli aspetti della comunicazione tra Windows Media Player e il negozio online. Il plug-in gestisce ad esempio l'accesso, il rinnovo della licenza, l'aggiornamento del catalogo, il download del contenuto e l'acquisto di contenuti.
-   Windows Media Player offre comunicazioni avanzate tra il lettore e le pagine Web fornite dal negozio online e ospitate nel lettore.

## <a name="types-of-online-stores"></a>Tipi di negozi online

Esistono due tipi di archivi online: tipo 1 e tipo 2.

Un archivio di tipo 1 fornisce il livello di integrazione più avanzato con Windows Media Player. Fornisce un catalogo musicale scaricabile ed è strettamente integrato nell'interfaccia utente del lettore. Gli archivi di tipo 1 sono supportati da Windows Media Player 11 e versioni successive.

Gli archivi di tipo 2, supportati da Windows Media Player 9 Series e versioni successive, presentano due sottocategorie: negozi commerciali e Music Store.

Un negozio commerciale offre l'esperienza di base, fornendo fino a tre riquadri attività del servizio che visualizzano le pagine Web del negozio.

Un Music Store offre un'esperienza più integrata per l'utente rispetto a un negozio commerciale. In un Music Store gli utenti possono fare clic su pulsanti e collegamenti in Windows Media Player (all'esterno delle pagine Web fornite dal negozio) per eseguire azioni quali l'acquisto di un CD o DVD, l'acquisizione di altre informazioni su un particolare elemento multimediale o la visualizzazione del riquadro visualizzazione centro informazioni. In ogni caso, Windows Media Player chiama l'archivio musicale corrente per gestire queste richieste.

> [!Note]  
> Alcuni documenti fanno riferimento a negozi commerciali come servizi commerciali di base e fanno riferimento a Music Store come servizi musicali integrati.

 

Nella tabella seguente sono illustrate le funzionalità disponibili per i diversi tipi di archivi online.



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Funzionalità</th>
<th>Tipo 2 Store Commerce</th>
<th>Digitare 2 Music Store</th>
<th>Archivio di tipo 1</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Crea riquadri attività servizio
<blockquote>
[!Note]<br />
Windows Media Player 10 presenta fino a tre riquadri attività del servizio. Windows Media Player 11 ne include solo uno.
</blockquote>
<br/></td>
<td>Sì</td>
<td>Sì</td>
<td>Sì</td>
</tr>
<tr class="even">
<td>Modificare l'aspetto dell'archivio cambiando gli attributi, ad esempio il colore del pulsante, il colore della barra delle applicazioni e il testo del pulsante.</td>
<td>Sì</td>
<td>Sì</td>
<td>Sì</td>
</tr>
<tr class="odd">
<td>Aggiungere le immagini del logo al menu e alla barra delle applicazioni di Windows Media Player Online Store.</td>
<td>Sì</td>
<td>Sì</td>
<td>Sì</td>
</tr>
<tr class="even">
<td>Passare da HTMLView al negozio online.</td>
<td>Sì</td>
<td>Sì</td>
<td>Sì</td>
</tr>
<tr class="odd">
<td>Gestire le richieste di Media Player Windows per acquistare un CD o un DVD.</td>
<td>No</td>
<td>Sì</td>
<td>Sì</td>
</tr>
<tr class="even">
<td>Gestire le richieste di Media Player Windows per fornire informazioni dettagliate sugli album.</td>
<td>No</td>
<td>Sì</td>
<td>Sì</td>
</tr>
<tr class="odd">
<td>Fornire la pagina Web visualizzazione centro informazioni.</td>
<td>No</td>
<td>Sì</td>
<td>Sì</td>
</tr>
<tr class="even">
<td>Personalizzare il programma di installazione di Windows Media Player per specificare un archivio online iniziale.</td>
<td>No</td>
<td>Sì</td>
<td>Sì</td>
</tr>
<tr class="odd">
<td>Specificare un plug-in che implementi <a href="/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice"><strong>IWMPSubscriptionService</strong></a>.
<blockquote>
[!Note]<br />
In Windows Media Player 10 e versioni successive, questo plug-in può implementare anche <a href="/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2"><strong>IWMPSubscriptionService2</strong></a>.
</blockquote>
<br/></td>
<td>No</td>
<td>Sì</td>
<td>No</td>
</tr>
<tr class="even">
<td>Fornire un catalogo musicale scaricato da Windows Media Player</td>
<td>No</td>
<td>No</td>
<td>Sì</td>
</tr>
<tr class="odd">
<td>Fornire pagine Web personalizzate e menu di scelta rapida in base alla navigazione dell'utente nell'interfaccia utente del lettore.</td>
<td>No</td>
<td>No</td>
<td>Sì</td>
</tr>
<tr class="even">
<td>Specificare un plug-in che implementi <a href="/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner"><strong>IWMPContentPartner</strong></a>.</td>
<td>No</td>
<td>No</td>
<td>Sì</td>
</tr>
</tbody>
</table>



 

Il resto della documentazione sugli archivi online è suddiviso nelle sezioni seguenti.



| Sezione                                                                                                                              | Descrizione                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Kit di benvenuto per gli archivi online](online-stores-welcome-kit.md)                                                                           | Contiene informazioni su come portare un archivio multimediale digitale online nella bacheca di Windows Media Player.             |
| [Digitare 1 negozi online](type-1-online-stores.md)                                                                                     | Contiene informazioni sulle sezioni about, guide e Reference per gli archivi online di tipo 1.                                             |
| [Digitare 2 archivi online](type-2-online-stores.md)                                                                                     | Contiene informazioni sulle sezioni about, guide e Reference per i negozi online di tipo 2.                                             |
| [Informazioni comuni ai negozi online di tipo 1 e di tipo 2](information-common-to-type-1-and-type-2-online-stores.md)                   | Contiene informazioni che si applicano sia ai negozi online di tipo 1 che di tipo 2.                                          |
| [Aggiornamento delle licenze per gli archivi con logo PlaysForSure](refreshing-licenses-for-stores-that-have-the-playsforsure-logo.md) | Sono incluse informazioni sulla modalità di aggiornamento delle licenze per gli archivi online non integrati con Windows Media Player. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Windows Media Player SDK**](windows-media-player-sdk.md)
</dt> </dl>

 

 





