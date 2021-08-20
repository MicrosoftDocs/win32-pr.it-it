---
title: Integrazione delle informazioni sull'album
description: Integrazione delle informazioni sull'album
ms.assetid: c59c0c1b-eddc-4061-87cc-a5c44ae0c15d
keywords:
- Windows Media Player store online, integrazione delle informazioni sull'album
- negozi online, integrazione delle informazioni sull'album
- Tipo 2 di negozi online, integrazione delle informazioni sull'album
- Windows Media Player online store, integrazione di informazioni sull'album
- negozi online, integrazione di informazioni sull'album
- store online di tipo 2, integrazione delle informazioni sull'album
- Windows Media Player,integrazione di informazioni sull'album
- Windows Media Player,integrazione delle informazioni sull'album
- Integrazione delle informazioni sull'album
- integrazione di informazioni sull'album
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcdd8c0c200d0d1779ecc9d4f90da3f3755f276431792f7a6b6450dd43e51cd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055429"
---
# <a name="album-info-integration"></a>Integrazione delle informazioni sull'album

Windows Media Player consente agli utenti di richiedere informazioni dettagliate sul CD o DVD da cui ha avuto origine il contenuto multimediale digitale facendo clic su un pulsante, ad esempio **Altre informazioni**. Quando l'utente fa clic sul pulsante, Windows Media Player 10 o versioni successive chiama il negozio di musica corrente per visualizzare i dettagli dell'album. In questo caso, Il lettore apre il riquadro delle informazioni sull'album e visualizza la pagina Web specificata **dall'attributo URL** dell'elemento **AlbumInfo** del documento ServiceInfo.

Windows Media Player aggiunge una stringa di query all'URL per fornire informazioni al negozio online sul contenuto richiesto dall'utente. La stringa di query include attributi come **Title,** **Album** e **Artist,** che il negozio online può usare per determinare l'album corretto da visualizzare. La documentazione di riferimento per **l'elemento AlbumInfo** fornisce l'elenco completo degli attributi della stringa di query e delle relative descrizioni.

## <a name="guidelines-for-album-info"></a>Linee guida per le informazioni sull'album

Quando si crea la pagina Web delle informazioni sull'album, usare le linee guida seguenti:

-   La pagina deve identificare chiaramente il negozio online che fornisce le informazioni. A tale scopo, ad esempio, è possibile visualizzare in primo piano il logo.
-   La pagina deve includere un collegamento all'informativa sulla privacy dell'azienda.
-   Evitare lo spostamento tra le pagine all'interno della funzionalità di informazioni sull'album, quando possibile. È consigliabile passare al negozio online per la maggior parte delle attività.
-   È consigliabile fornire informazioni preziose senza richiedere all'utente di installare programmi o accedere al negozio online.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sui negozi online di tipo 2**](about-type-2-online-stores.md)
</dt> <dt>

[**Elemento AlbumInfo**](albuminfo-element.md)
</dt> </dl>

 

 




