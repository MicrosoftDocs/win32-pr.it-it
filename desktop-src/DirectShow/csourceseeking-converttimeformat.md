---
description: 'Il metodo ConvertTimeFormat converte da un formato di ora a un altro. Questo metodo implementa il metodo IMediaSeeking:: ConvertTimeFormat.'
ms.assetid: d0cb44fa-30c1-41b4-92a4-7169161e3140
title: Metodo CSourceSeeking. ConvertTimeFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ConvertTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3869ef5bc9656414ca5b465a04d04a4ca4be41e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325660"
---
# <a name="csourceseekingconverttimeformat-method"></a>CSourceSeeking. ConvertTimeFormat, metodo

Il `ConvertTimeFormat` metodo converte da un formato di ora a un altro. Questo metodo implementa il metodo [**IMediaSeeking:: ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT ConvertTimeFormat(
         LONGLONG *pTarget,
   const GUID     *pTargetFormat,
         LONGLONG Source,
   const GUID     *pSourceFormat
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pTarget* 
</dt> <dd>

Puntatore a una variabile che riceve l'ora convertita.

</dd> <dt>

*pTargetFormat* 
</dt> <dd>

Puntatore al GUID del formato di destinazione. Se è **null**, viene utilizzato il formato corrente. Vedere [**GUID del formato ora**](time-format-guids.md).

</dd> <dt>

*Origine* 
</dt> <dd>

Valore dell'ora da convertire.

</dd> <dt>

*pSourceFormat* 
</dt> <dd>

Puntatore al GUID del formato dell'ora del formato da convertire. Se è **null**, viene utilizzato il formato corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** elencati nella tabella seguente.



| Codice restituito                                                                                  | Descrizione                          |
|----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Operazione riuscita<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Argomento non valido<br/>          |
| <dl> <dt>**\_puntatore E**</dt> </dl>    | Argomento puntatore **null**<br/> |



 

## <a name="remarks"></a>Commenti

L'unico formato di ora supportato dalla classe base è il \_ tempo medio di formato dell'ora \_ \_ (unità 100-nanosecondi). Questo metodo restituisce E \_ INVALIDARG, eccetto nel caso più semplice in cui *PTargetFormat* e *pSourceFormat* specificano il tempo di supporto del \_ formato ora \_ \_ .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




