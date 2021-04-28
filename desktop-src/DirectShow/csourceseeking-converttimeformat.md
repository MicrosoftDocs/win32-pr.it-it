---
description: 'Metodo CSourceSeeking.ConvertTimeFormat: il metodo ConvertTimeFormat esegue la conversione da un formato di ora a un altro. Questo metodo implementa il metodo IMediaSeeking::ConvertTimeFormat.'
ms.assetid: d0cb44fa-30c1-41b4-92a4-7169161e3140
title: Metodo CSourceSeeking.ConvertTimeFormat (Ctlutil.h)
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
ms.openlocfilehash: 6ba5c6808e091f48baac7d8928e327f45773e13a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085249"
---
# <a name="csourceseekingconverttimeformat-method"></a>Metodo CSourceSeeking.ConvertTimeFormat

Il `ConvertTimeFormat` metodo converte da un formato di ora a un altro. Questo metodo implementa il [**metodo IMediaSeeking::ConvertTimeFormat.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat)

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

Puntatore al GUID del formato di destinazione. Se **NULL,** viene usato il formato corrente. Vedere [**GUID di formato dell'ora.**](time-format-guids.md)

</dd> <dt>

*Origine* 
</dt> <dd>

Valore dell'ora da convertire.

</dd> <dt>

*pSourceFormat* 
</dt> <dd>

Puntatore al GUID del formato dell'ora del formato da convertire. Se **NULL,** viene usato il formato corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei **valori HRESULT** elencati nella tabella seguente.



| Codice restituito                                                                                  | Descrizione                          |
|----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Operazione riuscita<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Argomento non valido<br/>          |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>    | **Argomento puntatore NULL**<br/> |



 

## <a name="remarks"></a>Commenti

L'unico formato di ora supportato dalla classe di base è TIME \_ FORMAT \_ MEDIA TIME \_ (unità da 100 nanosecondi). Questo metodo restituisce E INVALIDARG, ad eccezione del caso semplice in cui \_ *pTargetFormat* e *pSourceFormat* specificano entrambi TIME \_ FORMAT MEDIA \_ \_ TIME.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




