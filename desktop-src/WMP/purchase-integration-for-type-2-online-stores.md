---
title: Integrazione degli acquisti per i negozi online di tipo 2
description: Integrazione degli acquisti per i negozi online di tipo 2
ms.assetid: aedaa6a0-d559-44b7-9c14-2abf44478b1c
keywords:
- Windows Media Player negozi online, integrazione degli acquisti
- negozi online, integrazione degli acquisti
- tipo 2 negozi online, integrazione degli acquisti
- Windows Media Player negozi online, integrazione degli acquisti
- negozi online, integrazione di acquisti
- Negozi online di tipo 2, integrazione degli acquisti
- Windows Media Player,integrazione degli acquisti
- Windows Media Player,integrazione degli acquisti
- integrazione dell'acquisto
- integrazione di acquisti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d854ecfd91cd0a887c242ad743874a6ec1a469ebcca3aa788bf57c2c59041d6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117746695"
---
# <a name="purchase-integration-for-type-2-online-stores"></a>Integrazione degli acquisti per i negozi online di tipo 2

Quando Windows Media Player riproduce contenuto multimediale digitale o l'utente sceglie Trova informazioni **album,** il lettore offre all'utente un collegamento per acquistare il CD o il DVD da cui il contenuto ha avuto origine se tale collegamento è disponibile. Quando l'utente fa clic sul collegamento, Windows Media Player 10 o versioni successive chiama il negozio di musica corrente per gestire la richiesta di acquisto. In questo caso, Il lettore passa al primo riquadro attività del servizio (in Windows Media Player 10) o alla scheda Negozi online (in Windows Media Player 11) e visualizza la pagina Web specificata dall'attributo **MediaPlayerURL** dell'elemento **BuyCD** del documento ServiceInfo. Gli attributi **MediaCenterURL** e **BrowserURL** vengono usati in modo simile per gestire le chiamate da Windows XP Media Center Edition 2004 e Windows XP Service Pack 2.

Windows Media Player aggiunge una stringa di query all'URL per fornire informazioni al negozio online sul contenuto scelto dall'utente per l'acquisto. La stringa di query include attributi come **Title,** **Album** e **Artist,** che il negozio online può usare per determinare l'album corretto da vendere. La documentazione di riferimento per **l'elemento BuyCD** fornisce l'elenco completo degli attributi della stringa di query e delle relative descrizioni.

## <a name="guidelines-for-the-buycd-page"></a>Linee guida per la pagina BuyCD

Quando si crea la pagina Web di BuyCD, usare le linee guida seguenti:

-   La pagina deve identificare chiaramente il negozio online che fornisce le informazioni. A tale scopo, ad esempio, è possibile visualizzare in primo piano il logo.
-   La pagina deve includere un collegamento all'informativa sulla privacy dell'azienda.
-   È meglio fornire informazioni di acquisto iniziali senza richiedere all'utente di installare programmi o accedere al negozio online.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sui negozi online di tipo 2**](about-type-2-online-stores.md)
</dt> <dt>

[**Elemento BuyCD**](buycd-element.md)
</dt> </dl>

 

 




