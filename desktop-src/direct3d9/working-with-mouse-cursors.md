---
description: I metodi del cursore del mouse consentono all'applicazione di specificare un cursore di colore fornendo una superficie che contiene un'immagine.
ms.assetid: 300a8a6f-abcd-49c9-889b-14b12ff5c821
title: Utilizzo dei cursori del mouse (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14855e2d17c9d23f078297840d951b8db338d613
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482413"
---
# <a name="working-with-mouse-cursors-direct3d-9"></a><span data-ttu-id="26573-103">Utilizzo dei cursori del mouse (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="26573-103">Working with Mouse Cursors (Direct3D 9)</span></span>

<span data-ttu-id="26573-104">I metodi del cursore del mouse consentono all'applicazione di specificare un cursore di colore fornendo una superficie che contiene un'immagine.</span><span class="sxs-lookup"><span data-stu-id="26573-104">The mouse cursor methods enable the application to specify a color cursor by providing a surface that contains an image.</span></span> <span data-ttu-id="26573-105">Il sistema garantisce che questo cursore venga aggiornato a metà della frequenza di visualizzazione o superiore se la frequenza dei fotogrammi dell'applicazione è lenta.</span><span class="sxs-lookup"><span data-stu-id="26573-105">The system will ensure that this cursor will be updated at half the display rate or more if the application's frame rate is slow.</span></span> <span data-ttu-id="26573-106">Tuttavia, il cursore non verrà mai aggiornato più di frequente rispetto alla frequenza di aggiornamento dello schermo.</span><span class="sxs-lookup"><span data-stu-id="26573-106">However, the cursor will never be updated more frequently than the display refresh rate.</span></span>

<span data-ttu-id="26573-107">La posizione del cursore del mouse è associata al cursore di sistema, ridimensionata in modo appropriato per la risoluzione spaziale della modalità di visualizzazione corrente, ma può essere spostata in modo esplicito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="26573-107">The mouse cursor position is tied to the system cursor, appropriately scaled for the current display mode spatial resolution, but it can be moved explicitly by the application.</span></span> <span data-ttu-id="26573-108">Questo comportamento è analogo al comportamento del cursore del mouse di sistema supportato dall'API Win32.</span><span class="sxs-lookup"><span data-stu-id="26573-108">This is analogous to the behavior of the Win32 API - supported system mouse cursor.</span></span> <span data-ttu-id="26573-109">Per ulteriori informazioni sull'utilizzo di un cursore del mouse nell'applicazione Direct3D, vedere gli argomenti di riferimento seguenti.</span><span class="sxs-lookup"><span data-stu-id="26573-109">For more information about how to use a mouse cursor in your Direct3D application, see the following reference topics.</span></span>

-   [<span data-ttu-id="26573-110">**IDirect3DDevice9:: ShowCursor**</span><span class="sxs-lookup"><span data-stu-id="26573-110">**IDirect3DDevice9::ShowCursor**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-showcursor)
-   [<span data-ttu-id="26573-111">**IDirect3DDevice9:: SetCursorPosition**</span><span class="sxs-lookup"><span data-stu-id="26573-111">**IDirect3DDevice9::SetCursorPosition**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorposition)
-   [<span data-ttu-id="26573-112">**IDirect3DDevice9:: SetCursorProperties**</span><span class="sxs-lookup"><span data-stu-id="26573-112">**IDirect3DDevice9::SetCursorProperties**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorproperties)

<span data-ttu-id="26573-113">Direct3D garantisce che il mouse sia supportato dalle implementazioni hardware o dal tempo di esecuzione Direct3D che esegue operazioni blitting con accelerazione hardware durante la chiamata di [**IDirect3DDevice9::P inviato nuovamente**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span><span class="sxs-lookup"><span data-stu-id="26573-113">Direct3D ensures that the mouse is supported either by hardware implementations or by the Direct3D run time that performs hardware-accelerated blitting operations when calling [**IDirect3DDevice9::Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span></span>

## <a name="related-topics"></a><span data-ttu-id="26573-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="26573-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26573-115">Suggerimenti per la programmazione</span><span class="sxs-lookup"><span data-stu-id="26573-115">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 
