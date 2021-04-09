---
title: Integrazione delle informazioni sugli album
description: Integrazione delle informazioni sugli album
ms.assetid: c59c0c1b-eddc-4061-87cc-a5c44ae0c15d
keywords:
- Windows Media Player Online Stores, integrazione delle informazioni sugli album
- archivi online, integrazione delle informazioni sugli album
- digitare 2 archivi online, integrazione delle informazioni sugli album
- Windows Media Player Online Stores, integrazione delle informazioni sugli album
- negozi online, integrazione delle informazioni sugli album
- digitare 2 archivi online, integrazione delle informazioni sugli album
- Windows Media Player, integrazione delle informazioni sugli album
- Windows Media Player, integrazione delle informazioni sugli album
- integrazione delle informazioni sugli album
- integrazione delle informazioni sugli album
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b03586217ec0a0eebd9abd0a9acae62790f838f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044633"
---
# <a name="album-info-integration"></a>Integrazione delle informazioni sugli album

Windows Media Player consente agli utenti di richiedere informazioni dettagliate sul CD o sul DVD da cui è stato originato il contenuto multimediale digitale facendo clic su un pulsante, ad esempio **altre informazioni**. Quando l'utente fa clic sul pulsante, Windows Media Player 10 o versioni successive chiama nell'archivio musica corrente per visualizzare i dettagli dell'album. Quando si verifica questa situazione, il lettore apre il riquadro informazioni album e visualizza la pagina Web specificata dall'attributo **URL** dell'elemento **AlbumInfo** del documento ServiceInfo.

Windows Media Player aggiunge una stringa di query all'URL per fornire informazioni al negozio online sul contenuto richiesto dall'utente. La stringa di query include attributi come **title**, **album** e **Artist**, che possono essere usati dall'archivio online per determinare l'album corretto da visualizzare. La documentazione di riferimento per l'elemento **AlbumInfo** fornisce l'elenco completo degli attributi della stringa di query e le relative descrizioni.

## <a name="guidelines-for-album-info"></a>Linee guida per le informazioni sugli album

Quando si crea la pagina Web relativa alle informazioni sugli album, attenersi alle linee guida seguenti:

-   La pagina deve identificare chiaramente l'archivio online che fornisce le informazioni. A tale scopo, è possibile visualizzare in primo piano il logo, ad esempio.
-   La pagina deve includere un collegamento all'informativa sulla privacy dell'azienda.
-   Quando possibile, evitare l'esplorazione delle pagine all'interno della funzionalità informazioni sugli album. Per la maggior parte delle attività, è necessario passare all'archivio online.
-   Si consiglia di fornire informazioni utili senza richiedere all'utente di installare programmi o accedere al proprio negozio online.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sui negozi online di tipo 2**](about-type-2-online-stores.md)
</dt> <dt>

[**Elemento AlbumInfo**](albuminfo-element.md)
</dt> </dl>

 

 




