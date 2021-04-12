---
title: Esposizione di informazioni aggiuntive non coperte dall'interfaccia IAccessible
description: A seconda dei prodotti, gli sviluppatori di server potrebbero dover esporre informazioni o funzionalità oltre al supporto di Microsoft Active Accessibility.
ms.assetid: c45009ca-6be3-4645-9097-36671a41dfce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3834c60de8f18fd5ec0719919a1cd79e22f451e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338663"
---
# <a name="exposing-additional-information-not-covered-by-iaccessible-interface"></a>Esposizione di informazioni aggiuntive non coperte dall'interfaccia IAccessible

A seconda dei prodotti, gli sviluppatori di server potrebbero dover esporre informazioni o funzionalità oltre al supporto di Microsoft Active Accessibility. In tal caso, collaborare con i fornitori di Assistive Technology (client) per assicurarsi che aggiungano il supporto per le funzionalità.

Non tentare di estendere l'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Non è possibile modificare le interfacce una volta pubblicate. Per esporre informazioni aggiuntive, utilizzare un'interfaccia personalizzata ed esporla utilizzando una delle tecniche seguenti:

-   [Uso \_ di ObjID NATIVEOM per esporre un'interfaccia del modello a oggetti nativa per una finestra](using-objid-nativeom-to-expose-a-native-object-model-interface-for-a-window.md)
-   [Utilizzo di QueryService per esporre un'interfaccia del modello a oggetti nativo per un oggetto IAccessible](using-queryservice-to-expose-a-native-object-model-interface-for-an-iaccessible-object.md)

Si noti che l'obiettivo dell'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) è disporre di un'interfaccia ben definita utilizzata da server e client. Prima di esporre interfacce personalizzate, assicurarsi di esporre quante più informazioni possibile tramite **IAccessible**.

Non è possibile utilizzare [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per esporre interfacce personalizzate. Usare **IServiceProvider:: QueryService** come descritto nelle procedure seguenti.

 

 