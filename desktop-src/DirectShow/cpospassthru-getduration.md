---
description: 'Metodo CPosPassThru.GetDuration: il metodo GetDuration recupera la durata del flusso. Questo metodo implementa il metodo IMediaSeeking::GetDuration.'
ms.assetid: 0552e7bb-4d7e-40a8-a8ad-89ae6fff8ccb
title: Metodo CPosPassThru.GetDuration (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetDuration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0b0af7bfaca405ed52a4e3c5a63c18b4bc087ba3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085579"
---
# <a name="cpospassthrugetduration-method"></a>Metodo CPosPassThru.GetDuration

Il `GetDuration` metodo recupera la durata del flusso. Questo metodo implementa il [**metodo IMediaSeeking::GetDuration.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration)

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDuration(
   LONGLONG *pDuration
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDuration* 
</dt> <dd>

Puntatore a una variabile che riceve la durata, in unità del formato di ora corrente.

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
</dt> </dl>

 

 




