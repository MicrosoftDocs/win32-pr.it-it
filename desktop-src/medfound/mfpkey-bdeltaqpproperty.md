---
description: Specifica l'incremento Delta tra il quantizzatore immagine del frame di ancoraggio e il quantizzatore dell'immagine del fotogramma B.
ms.assetid: 8ab9401b-6fed-4178-955f-2e0bf950bf60
title: Proprietà MFPKEY_BDELTAQP (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7ba1ca7d30e17841badeda0312f77471116a8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311584"
---
# <a name="mfpkey_bdeltaqp-property"></a>\_Proprietà BDELTAQP di MFPKEY

Specifica l'incremento Delta tra il quantizzatore immagine del frame di ancoraggio e il quantizzatore dell'immagine del fotogramma B.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCBDeltaQP

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

0

## <a name="remarks"></a>Commenti

Il quantizzatore immagini (QP) è una misurazione della modalità di compressione di un frame. I valori più alti rappresentano rapporti di compressione più elevati. Il QP può essere impostato con incrementi di due punti. Un frame B viene in genere compresso in un QP uguale a o 0,5 superiore rispetto al QP del frame di ancoraggio. Specificando un Delta QP con frame B maggiore di 0, è possibile comprimere i fotogrammi B a un rapporto di compressione ancora superiore.

È possibile impostare la QP Delta del frame B solo in incrementi completi. Questa proprietà deve essere impostata su un valore intero compreso tra 0 e 31. Il valore consigliato è 1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




