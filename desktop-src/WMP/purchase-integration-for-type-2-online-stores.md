---
title: Integrazione degli acquisti per i negozi di tipo 2 online
description: Integrazione degli acquisti per i negozi di tipo 2 online
ms.assetid: aedaa6a0-d559-44b7-9c14-2abf44478b1c
keywords:
- Windows Media Player Online Stores, Purchase Integration
- negozi online, integrazione degli acquisti
- digitare 2 negozi online, integrazione degli acquisti
- Windows Media Player Online Stores, integrazione degli acquisti
- negozi online, integrazione degli acquisti
- digitare 2 negozi online, integrazione degli acquisti
- Windows Media Player, integrazione degli acquisti
- Windows Media Player, integrazione degli acquisti
- integrazione degli acquisti
- integrazione di acquisti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3d8fb56b286b66de12bb59412e7f9077eb398f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298551"
---
# <a name="purchase-integration-for-type-2-online-stores"></a>Integrazione degli acquisti per i negozi di tipo 2 online

Quando Windows Media Player riproduce contenuto multimediale digitale o l'utente sceglie **trova informazioni sugli album**, il lettore offre all'utente un collegamento per acquistare il CD o il DVD da cui è stato originato il contenuto se è disponibile un collegamento di questo tipo. Quando l'utente fa clic sul collegamento, Windows Media Player 10 o versioni successive chiama nell'archivio musica corrente per gestire la richiesta di acquisto. Quando si verifica questa situazione, il lettore passa al primo riquadro attività del servizio (in Windows Media Player 10) o alla scheda Online Stores (in Windows Media Player 11) e visualizza la pagina Web specificata dall'attributo **MediaPlayerURL** dell'elemento **BuyCD** del documento ServiceInfo. Gli attributi **MediaCenterURL** e **BrowserURL** vengono utilizzati in modo analogo per gestire le chiamate da Windows xp Media Center Edition 2004 e Windows XP Service Pack 2.

Windows Media Player aggiunge una stringa di query all'URL per fornire informazioni al negozio online sul contenuto che l'utente ha scelto di acquistare. La stringa di query include attributi come **title**, **album** e **Artist**, che possono essere usati dall'archivio online per determinare l'album corretto da vendere. La documentazione di riferimento per l'elemento **BuyCD** fornisce l'elenco completo degli attributi della stringa di query e le relative descrizioni.

## <a name="guidelines-for-the-buycd-page"></a>Linee guida per la pagina BuyCD

Quando si crea la pagina Web BuyCD, usare le linee guida seguenti:

-   La pagina deve identificare chiaramente l'archivio online che fornisce le informazioni. A tale scopo, è possibile visualizzare in primo piano il logo, ad esempio.
-   La pagina deve includere un collegamento all'informativa sulla privacy dell'azienda.
-   È preferibile fornire le informazioni di acquisto iniziali senza richiedere all'utente di installare programmi o accedere al proprio negozio online.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sui negozi online di tipo 2**](about-type-2-online-stores.md)
</dt> <dt>

[**Elemento BuyCD**](buycd-element.md)
</dt> </dl>

 

 




