---
description: Valore che definisce il sistema di misurazione per un valore di profondità in un frame video.
ms.assetid: 7BFA846B-E614-4117-A196-298E065CB7F8
title: Attributo MF_MT_DEPTH_MEASUREMENT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8be6c06ea09f4017ae65935081eaa81d1ad00cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104560652"
---
# <a name="mf_mt_depth_measurement-attribute"></a>\_Attributo di \_ misurazione della profondità MF mt \_

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Valore che definisce il sistema di misurazione per un valore di profondità in un frame video.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Questo valore è un membro dell'enumerazione [**\_ MFDepthMeasurement**](/windows/win32/api/mfapi/ne-mfapi-mfdepthmeasurement)

Se questo attributo non è presente, si presuppone che sia **DistanceToFocalPlane**. La distanza dal piano focale è in genere più facile da utilizzare in un sistema di coordinate euclideo 3D.

![illustrazione di distancetofocalplane](images/distance-to-focal-plane.png)

Il formato distanza dal centro focale è in genere costituito da dati non elaborati provenienti dal sensore, ad esempio il tempo delle fotocamere.

![illustrazione di distancetoopticalcenter](images/distance-to-optical-center.png)

Le fotocamere con profondità non possono comprendere la profondità di tutti i pixel. Quando la confidenza di un pixel è bassa, a causa di materiale, occlusione o non compreso nell'intervallo e così via, il valore di profondità su tale pixel può non essere valido.

Quando un valore di pixel di profondità è 0, il pixel non è valido.

Alcune fotocamere di profondità allineano i metadati della maschera di maschera per ogni pixel oltre al valore di profondità per rappresentare il motivo per cui la profondità del pixel non è valida, a causa del materiale, dell'occlusione o dell'intervallo e così via. Si consiglia di evitare di alleghiare tali metadati come valori di profondità, perché in genere si verificano difficoltà quando si utilizzano tali valori in pixel shader. Invece. si consiglia di usare un buffer di immagini a 8 bit separato con la stessa risoluzione e di associarlo come attributo di [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample). Tali metadati variano a seconda del fornitore della fotocamera e non sono standardizzati dalla piattaforma. È consigliabile usare 16 bit completi per il valore di profondità per semplificare l'elaborazione a valle e usare un valore fisso, ad esempio 0, per l'invalidamento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1709 \[\]<br/>                          |
| Server minimo supportato<br/> | Windows Server, versione 1709 \[ solo per le app desktop\]<br/>                      |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 




