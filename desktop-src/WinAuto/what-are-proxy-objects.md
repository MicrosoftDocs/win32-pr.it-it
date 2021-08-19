---
title: Che cosa sono gli oggetti proxy
description: Un oggetto proxy funge da intermediario tra il client e un oggetto accessibile. Lo scopo dell'oggetto proxy è monitorare l'intervallo di vita dell'oggetto accessibile e inoltrare le chiamate all'oggetto accessibile solo se non viene eliminato.
ms.assetid: fdd5d44a-1797-47e6-8044-37dde926c18a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caf3625bf048241e4ef28163ed3b8ca7916ccc35cccc12e7eac05b2b9b9c96d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052189"
---
# <a name="what-are-proxy-objects"></a>Che cosa sono gli oggetti proxy?

Un *oggetto proxy* funge da intermediario tra il client e un oggetto accessibile. Lo scopo dell'oggetto proxy è monitorare l'intervallo di vita dell'oggetto accessibile e inoltrare le chiamate all'oggetto accessibile solo se non viene eliminato.

Quando un client chiama una [**proprietà IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per ottenere informazioni su un oggetto, l'oggetto proxy deve controllare se l'oggetto accessibile è ancora disponibile. In caso contrario, l'oggetto proxy passa la richiesta del client all'oggetto accessibile. Se l'oggetto accessibile viene eliminato,ad esempio quando viene chiusa una finestra di dialogo con controlli personalizzati, l'oggetto proxy restituisce un errore. Per indicare che l'oggetto è stato eliminato, è consigliabile che i server restituiranno il codice di errore **CO \_ E \_ OBJNOTCONNECTED** perché questo errore viene restituito da Component Object Model (COM) dopo che un server ha chiamato [CoDisconnectObject](/windows/win32/api/combaseapi/nf-combaseapi-codisconnectobject).

L'oggetto proxy è trasparente per il client. Quando il client chiama [**AccessibleObjectFromEvent,**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)o [**AccessibleObjectFromWindow,**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)riceve un puntatore a [**un'interfaccia IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Tuttavia, quando il client usa questo puntatore per chiamare una delle proprietà o dei metodi **IAccessible,** il codice eseguito si trova all'interno dell'oggetto proxy.

 

 