---
title: Come Active Accessibility espone Interfaccia utente elementi
description: Microsoft Active Accessibility crea un oggetto proxy per ogni elemento dell'interfaccia utente esposto.
ms.assetid: 64aa8fac-cea7-4466-ae34-2760956c296b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4260788cc37aa6d4a33fcccb68a51fb61833d753c98ba4ae5dcff89f0d18cec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994161"
---
# <a name="how-active-accessibility-exposes-user-interface-elements"></a>Come Active Accessibility espone Interfaccia utente elementi

Microsoft Active Accessibility crea un *oggetto proxy* per ogni elemento dell'interfaccia utente esposto. Un oggetto proxy funge da intermediario tra l'utilità client e l'elemento dell'interfaccia utente. Lo scopo dell'oggetto proxy è monitorare l'intervallo di vita dell'elemento dell'interfaccia utente e implementare le proprietà e i metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per conto dell'elemento dell'interfaccia utente. Anche gli sviluppatori di server che creano controlli personalizzati o altri elementi personalizzati dell'interfaccia utente devono creare oggetti proxy. Per altre informazioni, vedere [Creazione di oggetti proxy.](creating-proxy-objects.md)

Quando Microsoft Active Accessibility crea un oggetto per esporre un controllo predefinito o comune, in realtà crea almeno due oggetti: uno per il controllo e uno per la finestra che circonda il controllo. Nella maggior parte dei casi, queste finestre padre hanno la proprietà [Role](role-property.md) di [**ROLE SYSTEM \_ \_ WINDOW**](object-roles.md) e hanno la stessa proprietà [Name](name-property.md) e lo stesso nome della classe della finestra del controllo. Le informazioni sul controllo che i client comunicano agli utenti finali sono contenute nell'oggetto creato da Microsoft Active Accessibility per esporre il controllo, non nell'oggetto padre che espone la finestra che circonda il controllo.

Per ulteriori informazioni, vedere gli argomenti seguenti.

-   [Screening Out Unnecessary Objects](screening-out-unnecessary-objects.md)
-   [Specifica della proprietà Name](providing-the-name-property.md)
-   [Assicurarsi che gli elementi dell'interfaccia utente siano denominati correttamente](ensure-that-ui-elements-are-named-correctly.md)
-   [Elementi Interfaccia utente non supportati](unsupported-user-interface-elements.md)

 

 




