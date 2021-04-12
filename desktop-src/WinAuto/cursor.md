---
title: Cursor (riferimento all'elemento dell'interfaccia utente MSAA)
description: Un cursore è una piccola immagine il cui percorso sullo schermo è controllato da un dispositivo di puntamento, ad esempio un mouse, una penna o una trackball. Quando l'utente sposta il dispositivo di puntamento, il sistema operativo Windows sposta il cursore.
ms.assetid: ff97d474-7c96-4f89-bc34-2cf320381ce0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff351040d342adccda8cb03d56d91f9dc429074f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328852"
---
# <a name="cursor-msaa-ui-element-reference"></a><span data-ttu-id="dbcd7-104">Cursor (riferimento all'elemento dell'interfaccia utente MSAA)</span><span class="sxs-lookup"><span data-stu-id="dbcd7-104">Cursor (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="dbcd7-105">In questo argomento vengono descritti i cursori ai fini del riferimento all'elemento dell'interfaccia utente MSAA.</span><span class="sxs-lookup"><span data-stu-id="dbcd7-105">This topic describes cursors for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="dbcd7-106">L'uso di cursori in diversi framework dell'interfaccia utente non è descritto qui.</span><span class="sxs-lookup"><span data-stu-id="dbcd7-106">How to use cursors in various UI frameworks is not described here.</span></span> <span data-ttu-id="dbcd7-107">Vedere la documentazione di riferimento sulle API per il Framework dell'interfaccia utente in uso.</span><span class="sxs-lookup"><span data-stu-id="dbcd7-107">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="dbcd7-108">Un cursore è una piccola immagine il cui percorso sullo schermo è controllato da un dispositivo di puntamento, ad esempio un mouse, una penna o una trackball.</span><span class="sxs-lookup"><span data-stu-id="dbcd7-108">A cursor is a small picture whose location on the screen is controlled by a pointing device, such as a mouse, pen, or trackball.</span></span> <span data-ttu-id="dbcd7-109">Quando l'utente sposta il dispositivo di puntamento, il sistema operativo Windows sposta il cursore.</span><span class="sxs-lookup"><span data-stu-id="dbcd7-109">When the user moves the pointing device, the Windows operating system moves the cursor.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="dbcd7-110">Metodi IAccessible</span><span class="sxs-lookup"><span data-stu-id="dbcd7-110">IAccessible Methods</span></span>

<span data-ttu-id="dbcd7-111">Un cursore supporta i seguenti metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="dbcd7-111">A cursor supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="dbcd7-112">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="dbcd7-112">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="dbcd7-113">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="dbcd7-113">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="iaccessible-properties"></a><span data-ttu-id="dbcd7-114">Proprietà IAccessible</span><span class="sxs-lookup"><span data-stu-id="dbcd7-114">IAccessible Properties</span></span>

<span data-ttu-id="dbcd7-115">Un cursore supporta le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) seguenti:</span><span class="sxs-lookup"><span data-stu-id="dbcd7-115">A cursor supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>

-   <span data-ttu-id="dbcd7-116">[**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount): la proprietà **childCount** è zero.</span><span class="sxs-lookup"><span data-stu-id="dbcd7-116">[**get\_accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)—The **ChildCount** property is zero.</span></span>
-   <span data-ttu-id="dbcd7-117">[**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname): gli sviluppatori possono creare cursori personalizzati o usare i cursori predefiniti identificati dall'ID del cursore.</span><span class="sxs-lookup"><span data-stu-id="dbcd7-117">[**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)—Developers can create custom cursors or use the predefined cursors that are identified by their cursor ID.</span></span> <span data-ttu-id="dbcd7-118">La proprietà **Name** del cursore dipende dalla relativa forma ed è una delle seguenti:</span><span class="sxs-lookup"><span data-stu-id="dbcd7-118">The **Name** property of the cursor depends on its shape and is one of the following:</span></span> 

    | <span data-ttu-id="dbcd7-119">Forma del cursore</span><span class="sxs-lookup"><span data-stu-id="dbcd7-119">Cursor shape</span></span>     | <span data-ttu-id="dbcd7-120">Nome</span><span class="sxs-lookup"><span data-stu-id="dbcd7-120">Name</span></span>              |
    |------------------|-------------------|
    | <span data-ttu-id="dbcd7-121">Cursore personalizzato</span><span class="sxs-lookup"><span data-stu-id="dbcd7-121">Custom cursor</span></span>    | <span data-ttu-id="dbcd7-122">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="dbcd7-122">"Unknown"</span></span>         |
    | <span data-ttu-id="dbcd7-123">\_freccia IDC</span><span class="sxs-lookup"><span data-stu-id="dbcd7-123">IDC\_ARROW</span></span>       | <span data-ttu-id="dbcd7-124">"Normal"</span><span class="sxs-lookup"><span data-stu-id="dbcd7-124">"Normal"</span></span>          |
    | <span data-ttu-id="dbcd7-125">IDC \_ IBeam</span><span class="sxs-lookup"><span data-stu-id="dbcd7-125">IDC\_IBEAM</span></span>       | <span data-ttu-id="dbcd7-126">Modifica</span><span class="sxs-lookup"><span data-stu-id="dbcd7-126">"Edit"</span></span>            |
    | <span data-ttu-id="dbcd7-127">\_attesa IDC</span><span class="sxs-lookup"><span data-stu-id="dbcd7-127">IDC\_WAIT</span></span>        | <span data-ttu-id="dbcd7-128">Attendere</span><span class="sxs-lookup"><span data-stu-id="dbcd7-128">"Wait"</span></span>            |
    | <span data-ttu-id="dbcd7-129">IDC \_ incrociato</span><span class="sxs-lookup"><span data-stu-id="dbcd7-129">IDC\_CROSS</span></span>       | <span data-ttu-id="dbcd7-130">Di</span><span class="sxs-lookup"><span data-stu-id="dbcd7-130">"Graphic"</span></span>         |
    | <span data-ttu-id="dbcd7-131">IDC a \_ freccia</span><span class="sxs-lookup"><span data-stu-id="dbcd7-131">IDC\_UPARROW</span></span>     | <span data-ttu-id="dbcd7-132">Fino</span><span class="sxs-lookup"><span data-stu-id="dbcd7-132">"Up"</span></span>              |
    | <span data-ttu-id="dbcd7-133">IDC \_ SIZENWSE</span><span class="sxs-lookup"><span data-stu-id="dbcd7-133">IDC\_SIZENWSE</span></span>    | <span data-ttu-id="dbcd7-134">"Dimensioni NWSE"</span><span class="sxs-lookup"><span data-stu-id="dbcd7-134">"NWSE size"</span></span>       |
    | <span data-ttu-id="dbcd7-135">IDC \_ SIZENESW</span><span class="sxs-lookup"><span data-stu-id="dbcd7-135">IDC\_SIZENESW</span></span>    | <span data-ttu-id="dbcd7-136">"Dimensioni NESW"</span><span class="sxs-lookup"><span data-stu-id="dbcd7-136">"NESW size"</span></span>       |
    | <span data-ttu-id="dbcd7-137">IDC \_ SIZEWE</span><span class="sxs-lookup"><span data-stu-id="dbcd7-137">IDC\_SIZEWE</span></span>      | <span data-ttu-id="dbcd7-138">"Dimensioni orizzontali"</span><span class="sxs-lookup"><span data-stu-id="dbcd7-138">"Horizontal size"</span></span> |
    | <span data-ttu-id="dbcd7-139">IDC \_ SIZENS</span><span class="sxs-lookup"><span data-stu-id="dbcd7-139">IDC\_SIZENS</span></span>      | <span data-ttu-id="dbcd7-140">"Dimensioni verticali"</span><span class="sxs-lookup"><span data-stu-id="dbcd7-140">"Vertical size"</span></span>   |
    | <span data-ttu-id="dbcd7-141">IDC \_ SIZEALL</span><span class="sxs-lookup"><span data-stu-id="dbcd7-141">IDC\_SIZEALL</span></span>     | <span data-ttu-id="dbcd7-142">Spostare</span><span class="sxs-lookup"><span data-stu-id="dbcd7-142">"Move"</span></span>            |
    | <span data-ttu-id="dbcd7-143">\_No IDC</span><span class="sxs-lookup"><span data-stu-id="dbcd7-143">IDC\_NO</span></span>          | <span data-ttu-id="dbcd7-144">Accesso negato</span><span class="sxs-lookup"><span data-stu-id="dbcd7-144">"Forbidden"</span></span>       |
    | <span data-ttu-id="dbcd7-145">IDC \_ APPSTARTING</span><span class="sxs-lookup"><span data-stu-id="dbcd7-145">IDC\_APPSTARTING</span></span> | <span data-ttu-id="dbcd7-146">"Avvio dell'app"</span><span class="sxs-lookup"><span data-stu-id="dbcd7-146">"App start"</span></span>       |
    | <span data-ttu-id="dbcd7-147">Guida di IDC \_</span><span class="sxs-lookup"><span data-stu-id="dbcd7-147">IDC\_HELP</span></span>        | <span data-ttu-id="dbcd7-148">Aiuto</span><span class="sxs-lookup"><span data-stu-id="dbcd7-148">"Help"</span></span>            |

    

     

-   <span data-ttu-id="dbcd7-149">[**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole): la proprietà **Role** è [**il \_ \_ cursore del sistema Role**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="dbcd7-149">[**get\_accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)—The **Role** property is [**ROLE\_SYSTEM\_CURSOR**](object-roles.md).</span></span>
-   <span data-ttu-id="dbcd7-150">[**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate): la proprietà **state** è una combinazione di uno o più dei [valori](object-state-constants.md)seguenti:</span><span class="sxs-lookup"><span data-stu-id="dbcd7-150">[**get\_accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)—The **State** property is a combination of one or more of the following [values](object-state-constants.md):</span></span>

    <span data-ttu-id="dbcd7-151">[**Stato \_ di sistema \_**](object-state-constants.md) di stato invisibile al sistema a \| [ **\_ \_ virgola mobile**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="dbcd7-151">[**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FLOATING**](object-state-constants.md)</span></span>

## <a name="notes"></a><span data-ttu-id="dbcd7-152">Note</span><span class="sxs-lookup"><span data-stu-id="dbcd7-152">Notes</span></span>

-   <span data-ttu-id="dbcd7-153">A differenza di altri elementi dell'interfaccia utente, all'oggetto cursore non è associato un handle di finestra.</span><span class="sxs-lookup"><span data-stu-id="dbcd7-153">Unlike other UI elements, the cursor object does not have an associated window handle.</span></span> <span data-ttu-id="dbcd7-154">Per ottenere l'accesso all'oggetto cursore, i client devono impostare un [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) e attendere la generazione di eventi da parte dell'oggetto cursore.</span><span class="sxs-lookup"><span data-stu-id="dbcd7-154">To obtain access to the cursor object, clients must set a [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) and wait for the cursor object to generate events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dbcd7-155">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dbcd7-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dbcd7-156">IAccessible (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="dbcd7-156">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




