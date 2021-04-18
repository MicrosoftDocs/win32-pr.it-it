---
description: "Il metodo FindPin ottiene il pin con l'identificatore specificato. Questo metodo implementa il metodo IBaseFilter:: FindPin."
ms.assetid: 56ee3e0d-9e3f-4d25-846b-50119b55a122
title: Metodo CTransformFilter. FindPin (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1631651932d5adbc49fb59d44291dccea55fd41f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328337"
---
# <a name="ctransformfilterfindpin-method"></a>CTransformFilter. FindPin, metodo

Il metodo **FindPin** ottiene il pin con l'identificatore specificato. Questo metodo implementa il metodo [**IBaseFilter:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Id* 
</dt> <dd>

Stringa di caratteri wide che contiene l'identificatore del PIN.

</dd> <dt>

*ppPin* 
</dt> <dd>

Riceve un puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN. Se il metodo ha esito negativo, `*ppPin` viene impostato su **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.



| Codice restituito                                                                                       | Descrizione                                           |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>              | Esito positivo.<br/>                                   |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl>     | Memoria insufficiente.<br/>                       |
| <dl> <dt>**\_puntatore E**</dt> </dl>         | Argomento puntatore **null** .<br/>                 |
| <dl> <dt>**VFW \_ E \_ non \_ trovato**</dt> </dl> | Non è stato possibile trovare un pin con questo identificatore.<br/> |



 

## <a name="remarks"></a>Commenti

> [!IMPORTANT]
> L'implementazione di questo metodo non chiama [**Ipin:: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) per trovare la corrispondenza con l'identificatore del PIN. Al contrario, il metodo presuppone che il pin di input sia denominato "in" e che il pin di output sia denominato "out". Se si usa un set di identificatori di PIN diverso, eseguire l'override di questo metodo.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




