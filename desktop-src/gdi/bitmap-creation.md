---
description: Per creare una bitmap, usare la funzione CreateBitmap, CreateBitmapIndirect o CreateCompatibleBitmap, CreateDIBitmap e CreateDiscardableBitmap.
ms.assetid: 313072fc-68c9-4ece-95bb-2748ccbd7f57
title: Creazione di bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db37dd14f8be47ebf93c7ee7f586c54c2e55ea900402d9c255a3196987aaed43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038259"
---
# <a name="bitmap-creation"></a>Creazione di bitmap

Per creare una bitmap, usare la funzione [**CreateBitmap,**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect)o [**CreateCompatibleBitmap,**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)e [**CreateDiscardableBitmap.**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap)

Queste funzioni consentono di specificare la larghezza e l'altezza, in pixel, della bitmap. La [**funzione CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) e [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect) consentono anche di specificare il numero di piani colori e il numero di bit necessari per identificare il colore. D'altra parte, le funzioni [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) e [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap) usano un contesto di dispositivo specificato per ottenere il numero di piani di colore e il numero di bit necessari per identificare il colore.

La [**funzione CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap) crea una bitmap dipendente dal dispositivo da una bitmap indipendente dal dispositivo. Contiene una tabella dei colori che descrive in che modo i valori dei pixel corrispondono ai valori di colore RGB. Per altre informazioni, vedere [Bitmap dipendenti dal dispositivo e](device-dependent-bitmaps.md) Bitmap indipendenti dal [dispositivo.](device-independent-bitmaps.md)

Dopo aver creato la bitmap, non è possibile modificarne le dimensioni, il numero di piani colori o il numero di bit necessari per identificare il colore.

Quando una bitmap non è più necessaria, chiamare [**la funzione DeleteObject**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject) per eliminarla.

 

 



