---
description: Esegue una query per determinare se l'output video è di definizione standard, video con componente analogico.
ms.assetid: bd4fc5bc-c45d-4228-9759-6300fdfff6a0
title: AM_PROPERTY_COPY_ANALOG_COMPONENT proprietà (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6448bfbcc07be6ca37189c15c7c605887e6d22b3
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910309"
---
# <a name="am_property_copy_analog_component-property"></a>AM \_ PROPERTY \_ COPY \_ ANALOG \_ COMPONENT Property

Esegue una query per determinare se l'output video è di definizione standard, video con componente analogico.



| Label | Valore |
|-------------------|---------------------------------------|
| GUID set di proprietà | AM \_ KSPROPSETID \_ CopyProt             |
| ID proprietà       | AM \_ PROPERTY \_ COPY \_ ANALOG \_ COMPONENT |
| Tipo di dati         | **Ulong**                             |



 

## <a name="remarks"></a>Commenti

Questa proprietà è di sola lettura.

Il valore della proprietà è **TRUE** se l'output video è un video con componente analogico con una risoluzione non superiore a 480p per NTSC o 540p per PAL. In caso contrario, il valore è **FALSE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Set di proprietà protezione copia DVD**](dvd-copy-protection-property-set.md)
</dt> </dl>

 

 




