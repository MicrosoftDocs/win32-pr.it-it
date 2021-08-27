---
description: L'oggetto InkOverlay può essere associato a un controllo finestra e viene usato per abilitare la funzionalità input penna di base.
ms.assetid: c15d80dc-0cbf-48a2-9f5d-d94d521b1a8c
title: Cancellazione tramite l'oggetto InkOverlay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb6d95e7939bc53c534d3bfc9a542e40b95fbce05234000e24b107f0f2625eae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110941"
---
# <a name="erasing-by-using-the-inkoverlay-object"></a>Cancellazione tramite l'oggetto InkOverlay

[**L'oggetto InkOverlay**](inkoverlay-class.md) può essere collegato a un controllo finestra e viene usato per abilitare la funzionalità input penna di base. È possibile usare **l'oggetto InkOverlay** per cancellare l'input penna impostando la [**proprietà EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) su **Delete.** È quindi possibile impostare la [**proprietà EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) su **Stroke** o **Point** membri di [**InkOverlayEraserMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode). **L'impostazione della proprietà EraserMode** **su Stroke** cancella interi tratti. Se si **imposta la proprietà EraserMode** **su Point,** l'input penna passato dal cursore viene cancellato.

 

 



