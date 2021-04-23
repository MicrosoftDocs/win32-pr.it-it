---
description: Questa proprietà viene usata per segnalare quale versione del set di proprietà Rate Change deve essere usata dal decodificatore.
ms.assetid: 49d1bfda-749b-4614-9a75-1f76fa8b320d
title: AM_RATE_UseRateVersion proprietà (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dd33ef96c50ecc3da0711f08f0c7ffbf0a20825
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910219"
---
# <a name="am_rate_userateversion-property"></a>Proprietà \_ Am RATE \_ UseRateVersion

Questa proprietà viene usata per segnalare quale versione del set di proprietà Rate Change deve essere usata dal decodificatore. Il valore è di **tipo WORD.** Il byte più significativo contiene il numero di versione secondaria e il byte meno significativo contiene il byte meno significativo. La versione 1.1 viene quindi segnalata con il valore 0x0101.

Se il decodificatore non supporta la versione specificata, dovrebbe non riuscire la chiamata a [**IKsPropertySet::Set**](ikspropertyset-set.md) e restituire E \_ NOINTERFACE. Se il filtro di origine non imposta la versione, per impostazione predefinita il decodificatore deve essere la versione 1.0.



| Label | Valore |
|-------------------|-------------------------------|
| GUID set di proprietà | AM \_ KSPROPSETID \_ TSRateChange |
| ID proprietà       | AM \_ RATE \_ UseRateVersion      |
| Tipo di dati         | **WORD**                      |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Rate Change Property Set**](rate-change-property-set.md)
</dt> </dl>

 

 




