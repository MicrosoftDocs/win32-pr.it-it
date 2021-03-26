---
description: Per creare una bitmap, usare la funzione CreateBitmap, CreateBitmapIndirect o CreateCompatibleBitmap, CreateDIBitmap e CreateDiscardableBitmap.
ms.assetid: 313072fc-68c9-4ece-95bb-2748ccbd7f57
title: Creazione di bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d00a0bc5a39d1b5e6053a34a87c28d6792a42b0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226713"
---
# <a name="bitmap-creation"></a>Creazione di bitmap

Per creare una bitmap, usare la funzione [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap), [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect)o [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) , [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)e [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap).

Queste funzioni consentono di specificare la larghezza e l'altezza, in pixel, della bitmap. La funzione [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) e [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect) consente inoltre di specificare il numero di piani di colore e il numero di bit necessari per identificare il colore. D'altra parte, le funzioni [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) e [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap) usano un contesto di dispositivo specifico per ottenere il numero di piani di colore e il numero di bit necessari per identificare il colore.

La funzione [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap) crea una bitmap dipendente dal dispositivo da una bitmap indipendente dal dispositivo. Contiene una tabella colori che descrive il modo in cui i valori dei pixel corrispondono ai valori dei colori RGB. Per altre informazioni, vedere [bitmap dipendenti dal dispositivo](device-dependent-bitmaps.md) e [bitmap indipendenti dal dispositivo](device-independent-bitmaps.md).

Dopo la creazione della bitmap, non è possibile modificarne le dimensioni, il numero di piani di colore o il numero di bit necessari per identificare il colore.

Quando non è più necessaria una bitmap, chiamare la funzione [**DeleteObject**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject) per eliminarla.

 

 



