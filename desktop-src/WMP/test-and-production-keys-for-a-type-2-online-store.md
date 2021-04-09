---
title: Chiavi di test e di produzione per un negozio online di tipo 2
description: Chiavi di test e di produzione per un negozio online di tipo 2
ms.assetid: 4fce47e2-d73d-4484-9bda-48257268ed96
keywords:
- Windows Media Player Online Store, chiavi di test
- archivi online, chiavi di test
- digitare 2 archivi online, chiavi di test
- Windows Media Player Online Store, chiavi di produzione
- archivi online, chiavi di produzione
- digitare 2 archivi online, chiavi di produzione
- Windows Media Player Online Stores, documento ServiceInfo
- archivi online, documento ServiceInfo
- digitare 2 archivi online, documento ServiceInfo
- test chiavi
- chiavi di produzione
- Documento ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f009e1b0ca58a66820e193e3b66f8ca50ccadc43
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955743"
---
# <a name="test-and-production-keys-for-a-type-2-online-store"></a>Chiavi di test e di produzione per un negozio online di tipo 2

Quando si inizia lo sviluppo dello Store online, Microsoft fornisce due chiavi numeriche: una chiave di test e una chiave di produzione. Allo stesso tempo, è necessario fornire a Microsoft due URL: uno che punta al documento ServiceInfo di test e uno che fa riferimento al documento ServiceInfo di produzione.

Durante la fase di sviluppo e test, il negozio online è visibile in Windows Media Player solo se la chiave di test o la chiave di produzione si trova nel registro di sistema nel computer dell'utente. Se la chiave di test si trova nel registro di sistema, Windows Media Player Recupera il documento ServiceInfo di test, che fa riferimento al plug-in, alle pagine Web e alle immagini che appartengono all'archivio di test. Se la chiave di produzione si trova nel registro di sistema, Windows Media Player Recupera il documento ServiceInfo di produzione, che fa riferimento al plug-in, alle pagine Web e alle immagini che appartengono all'archivio di produzione.

È possibile usare gli archivi di test e di produzione in qualsiasi modo. In genere, tuttavia, la distinzione è la seguente:

-   L'archivio di test è il punto in cui vengono apportate modifiche quotidiane al plug-in, alle pagine Web, alle immagini e ad altri componenti del servizio.
-   Lo Store di produzione è il luogo in cui si mantiene una versione stabile del servizio, che include il plug-in, le pagine Web, le immagini e altri componenti.

Prima di poter pubblicare l'archivio online in Windows Media Player, Microsoft deve verificare che il servizio venga eseguito correttamente. Durante la fase di convalida, Microsoft usa la chiave di produzione. Microsoft non utilizza la chiave di test durante la fase di convalida.

Quando l'archivio online di produzione completa correttamente il processo di convalida, Microsoft pubblica l'archivio, il che significa che l'archivio di produzione viene visualizzato in Windows Media Player per tutti gli utenti, non solo quelli che hanno la chiave di produzione nel registro di sistema. Dopo la pubblicazione del negozio, le chiavi di test e di produzione non sono più necessarie.

> [!Note]  
> Gli utenti potrebbero essere in grado di indovinare la chiave di test o di produzione per il negozio online e visualizzare l'archivio mentre è in fase di sviluppo. È necessario prestare attenzione a esporre le funzionalità che si desidera tenere segrete fino alla versione pubblica.

 

Per informazioni dettagliate sulla posizione in cui inserire le chiavi di produzione e di test nel registro di sistema dell'utente, vedere [chiavi e voci del registro di sistema per un archivio di tipo 2 online](registry-keys-and-entries-for-a-type-2-online-store.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sui negozi online di tipo 2**](about-type-2-online-stores.md)
</dt> <dt>

[**Digitare 2 esempi di archivio online**](type-2-online-store-samples.md)
</dt> </dl>

 

 




