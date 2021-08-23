---
description: Valore che definisce il sistema di misurazione per un valore di profondità in un fotogramma video.
ms.assetid: 7BFA846B-E614-4117-A196-298E065CB7F8
title: MF_MT_DEPTH_MEASUREMENT attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a292e5a96cec7490917ef0bb897a9a7a67dd303d29692bf6db5ff58e1d4388c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119605802"
---
# <a name="mf_mt_depth_measurement-attribute"></a>Attributo MF \_ MT \_ DEPTH \_ MEASUREMENT

\[Alcune informazioni riguardano prodotti pre-rilasciati che possono essere modificati in modo sostanziale prima che venga rilasciato commercialmente. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Valore che definisce il sistema di misurazione per un valore di profondità in un fotogramma video.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Questo valore è un membro [**\_ dell'enumerazione MFDepthMeasurement**](/windows/win32/api/mfapi/ne-mfapi-mfdepthmeasurement)

Se questo attributo non è presente, si presuppone che sia **DistanceToFocalPlane**. La distanza dal piano focale è in genere più facile da usare in un sistema di coordinate Euclidian 3D.

![Illustrazione di distancetofocalplane](images/distance-to-focal-plane.png)

La distanza dal formato del centro focale è in genere dati non elaborati dal sensore, ad esempio l'ora delle fotocamere di volo.

![Illustrazione di distancetoopticalcenter](images/distance-to-optical-center.png)

Le fotocamere di profondità non possono percepire la profondità di tutti i pixel. Quando l'attendibilità di un pixel è bassa, a causa di materiale, occlusione o non compreso nell'intervallo, il valore di profondità su tale pixel può non essere valido.

Quando il valore di un pixel di profondità è 0, il pixel non è valido.

Alcune fotocamere di profondità collegano metadati maschera di bit per ogni pixel oltre al valore di profondità per rappresentare il motivo per cui la profondità del pixel non è valida, a causa di materiale, occlusione o non compreso nell'intervallo e così via. È consigliabile evitare di associare metadati di questo tipo come valori di profondità dei bit, perché in genere causano difficoltà quando si usano tali valori in pixel shader. Invece. È consigliabile usare un buffer immagine a 8 bit separato con la stessa risoluzione e associarlo come attributo di [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample). Questi metadati variano per ogni fornitore di fotocamera e non sono standardizzati dalla piattaforma. È consigliabile usare 16 bit completi per il valore di profondità per semplificare l'elaborazione a valle e usare un valore fisso, ad esempio 0 per l'invalidazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1709 \[\]<br/>                          |
| Server minimo supportato<br/> | Windows Server, solo app desktop versione 1709 \[\]<br/>                      |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



 

 




