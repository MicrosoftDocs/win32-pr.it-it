---
title: Che cosa sono gli oggetti proxy
description: Un oggetto proxy funge da intermediario tra il client e un oggetto accessibile. Lo scopo dell'oggetto proxy è monitorare il ciclo di vita dell'oggetto accessibile e inviare le chiamate all'oggetto accessibile solo se non viene eliminato definitivamente.
ms.assetid: fdd5d44a-1797-47e6-8044-37dde926c18a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60d54fb20d677f1a417d633242ddf40c704087f3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338934"
---
# <a name="what-are-proxy-objects"></a>Che cosa sono gli oggetti proxy?

Un oggetto *proxy* funge da intermediario tra il client e un oggetto accessibile. Lo scopo dell'oggetto proxy è monitorare il ciclo di vita dell'oggetto accessibile e inviare le chiamate all'oggetto accessibile solo se non viene eliminato definitivamente.

Quando un client chiama una proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per ottenere informazioni su un oggetto, l'oggetto proxy deve verificare se l'oggetto accessibile è ancora disponibile. In tal caso, l'oggetto proxy passa la richiesta del client all'oggetto accessibile. Se l'oggetto accessibile viene eliminato definitivamente, ad esempio quando una finestra di dialogo con controlli personalizzati viene chiusa, l'oggetto proxy restituisce un errore. Per indicare che l'oggetto è stato eliminato definitivamente, è consigliabile che i server restituiscano il codice di errore **\_ \_ OBJNOTCONNECTED** , perché questo errore viene restituito da Component Object Model (com) dopo che un server chiama [CoDisconnectObject](/windows/win32/api/combaseapi/nf-combaseapi-codisconnectobject).

L'oggetto proxy è trasparente per il client. Quando il client chiama [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)o [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow), riceve un puntatore a un'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Tuttavia, quando il client utilizza questo puntatore per chiamare qualsiasi proprietà o metodo **IAccessible** , il codice eseguito si trova all'interno dell'oggetto proxy.

 

 