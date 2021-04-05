---
description: L'oggetto InkOverlay può essere collegato a un controllo finestra e viene usato per abilitare la funzionalità di input penna di base.
ms.assetid: c15d80dc-0cbf-48a2-9f5d-d94d521b1a8c
title: Cancellazione tramite l'oggetto InkOverlay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cf85926f3566340cbde0d3202f3485e7c54cccf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751914"
---
# <a name="erasing-by-using-the-inkoverlay-object"></a><span data-ttu-id="33327-103">Cancellazione tramite l'oggetto InkOverlay</span><span class="sxs-lookup"><span data-stu-id="33327-103">Erasing by Using the InkOverlay Object</span></span>

<span data-ttu-id="33327-104">L'oggetto [**InkOverlay**](inkoverlay-class.md) può essere collegato a un controllo finestra e viene usato per abilitare la funzionalità di input penna di base.</span><span class="sxs-lookup"><span data-stu-id="33327-104">The [**InkOverlay**](inkoverlay-class.md) object can be attached to a window control and is used to enable basic ink capability.</span></span> <span data-ttu-id="33327-105">È possibile utilizzare l'oggetto **InkOverlay** per cancellare l'input penna impostando la proprietà [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) uguale a **Delete**.</span><span class="sxs-lookup"><span data-stu-id="33327-105">You can use the **InkOverlay** object to erase ink by setting the [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) property equal to **Delete**.</span></span> <span data-ttu-id="33327-106">È quindi possibile impostare la proprietà [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) sui membri **Stroke** o **Point** di [**InkOverlayEraserMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode).</span><span class="sxs-lookup"><span data-stu-id="33327-106">You can then set the [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) property to either the **Stroke** or **Point** members of [**InkOverlayEraserMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode).</span></span> <span data-ttu-id="33327-107">L'impostazione della proprietà **EraserMode** su **Stroke** Cancella tutti i tratti.</span><span class="sxs-lookup"><span data-stu-id="33327-107">Setting the **EraserMode** property to **Stroke** erases entire strokes.</span></span> <span data-ttu-id="33327-108">Se si imposta la proprietà **EraserMode** su **Point** , viene cancellato l'input penna su cui il cursore viene spostato.</span><span class="sxs-lookup"><span data-stu-id="33327-108">Setting the **EraserMode** property to **Point** erases the ink that the cursor passes over.</span></span>

 

 



