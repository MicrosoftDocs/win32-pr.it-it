---
title: Identificatore dell'oggetto OBJID_QUERYCLASSNAMEIDX
description: Microsoft Active Accessibility usa l' \_ identificatore di oggetto QUERYCLASSNAMEIDX di ObjID con il \_ messaggio WM GetObject per determinare la classe a cui appartiene un controllo Windows standard o un controllo comune.
ms.assetid: 2167df6d-5df3-40b7-bebe-142f4bd98cd7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba7d73a152380411ef0b230de8f0e3372a6718b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297823"
---
# <a name="the-objid_queryclassnameidx-object-identifier"></a><span data-ttu-id="1946c-103">\_Identificatore oggetto QUERYCLASSNAMEIDX ObjID</span><span class="sxs-lookup"><span data-stu-id="1946c-103">The OBJID\_QUERYCLASSNAMEIDX Object Identifier</span></span>

<span data-ttu-id="1946c-104">Microsoft Active Accessibility usa l'identificatore di oggetto [**\_ QUERYCLASSNAMEIDX di ObjID**](object-identifiers.md) con il messaggio [**WM \_ GetObject**](wm-getobject.md) per determinare la classe a cui appartiene un controllo Windows standard o un controllo comune.</span><span class="sxs-lookup"><span data-stu-id="1946c-104">Microsoft Active Accessibility uses the [**OBJID\_QUERYCLASSNAMEIDX**](object-identifiers.md) object identifier with the [**WM\_GETOBJECT**](wm-getobject.md) message to determine the class to which a standard Windows control or common control belongs.</span></span> <span data-ttu-id="1946c-105">Un controllo risponde a questo messaggio restituendo un valore che Microsoft Active Accessibility esegue il mapping al nome della classe del controllo.</span><span class="sxs-lookup"><span data-stu-id="1946c-105">A control responds to this message by returning a value that Microsoft Active Accessibility maps to the class name of the control.</span></span> <span data-ttu-id="1946c-106">Microsoft Active Accessibility utilizza queste informazioni per fornire supporto per l'accessibilità per i controlli Windows standard e i controlli comuni.</span><span class="sxs-lookup"><span data-stu-id="1946c-106">Microsoft Active Accessibility uses this information to provide accessibility support for standard Windows controls and common controls.</span></span>

<span data-ttu-id="1946c-107">Generalmente, solo i controlli Windows standard e i controlli comuni rispondono all'identificatore di oggetto [**\_ QUERYCLASSNAMEIDX di ObjID**](object-identifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="1946c-107">Generally, only the standard Windows controls and the common controls respond to the [**OBJID\_QUERYCLASSNAMEIDX**](object-identifiers.md) object identifier.</span></span> <span data-ttu-id="1946c-108">Tuttavia, un controllo personalizzato può anche rispondere se include tutte le stesse funzionalità di un controllo Windows standard o di un controllo comune esistente.</span><span class="sxs-lookup"><span data-stu-id="1946c-108">However, a custom control can also respond if it includes all of the same functionality as an existing standard Windows control or common control.</span></span> <span data-ttu-id="1946c-109">In questo modo il controllo personalizzato sarà supportato da uno degli oggetti proxy standard forniti da Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="1946c-109">This enables the custom control to be supported by one of the standard proxy objects provided by Microsoft Active Accessibility.</span></span>

<span data-ttu-id="1946c-110">Per ulteriori informazioni, vedere [Appendice F: valori identificatore oggetto per objid \_ QUERYCLASSNAMEIDX](appendix-f--object-identifier-values-for-objid-queryclassnameidx.md).</span><span class="sxs-lookup"><span data-stu-id="1946c-110">For more information, see [Appendix F: Object Identifier Values for OBJID\_QUERYCLASSNAMEIDX](appendix-f--object-identifier-values-for-objid-queryclassnameidx.md).</span></span>

 

 




