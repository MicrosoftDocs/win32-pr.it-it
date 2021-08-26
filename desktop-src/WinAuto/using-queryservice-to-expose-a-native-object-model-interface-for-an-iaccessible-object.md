---
title: Usare QueryService per recuperare un'interfaccia nativa per un oggetto IAccessible
description: Gli sviluppatori di server possono usare questa tecnica per esporre un puntatore a un nodo di documento personalizzato per un oggetto IAccessible. Si presuppone che si esponga già oggetti IAccessible. Questa tecnica consente ai client di ottenere un oggetto personalizzato da un oggetto IAccessible.
ms.assetid: aaa0e840-f8c2-4f3d-9d97-1910f00c1041
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22c55e503bdda05692b13548d2d63eaeb3246562b4f4e8fc1e8645d25941a7f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098071"
---
# <a name="use-queryservice-to-retrieve-a-native-interface-for-an-iaccessible-object"></a>Usare QueryService per recuperare un'interfaccia nativa per un oggetto IAccessible

Gli sviluppatori di server possono usare questa tecnica per esporre un puntatore a un nodo di documento personalizzato per un [**oggetto IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Si presuppone che si esponga già **oggetti IAccessible.** Questa tecnica consente ai client di ottenere un oggetto personalizzato da un **oggetto IAccessible.**

**Per esporre un modello a oggetti nativo per IAccessible (server)**

1.  Aggiungere il supporto per **l'interfaccia IServiceProvider** [**nell'oggetto IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
2.  Definire un GUID che rappresenta la funzionalità di recupero dell'interfaccia personalizzata da un [**oggetto IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Si tratta di un ID servizio. È possibile usare GUIDGEN.EXE per generare un ID servizio o riusare l'ID interfaccia se si dispone di un'interfaccia personalizzata.
3.  Implementare **il metodo IServiceProvider::QueryService** in modo che restituisca un puntatore all'interfaccia personalizzata quando viene chiamato con l'ID servizio definito in precedenza in questa procedura. **QueryService deve** restituire **NULL per tutti** gli altri valori di ID servizio.
4.  Pubblicare l'ID servizio in modo che i client possano usarlo.

I client possono usare questa funzionalità per ottenere un puntatore all'oggetto personalizzato da un [**oggetto IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

**Per ottenere un puntatore a un oggetto personalizzato da un oggetto IAccessible (client)**

1.  Chiamare [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))(IID IServiceProvider) su un puntatore a interfaccia \_ [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per ottenere un puntatore a interfaccia **IServiceProvider.**
2.  Chiamare **IServiceProvider::QueryService con** l'ID servizio pubblicato per ottenere un puntatore all'oggetto personalizzato per [**IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
3.  Rilasciare **l'interfaccia IServiceProvider** se non è più necessaria.

Per essere utilizzabili tra processi, i server potrebbero dover registrare l'interfaccia restituita con Component Object Model (COM).

Questa tecnica viene usata da Microsoft Internet Explorer 4.0 e versioni successive. Consente ai client di ottenere un puntatore a interfaccia **IHTMLElement2** che corrisponde a un [**oggetto IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

 

 