---
title: Usare QueryService per recuperare un'interfaccia nativa per un oggetto IAccessible
description: Gli sviluppatori di server possono utilizzare questa tecnica per esporre un puntatore a un nodo di documento personalizzato per un oggetto IAccessible. Si presuppone che gli oggetti IAccessible siano già esposti. Questa tecnica consente ai client di ottenere un oggetto personalizzato da un oggetto IAccessible.
ms.assetid: aaa0e840-f8c2-4f3d-9d97-1910f00c1041
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29d971462154eb12789a74e8cc6edb5aed68c84b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047040"
---
# <a name="use-queryservice-to-retrieve-a-native-interface-for-an-iaccessible-object"></a>Usare QueryService per recuperare un'interfaccia nativa per un oggetto IAccessible

Gli sviluppatori di server possono utilizzare questa tecnica per esporre un puntatore a un nodo di documento personalizzato per un oggetto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Si presuppone che gli oggetti **IAccessible** siano già esposti. Questa tecnica consente ai client di ottenere un oggetto personalizzato da un oggetto **IAccessible** .

**Per esporre un modello a oggetti nativo per un IAccessible (Server)**

1.  Aggiunta del supporto per l'interfaccia **IServiceProvider** nell'oggetto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .
2.  Definire un GUID che rappresenta la funzionalità di ottenimento dell'interfaccia personalizzata da oggetti [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Questa operazione è denominata ID del servizio. È possibile utilizzare GUIDGEN.EXE per generare un ID servizio o riutilizzare l'ID di interfaccia se si dispone di un'interfaccia personalizzata.
3.  Implementare il metodo **IServiceProvider:: QueryService** in modo che restituisca un puntatore all'interfaccia personalizzata quando viene chiamato con l'ID del servizio definito in precedenza in questa procedura. **QueryService** deve restituire **null** per tutti gli altri valori ID del servizio.
4.  Pubblicare l'ID del servizio in modo che i client possano usarlo.

I client possono utilizzare questa funzionalità per ottenere un puntatore all'oggetto personalizzato da un oggetto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .

**Per ottenere un puntatore a un oggetto personalizzato da un IAccessible (client)**

1.  Chiamare [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))(IID \_ IServiceProvider) su un puntatore di interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per ottenere un puntatore a interfaccia **IServiceProvider** .
2.  Chiamare **IServiceProvider:: QueryService** con l'ID del servizio pubblicato per ottenere un puntatore all'oggetto personalizzato per [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).
3.  Rilasciare l'interfaccia **IServiceProvider** se non è più necessaria.

Per essere utilizzabile tra più processi, è possibile che i server debbano registrare l'interfaccia restituita con Component Object Model (COM).

Questa tecnica viene utilizzata da Microsoft Internet Explorer 4,0 e versioni successive. Consente ai client di ottenere un puntatore a interfaccia **IHTMLElement2** che corrisponde a un oggetto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .

 

 