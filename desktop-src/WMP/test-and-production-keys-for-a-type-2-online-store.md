---
title: Chiavi di test e produzione per uno Store online di tipo 2
description: Chiavi di test e produzione per uno Store online di tipo 2
ms.assetid: 4fce47e2-d73d-4484-9bda-48257268ed96
keywords:
- Windows Media Player online, chiavi di test
- negozi online, chiavi di test
- store online di tipo 2, chiavi di test
- Windows Media Player negozi online, chiavi di produzione
- negozi online, chiavi di produzione
- store online di tipo 2, chiavi di produzione
- Windows Media Player negozi online, documento ServiceInfo
- negozi online, documento ServiceInfo
- Tipo 2 negozi online, documento ServiceInfo
- chiavi di test
- chiavi di produzione
- Documento ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e0914417aa58d16c89c31ef0efbba6b5b2df70b69c0df62f809880ced33ee91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118118423"
---
# <a name="test-and-production-keys-for-a-type-2-online-store"></a>Chiavi di test e produzione per uno Store online di tipo 2

Quando si inizia lo sviluppo del negozio online, Microsoft fornisce due chiavi numeriche: una chiave di test e una chiave di produzione. Allo stesso tempo, è necessario fornire a Microsoft due URL: uno che punta al documento ServiceInfo di test e uno che punta al documento ServiceInfo di produzione.

Durante la fase di sviluppo e test, il negozio online è visibile in Windows Media Player solo se la chiave di test o la chiave di produzione si trova nel Registro di sistema nel computer dell'utente. Se la chiave di test si trova nel Registro di sistema, Windows Media Player recupera il documento ServiceInfo di test, che punta al plug-in, alle pagine Web e alle immagini che appartengono all'archivio test. Se la chiave di produzione si trova nel Registro di sistema, Windows Media Player recupera il documento ServiceInfo di produzione, che punta al plug-in, alle pagine Web e alle immagini che appartengono all'archivio di produzione.

È possibile usare i negozi di test e di produzione in qualsiasi modo si trovino utili. In genere, tuttavia, la distinzione è la seguente:

-   L'archivio test è la posizione in cui si apportano modifiche giornaliere al plug-in, alle pagine Web, alle immagini e ad altri componenti del servizio.
-   L'archivio di produzione è la posizione in cui si mantiene una versione stabile del servizio, che include plug-in, pagine Web, immagini e altri componenti.

Prima che il negozio online possa essere pubblicato in Windows Media Player, Microsoft deve verificare che il servizio funzioni correttamente. Durante la fase di convalida, Microsoft usa la chiave di produzione. Microsoft non usa la chiave di test durante la fase di convalida.

Quando il negozio online di produzione completa correttamente il processo di convalida, Microsoft pubblica il negozio, il che significa che il negozio di produzione viene visualizzato nel Windows Media Player per tutti gli utenti, non solo per quelli che hanno la chiave di produzione nel Registro di sistema. Dopo la pubblicazione dell'archivio, le chiavi di test e di produzione non sono più necessarie.

> [!Note]  
> Gli utenti potrebbero essere in grado di indovinare la chiave di test o di produzione per il negozio online e visualizzare il negozio durante lo sviluppo. È consigliabile prestare attenzione all'esposizione delle funzionalità che si desidera mantenere segrete fino al rilascio pubblico.

 

Per informazioni dettagliate su dove inserire le chiavi di produzione e di test nel Registro di sistema dell'utente, vedere Chiavi e voci del Registro di sistema per un negozio online di [tipo 2.](registry-keys-and-entries-for-a-type-2-online-store.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sui negozi online di tipo 2**](about-type-2-online-stores.md)
</dt> <dt>

[**Esempi di Tipo 2 Online Store**](type-2-online-store-samples.md)
</dt> </dl>

 

 




