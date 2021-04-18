---
description: I sottotipi seguenti vengono usati dai decodificatori che usano l'accelerazione video DirectX (DXVA).
ms.assetid: 031b076b-cdfa-407f-8efa-391bce3075ef
title: Sottotipi video di accelerazione video DirectX (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0df0f079e795638c6802570c95e2468209a7256
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328477"
---
# <a name="directx-video-acceleration-video-subtypes"></a>Sottotipi video di accelerazione video DirectX

I sottotipi seguenti vengono usati dai decodificatori che usano l'accelerazione video DirectX (DXVA). AI44 e IA44 sono superfici con un valore bits per pixel pari a 8. Sono presenti 4 *bit di I* e 4 bit di. *I* rappresenta un indice in una tavolozza YUV a 16 voci. *Un oggetto* rappresenta 4 bit di informazioni di trasparenza (anche noto come per pixel-alfa). Pertanto, le superfici AI44 e IA44 consentono 16 colori diversi con 16 diversi valori di trasparenza o 256 diverse rappresentazioni di pixel. Con AI44, il Alpha viene archiviato nell'oggetto Hi-sgranocchiate, in IA44 l'alfa viene archiviato nello lo-bocconcino. Entrambi i formati sono molto utili per immagini di sottoimmagine DVD e immagini di Line21 e televideo. Microsoft preferisce la versione AI44 perché è leggermente più semplice generare testo usando questo formato.

| Subtype            | Descrizione                                                 |
|--------------------|-------------------------------------------------------------|
| \_AI44 MEDIASUBTYPE | Per la sovrimpressione di immagini e testo. Vedere la descrizione precedente. |
| \_IA44 MEDIASUBTYPE | Per la sovrimpressione di immagini e testo. Vedere la descrizione precedente. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dshow. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sottotipi video](video-subtypes.md)
</dt> </dl>

 

 




