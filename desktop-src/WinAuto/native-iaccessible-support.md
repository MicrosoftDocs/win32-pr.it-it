---
title: Supporto di IAccessible nativo
description: Oleacc.dll implementa IAccIdentity per conto del \_ client ObjID \ 160, i puntatori dell'interfaccia IAccessible e i relativi elementi figlio immediatamente semplici.
ms.assetid: 98c6d68b-b64d-44d4-93c3-6c7c6732d59d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 606261a642f57c85f3f23a80257b7cdc498b927b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856429"
---
# <a name="native-iaccessible-support"></a><span data-ttu-id="6399b-103">Supporto di IAccessible nativo</span><span class="sxs-lookup"><span data-stu-id="6399b-103">Native IAccessible Support</span></span>

<span data-ttu-id="6399b-104">Oleacc.dll implementa [**IAccIdentity**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) per conto dei puntatori dell'interfaccia  [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) del [**\_ client ObjID**](object-identifiers.md)e dei relativi elementi figlio immediati.</span><span class="sxs-lookup"><span data-stu-id="6399b-104">Oleacc.dll implements [**IAccIdentity**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) on behalf of [**OBJID\_CLIENT**](object-identifiers.md) [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointers and their immediate simple element children.</span></span> <span data-ttu-id="6399b-105">Un puntatore all'interfaccia  **IAccessible** del **\_ client ObjID** viene restituito quando [**WM \_ GetObject**](wm-getobject.md) con *lParam*  =  **objid \_ client** viene inviato a un **HWND**, che rappresenta l'area client della finestra o il controllo nel suo complesso.</span><span class="sxs-lookup"><span data-stu-id="6399b-105">An **OBJID\_CLIENT** **IAccessible** interface pointer is returned when [**WM\_GETOBJECT**](wm-getobject.md) with *lParam* = **OBJID\_CLIENT** is sent to an **HWND**, which represents the client area of the window or the control as a whole.</span></span> <span data-ttu-id="6399b-106">L'elemento padre di un puntatore a interfaccia **IAccessible** di questo tipo ha in genere un ruolo di [**finestra del \_ sistema \_ di ruoli**](object-roles.md) e è l'oggetto **IAccessible** restituito quando **WM \_ GetObject** con *lParam*  =  [**objid \_ finestra**](object-identifiers.md) viene inviato a HWND.</span><span class="sxs-lookup"><span data-stu-id="6399b-106">The parent of such an **IAccessible** interface pointer will typically have a role of [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) and is the **IAccessible** object returned when **WM\_GETOBJECT** with *lParam* = [**OBJID\_WINDOW**](object-identifiers.md) is sent to an hwnd.</span></span>

<span data-ttu-id="6399b-107">Questi puntatori di interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) si verificano in genere quando un proxy Oleacc.dll viene sottoclassato o quando un controllo personalizzato semplice (ad esempio un contenitore **IAccessible** più un livello di elementi figlio di elementi semplici) fornisce un'implementazione **IAccessible** nativa.</span><span class="sxs-lookup"><span data-stu-id="6399b-107">These [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointers typically occur where an Oleacc.dll proxy is subclassed, or where a simple custom control (such as a container **IAccessible** plus one level of simple element children) provides a native **IAccessible** implementation.</span></span>

<span data-ttu-id="6399b-108">Implementazioni [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) native più complesse, ad esempio quando esiste una gerarchia di **IAccessible** o in cui vengono usati gli ID oggetto personalizzati, devono implementare [**IAccIdentity**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) .</span><span class="sxs-lookup"><span data-stu-id="6399b-108">More complicated native [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementations such as where a hierarchy of **IAccessible** s exists or where custom object IDs are used must implement [**IAccIdentity**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) themselves.</span></span>

 

 




