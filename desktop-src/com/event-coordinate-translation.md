---
title: Conversione delle coordinate degli eventi
description: Conversione delle coordinate degli eventi
ms.assetid: e7de8af1-a409-4140-9e85-e035bd583912
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c40a742ead8fc8d7e431c1caa5210f0978168cb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713219"
---
# <a name="event-coordinate-translation"></a>Conversione delle coordinate degli eventi

La specifica 96 per i controlli richiede che le coordinate passate per gli eventi generati dal controllo cambino HIMETRIC in base ai punti. Questa modifica consente di passare gli eventi delle coordinate in linea con proprietà e metodi e quindi la traduzione delle coordinate non è più la responsabilità del contenitore. In questo modo si verificano alcuni problemi di compatibilità in cui un controllo genera eventi usando una base di coordinate non prevista. dovrebbe trattarsi solo di un problema per cui un contenitore di controlli 96 ospita un controllo precedente a 96 precedente, come indicato di seguito:

-   Quando un contenitore precedente a 96 precedente ospita un controllo 96, il controllo presenta le coordinate dell'evento come punti, questo non dovrebbe causare problemi al contenitore poiché il contenitore deve riconoscere il tipo di parametro.
-   Quando un contenitore 96 ospita un controllo precedente a 96, il controllo presenterà il contenitore con le coordinate e si aspetterà che il contenitore debba eseguire una traduzione necessaria. Tuttavia, il contenitore 96 prevede che un controllo sia conforme alla specifica dei controlli 96 e presenti le coordinate come punti. Il controllo Usa il metodo [**TransformCoords**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-transformcoords) sull'interfaccia [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) fornita dal contenitore in modo analogo a quanto accade per le proprietà e i metodi per ottenere questo risultato.

Di conseguenza, l'utente di un contenitore 96 che ospita i controlli precedenti a 96 dovrà tenere presente che, quando vengono attivati gli eventi, potrebbe essere necessaria una conversione aggiuntiva delle coordinate.

 

 




