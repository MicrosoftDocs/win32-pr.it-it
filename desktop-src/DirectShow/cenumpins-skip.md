---
description: 'Il metodo Skip ignora un numero specificato di pin nella sequenza di enumerazione. Questo metodo implementa il metodo IEnumPins:: Skip.'
ms.assetid: d42f958c-f488-4730-ab84-fc4e4150b186
title: Metodo CEnumPins. Skip (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.Skip
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1865453a89130303f28f338d8b7567e856c64173
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329833"
---
# <a name="cenumpinsskip-method"></a>Metodo CEnumPins. Skip

Il `Skip` metodo ignora un numero specificato di pin nella sequenza di enumerazione. Questo metodo implementa il metodo [**IEnumPins:: Skip**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-skip) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT Skip(
   ULONG cPins
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*cPins* 
</dt> <dd>

Numero di pin da ignorare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.



| Codice restituito                                                                                                | Descrizione                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>                    | Ignorato oltre la fine della sequenza.<br/>                                       |
| <dl> <dt>**\_OK**</dt> </dl>                       | Esito positivo.<br/>                                                                    |
| <dl> <dt>**non \_ \_ \_ \_ sincronizzato con VFW E enum \_**</dt> </dl> | Lo stato del filtro è stato modificato ed è ora incoerente con l'enumeratore.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CEnumPins**](cenumpins.md)
</dt> </dl>

 

 




