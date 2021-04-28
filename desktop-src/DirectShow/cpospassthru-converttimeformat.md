---
description: 'Metodo CPosPassThru.ConvertTimeFormat: il metodo ConvertTimeFormat esegue la conversione da un formato di ora a un altro. Questo metodo implementa il metodo IMediaSeeking::ConvertTimeFormat.'
ms.assetid: e766d112-ee41-4c64-a735-b6317093518a
title: Metodo CPosPassThru.ConvertTimeFormat (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.ConvertTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fc463cb6dc891e677266289971a1dac8b335a8c7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098959"
---
# <a name="cpospassthruconverttimeformat-method"></a>Metodo CPosPassThru.ConvertTimeFormat

Il `ConvertTimeFormat` metodo esegue la conversione da un formato di ora a un altro. Questo metodo implementa il [**metodo IMediaSeeking::ConvertTimeFormat.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat)

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

Puntatore al GUID del formato dell'ora del formato di destinazione. Se **NULL,** viene usato il formato corrente.

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

Restituisce il **valore HRESULT** dal pin connesso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> <dt>

[**GUID di formato ora**](time-format-guids.md)
</dt> </dl>

 

 




