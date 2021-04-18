---
title: Aggiornamento delle licenze per gli archivi con logo PlaysForSure
description: Aggiornamento delle licenze per gli archivi con logo PlaysForSure
ms.assetid: d08d6b6e-937e-4dec-b7ca-376cdad069f9
keywords:
- Windows Media Player Online Stores, aggiornamento delle licenze
- negozi online, aggiornamento delle licenze
- Windows Media Player Online Stores, aggiornamento delle licenze
- archivi online, aggiornamento delle licenze
- Windows Media Player Online Stores, logo PlaysForSure
- negozi online, logo PlaysForSure
- aggiornamento delle licenze
- licenze, aggiornamento
- PlaysForSure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42e48a3ddfd2b0670e3720f7c71587d0330a69a7
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104117399"
---
# <a name="refreshing-licenses-for-stores-that-have-the-playsforsure-logo"></a>Aggiornamento delle licenze per gli archivi con logo PlaysForSure

Alcuni archivi musicali online hanno il logo PlaysForSure, ma non sono integrati con Windows Media Player 11. Questi archivi devono fornire un documento ServiceInfo e un componente leggero, in modo che Windows Media Player 11 possa ottenere e aggiornare le licenze per il contenuto.

Nell'esempio seguente viene illustrato il funzionamento del processo di aggiornamento delle licenze.

1.  L'utente ottiene 50 brani musicali dallo Store online di proseware. Ogni traccia è un file con estensione WMA. Insieme alle tracce, l'utente ottiene le licenze per riprodurre le tracce.
2.  L'utente copia le tracce 50 in un nuovo computer in cui è installato Windows Media Player 11 e aggiunge le tracce alla libreria di Media Player di Windows.
3.  In un secondo momento, il modulo di aggiornamento della licenza (LRM), che fa parte di Windows Media Player 11, esamina i metadati nelle tracce 50 e determina che Proseware è il provider di contenuti.
    > [!Note]  
    > Windows Media Player è in grado di identificare il provider di contenuti controllando l'attributo **contentdistributor** in un file multimediale. Se un negozio online con il logo PlaysForSure fornisce un file multimediale che usa Windows Media Digital Rights Management (WMDRM), l'archivio online deve inserire l'attributo **contentdistributor** nel file multimediale. Per ulteriori informazioni, vedere Aggiunta dell'attributo content Distributor in Windows Media Player SDK.

     

4.  Il LRM cerca l'URL del documento ServiceInfo di Proseware, Scarica il documento ed esamina l'elemento di **installazione** del documento per ottenere l'URL di un pacchetto che il LRM può usare per installare il componente di proseware. Il LRM installa e carica il componente.
5.  Per ognuna delle tracce 50, LRM chiama il metodo [IWMPSubscriptionService:: allowPlay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay) del componente proseware. Il metodo **allowPlay** inserisce una licenza per la singola traccia nel nuovo computer e restituisce **true** nel parametro *pfAllowPlay* .
    > [!Note]  
    > Il componente Proseware deve fornire tutte le licenze necessarie per riprodurre la singola traccia. Ovvero, se necessario, il componente deve fornire una licenza radice e una licenza foglia.

     

    Durante la prima chiamata al metodo **allowPlay** , il componente Proseware deve visualizzare una finestra di dialogo per verificare che l'utente corrente disponga di un account Proseware e abbia il diritto di riprodurre la traccia. Durante le chiamate successive a **allowPlay**, il componente può usare le credenziali ottenute nella prima chiamata per verificare che l'utente abbia il diritto di riprodurre le tracce rimanenti.

Il componente, scritto dall'archivio online, deve implementare il metodo **allowPlay** dell'interfaccia **IWMPSubscriptionService** . Il componente deve restituire E \_ NOTIMPL da ognuno degli altri tre metodi: **allowCDBurn**, **allowPDATransfer** e **startBackgroundProcessing**. Inoltre, il componente deve impostare il valore della voce del registro di sistema **capabilities** su 1; ovvero è \_ necessario impostare il flag della funzionalità Cap della sottoscrizione \_ ALLOWPLAY e tutti gli altri flag di funzionalità devono essere cancellati. Per ulteriori informazioni sulla registrazione del componente, vedere [chiavi e voci del registro di sistema per un archivio di tipo 2 online](registry-keys-and-entries-for-a-type-2-online-store.md).

Per informazioni sulla creazione di un componente che implementa l'interfaccia **IWMPSubscriptionService** , vedere [compilazione del plug-in per un negozio online di tipo 2](building-the-plug-in-for-a-type-2-online-store.md).

Per informazioni su come fornire a Microsoft un documento ServiceInfo, inviare un messaggio di posta elettronica al team di servizi virtuali di Windows Media Player. L'indirizzo di posta elettronica del team è mpsvctm@microsoft.com .

Per istruzioni tecniche sull'utilizzo di un'ampia gamma di SDK per Windows Media per creare un servizio che offra contenuti multimediali digitali con licenza, visitare il [centro per sviluppatori Microsoft Windows Media](https://msdn.microsoft.com/windowsmedia/default.aspx) e cercare "creazione di un Windows Media Player 10 sottoscrizione online store".

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> <dt>

[**Windows Media Player Online Stores**](windows-media-player-online-stores.md)
</dt> </dl>

 

 




