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
# <a name="erasing-by-using-the-inkoverlay-object"></a>Cancellazione tramite l'oggetto InkOverlay

L'oggetto [**InkOverlay**](inkoverlay-class.md) può essere collegato a un controllo finestra e viene usato per abilitare la funzionalità di input penna di base. È possibile utilizzare l'oggetto **InkOverlay** per cancellare l'input penna impostando la proprietà [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) uguale a **Delete**. È quindi possibile impostare la proprietà [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) sui membri **Stroke** o **Point** di [**InkOverlayEraserMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode). L'impostazione della proprietà **EraserMode** su **Stroke** Cancella tutti i tratti. Se si imposta la proprietà **EraserMode** su **Point** , viene cancellato l'input penna su cui il cursore viene spostato.

 

 



