---
title: Conversione delle coordinate degli eventi
description: Conversione delle coordinate degli eventi
ms.assetid: e7de8af1-a409-4140-9e85-e035bd583912
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 843c2e5a3f978f405a3c126ef6a246024b55ccd2f73fbf86a8eed285b6181169
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993141"
---
# <a name="event-coordinate-translation"></a>Conversione delle coordinate degli eventi

La specifica 96 per i controlli richiede che le coordinate passate per gli eventi generati dal controllo cambino da HIMETRIC a essere basate sui punti. Questa modifica porta il passaggio dell'evento delle coordinate in linea con le proprietà e i metodi e pertanto la traslazione delle coordinate non è più responsabilità del contenitore. Ciò genera alcuni problemi di compatibilità in cui un controllo genera eventi usando una base di coordinate non prevista. Questo dovrebbe essere solo un problema per cui un contenitore di controlli 96 ospita un controllo precedente alla versione 96, come indicato di seguito:

-   Quando un contenitore precedente alla 96 ospita un controllo 96, il controllo presenterà le coordinate dell'evento come punti, ciò non dovrebbe causare problemi al contenitore perché il contenitore deve riconoscere il tipo di parametro.
-   Quando un contenitore 96 ospita un controllo precedente al 96, il controllo presenterà al contenitore le coordinate e si aspetta che il contenitore eserciti la traduzione necessaria. Tuttavia, il contenitore 96 si aspetta che un controllo sia conforme alla specifica dei 96 controlli e presenti le coordinate come punti. Il controllo usa il [**metodo TransformCoords**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-transformcoords) nell'interfaccia [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) fornita dal contenitore allo stesso modo delle proprietà e dei metodi per ottenere questo risultato.

Di conseguenza, l'utente di un contenitore 96 che ospita controlli pre-96 dovrà tenere presente che potrebbe essere necessaria un'ulteriore conversione delle coordinate quando vengono generati eventi.

 

 




