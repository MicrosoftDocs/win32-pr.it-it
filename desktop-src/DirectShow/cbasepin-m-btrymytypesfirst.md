---
description: Flag che indica se il pin tenta i propri tipi di supporti preferiti prima di quelli del PIN di ricezione.
ms.assetid: 50462ee4-4a61-472f-9a7e-9cdb39be4dea
title: 'Membro CBasePin:: m_bTryMyTypesFirst (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bTryMyTypesFirst
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 72f98021b6ba97d32974f26ac4e76ca31fa54e5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331536"
---
# <a name="cbasepinm_btrymytypesfirst-member"></a>Membro bTryMyTypesFirst di CBasePin:: m \_

Flag che indica se il pin tenta i propri tipi di supporti preferiti prima di quelli del PIN di ricezione.

## <a name="syntax"></a>Sintassi


```C++
bool m_bTryMyTypesFirst;
```



## <a name="remarks"></a>Osservazioni

Il valore predefinito di questo flag è **false**. Se il flag è **true**, il metodo [**CBasePin:: AgreeMediaType**](cbasepin-agreemediatype.md) inverte l'ordine in cui tenta i tipi di supporto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




