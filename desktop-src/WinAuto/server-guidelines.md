---
title: Linee guida sul server
description: Affinché Microsoft Active Accessibility funzioni come previsto, i server devono fornire informazioni sull'accessibilità ai client.
ms.assetid: 88be4bae-fdeb-467c-b5b1-19f2adc0575d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 344721428c94e2ea3d9e9ff78e194851ba9304db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395510"
---
# <a name="server-guidelines"></a><span data-ttu-id="f8596-103">Linee guida sul server</span><span class="sxs-lookup"><span data-stu-id="f8596-103">Server Guidelines</span></span>

<span data-ttu-id="f8596-104">Affinché Microsoft Active Accessibility funzioni come previsto, i server devono fornire informazioni sull'accessibilità ai client.</span><span class="sxs-lookup"><span data-stu-id="f8596-104">For Microsoft Active Accessibility to work as designed, servers must provide accessibility information to clients.</span></span>

<span data-ttu-id="f8596-105">Per implementare [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), è necessario che gli sviluppatori di server seguano questo processo di base.</span><span class="sxs-lookup"><span data-stu-id="f8596-105">To implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), server developers must follow this basic process.</span></span>

1.  <span data-ttu-id="f8596-106">Creare oggetti accessibili implementando le proprietà e i metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per gli elementi dell'interfaccia utente personalizzati e per il client dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f8596-106">Create accessible objects by implementing the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods for your custom user interface elements and for your application's client.</span></span> <span data-ttu-id="f8596-107">Assicurarsi di fornire un'interfaccia duale che supporti sia **IAccessible** che [**IDispatch**](idispatch-interface.md) in modo che i client scritti in Microsoft Visual Basic e vari linguaggi di scripting possano ottenere informazioni sugli oggetti.</span><span class="sxs-lookup"><span data-stu-id="f8596-107">Be sure to provide a dual interface that supports both **IAccessible** and [**IDispatch**](idispatch-interface.md) so that clients written in Microsoft Visual Basic and various scripting languages can get information about the objects.</span></span>
2.  <span data-ttu-id="f8596-108">Chiamare [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) per notificare ai client le modifiche apportate agli elementi dell'interfaccia utente personalizzata.</span><span class="sxs-lookup"><span data-stu-id="f8596-108">Call [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) to notify clients of changes to your custom user interface elements.</span></span>
3.  <span data-ttu-id="f8596-109">Gestire [**WM \_ GetObject**](wm-getobject.md) per fornire l'accesso agli oggetti accessibili.</span><span class="sxs-lookup"><span data-stu-id="f8596-109">Handle [**WM\_GETOBJECT**](wm-getobject.md) to provide access to your accessible objects.</span></span>

<span data-ttu-id="f8596-110">Per suggerimenti e linee guida per la progettazione di oggetti accessibili, vedere [la guida per gli sviluppatori per i server Active Accessibility](developer-s-guide-for-active-accessibility-servers.md).</span><span class="sxs-lookup"><span data-stu-id="f8596-110">For suggestions and guidelines for designing accessible objects, see [Developer's Guide for Active Accessibility Servers](developer-s-guide-for-active-accessibility-servers.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f8596-111">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="f8596-111">In this section</span></span>

-   [<span data-ttu-id="f8596-112">Modalità di implementazione degli ID figlio da server</span><span class="sxs-lookup"><span data-stu-id="f8596-112">How Servers Implement Child IDs</span></span>](how-servers-implement-child-ids.md)

 

 




