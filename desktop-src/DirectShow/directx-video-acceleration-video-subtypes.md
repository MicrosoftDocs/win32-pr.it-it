---
description: I sottotipi seguenti vengono usati dai decodificatori che usano DirectX Video Acceleration (DXVA).
ms.assetid: 031b076b-cdfa-407f-8efa-391bce3075ef
title: Sottotipi video di accelerazione video DirectX (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9a2197d504929e001e07fb1ac107dbd7b13b1f443e43ec8ed90232372b08f69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016149"
---
# <a name="directx-video-acceleration-video-subtypes"></a>Sottotipi video di accelerazione video DirectX

I sottotipi seguenti vengono usati dai decodificatori che usano DirectX Video Acceleration (DXVA). AI44 e IA44 sono superfici con un valore di bit per pixel pari a 8. Sono presenti 4 bit di I e 4 bit di *un oggetto*. *I* rappresenta un indice in una tavolozza YUV a 16 voci. *Un* oggetto rappresenta 4 bit di informazioni sulla trasparenza (noti anche come per pixel-alfa). Di conseguenza, le superfici AI44 e IA44 consentono 16 colori diversi con 16 valori di trasparenza diversi o 256 rappresentazioni in pixel diverse. Con AI44 il valore alfa viene archiviato nell'hi-nibble, in IA44 l'alfa viene archiviato nel lo-nibble. Entrambi i formati sono molto utili per le immagini di immagini secondarie DVD e le immagini Line21 e Teletext. Microsoft preferisce la versione AI44 perché è leggermente più semplice generare testo usando questo formato.

| Subtype            | Descrizione                                                 |
|--------------------|-------------------------------------------------------------|
| MEDIASUBTYPE \_ AI44 | Per immagini secondarie e sovrimpressione di testo. Vedere la descrizione precedente. |
| MEDIASUBTYPE \_ IA44 | Per immagini secondarie e sovrimpressione di testo. Vedere la descrizione precedente. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sottotipi video](video-subtypes.md)
</dt> </dl>

 

 




