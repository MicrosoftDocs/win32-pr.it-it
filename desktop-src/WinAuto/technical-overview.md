---
title: Panoramica tecnica
description: Microsoft Active Accessibility migliora il modo in cui gli strumenti di accessibilità (programmi specializzati che consentono agli utenti con disabilità di usare i computer in modo più efficace) funzionano con le applicazioni eseguite in Microsoft Windows.
ms.assetid: d71ef40e-4c58-4ee6-8909-04ff4f8d20d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69f3931c6a69e9b8caed849942424039178a7884
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712946"
---
# <a name="technical-overview"></a><span data-ttu-id="c6b6a-103">Panoramica tecnica</span><span class="sxs-lookup"><span data-stu-id="c6b6a-103">Technical Overview</span></span>

<span data-ttu-id="c6b6a-104">Microsoft Active Accessibility migliora il modo in cui gli strumenti di accessibilità (programmi specializzati che consentono agli utenti con disabilità di usare i computer in modo più efficace) funzionano con le applicazioni eseguite in Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c6b6a-104">Microsoft Active Accessibility improves the way accessibility aids (specialized programs that help people with disabilities use computers more effectively) work with applications running on Microsoft Windows.</span></span>

<span data-ttu-id="c6b6a-105">Microsoft Active Accessibility si basa sul Component Object Model (COM), sviluppato da Microsoft ed è uno standard di settore che definisce un modo comune per la comunicazione tra le applicazioni e i sistemi operativi.</span><span class="sxs-lookup"><span data-stu-id="c6b6a-105">Microsoft Active Accessibility is based on the Component Object Model (COM), which was developed by Microsoft and is an industry standard that defines a common way for applications and operating systems to communicate.</span></span> <span data-ttu-id="c6b6a-106">Microsoft Active Accessibility è costituito dai componenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="c6b6a-106">Microsoft Active Accessibility consists of the following components:</span></span>

-   <span data-ttu-id="c6b6a-107">Interfaccia COM [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), che espone informazioni sugli elementi dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="c6b6a-107">The COM interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), which exposes information about UI elements.</span></span> <span data-ttu-id="c6b6a-108">**IAccessible** dispone inoltre di proprietà e metodi per ottenere informazioni e modificare tale elemento dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="c6b6a-108">**IAccessible** also has properties and methods for obtaining information about and manipulating that UI element.</span></span>
-   <span data-ttu-id="c6b6a-109">WinEvents, un sistema di eventi che consente ai server di notificare ai client quando un oggetto accessibile viene modificato.</span><span class="sxs-lookup"><span data-stu-id="c6b6a-109">WinEvents, an event system that allows servers to notify clients when an accessible object changes.</span></span>
-   <span data-ttu-id="c6b6a-110">Oleacc.dll, un supporto o una DLL di run-time.</span><span class="sxs-lookup"><span data-stu-id="c6b6a-110">Oleacc.dll, a support or run-time DLL.</span></span>

<span data-ttu-id="c6b6a-111">Microsoft Active Accessibility DLL, Oleacc.dll, è costituito dai componenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="c6b6a-111">The Microsoft Active Accessibility DLL, Oleacc.dll, consists of the following components:</span></span>

-   <span data-ttu-id="c6b6a-112">Funzioni che consentono ai client di richiedere un puntatore a interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) (ad esempio, [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)).</span><span class="sxs-lookup"><span data-stu-id="c6b6a-112">Functions that allow clients to request an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer (for example, [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)).</span></span>
-   <span data-ttu-id="c6b6a-113">Funzioni che consentono ai server di restituire un puntatore di interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) a un client, ad esempio [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject).</span><span class="sxs-lookup"><span data-stu-id="c6b6a-113">Functions that allow servers to return an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer to a client (for example, [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)).</span></span>
-   <span data-ttu-id="c6b6a-114">Funzioni per ottenere il testo localizzato per il ruolo e i codici di stato (ad esempio, [**GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) e [**GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta)).</span><span class="sxs-lookup"><span data-stu-id="c6b6a-114">Functions for getting localized text for the role and state codes (for example, [**GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) and [**GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta)).</span></span>
-   <span data-ttu-id="c6b6a-115">Alcune funzioni helper ([**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren)).</span><span class="sxs-lookup"><span data-stu-id="c6b6a-115">Some helper functions ([**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren)).</span></span>
-   <span data-ttu-id="c6b6a-116">Codice che fornisce l'implementazione predefinita di [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per i controlli utente e COMCTL standard.</span><span class="sxs-lookup"><span data-stu-id="c6b6a-116">Code that provides the default implementation of [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) for standard USER and COMCTL controls.</span></span> <span data-ttu-id="c6b6a-117">Poiché queste implementano **IAccessible** per conto dei controlli di sistema, sono note come *proxy*.</span><span class="sxs-lookup"><span data-stu-id="c6b6a-117">Because these implement **IAccessible** on behalf of the system controls, they are known as *proxies*.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c6b6a-118">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="c6b6a-118">In this section</span></span>

-   [<span data-ttu-id="c6b6a-119">Funzionamento di Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="c6b6a-119">How Active Accessibility Works</span></span>](how-active-accessibility-works.md)
-   [<span data-ttu-id="c6b6a-120">Nozioni di base Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="c6b6a-120">Active Accessibility Basics</span></span>](active-accessibility-basics.md)
-   [<span data-ttu-id="c6b6a-121">Linee guida sul server</span><span class="sxs-lookup"><span data-stu-id="c6b6a-121">Server Guidelines</span></span>](server-guidelines.md)
-   [<span data-ttu-id="c6b6a-122">Linee guida sui client</span><span class="sxs-lookup"><span data-stu-id="c6b6a-122">Client Guidelines</span></span>](client-guidelines.md)
-   [<span data-ttu-id="c6b6a-123">Linee guida per COM e Unicode</span><span class="sxs-lookup"><span data-stu-id="c6b6a-123">COM and Unicode Guidelines</span></span>](com-and-unicode-guidelines.md)

 

 




