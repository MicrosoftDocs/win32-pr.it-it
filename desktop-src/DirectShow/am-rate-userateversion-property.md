---
description: Questa proprietà viene utilizzata per segnalare la versione della proprietà rate Change impostata che il decodificatore deve utilizzare.
ms.assetid: 49d1bfda-749b-4614-9a75-1f76fa8b320d
title: Proprietà AM_RATE_UseRateVersion (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ab609d2d38dc28257d13994e6cd464094b714be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330322"
---
# <a name="am_rate_userateversion-property"></a>\_Proprietà rate \_ UseRateVersion

Questa proprietà viene utilizzata per segnalare la versione della proprietà rate Change impostata che il decodificatore deve utilizzare. Il valore è un tipo di **parola** . Il byte di ordine superiore contiene il numero di versione secondario e il byte di ordine inferiore contiene il byte di ordine inferiore. Quindi, la versione 1,1 viene segnalata con il valore 0x0101.

Se il decodificatore non supporta la versione specificata, deve avere esito negativo la chiamata a [**IKsPropertySet:: set**](ikspropertyset-set.md) E restituire e \_ nointerface. Se il filtro di origine non imposta la versione, il decodificatore deve avere come valore predefinito la versione 1,0.



|                   |                               |
|-------------------|-------------------------------|
| GUID set di proprietà | \_TSRateChange KSPROPSETID \_ |
| ID proprietà       | \_Frequenza \_ UseRateVersion      |
| Tipo di dati         | **WORD**                      |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dvdmedia. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Set di proprietà di modifica della frequenza**](rate-change-property-set.md)
</dt> </dl>

 

 




