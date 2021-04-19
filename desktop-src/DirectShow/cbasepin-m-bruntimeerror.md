---
description: Flag che indica se si è verificato un errore in fase di esecuzione.
ms.assetid: 917bcb21-a11e-4ac5-af96-565f61c155cd
title: 'Membro CBasePin:: m_bRunTimeError (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bRunTimeError
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5e8b0c5548d3089a6e619f88db5e4eed19b12be8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332869"
---
# <a name="cbasepinm_bruntimeerror-member"></a>Membro bRunTimeError di CBasePin:: m \_

Flag che indica se si è verificato un errore in fase di esecuzione.

## <a name="syntax"></a>Sintassi


```C++
bool m_bRunTimeError;
```



## <a name="remarks"></a>Osservazioni

Il valore predefinito di questo flag è **false**. Impostare il flag su **true** se si verifica un errore in fase di esecuzione durante il flusso. Il metodo [**CBasePin:: inactive**](cbasepin-inactive.md) Reimposta il flag su **false**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




