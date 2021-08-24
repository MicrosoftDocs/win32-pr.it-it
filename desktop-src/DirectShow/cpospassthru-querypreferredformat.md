---
description: Il metodo QueryPreferredFormat recupera il formato di ora preferito per il flusso. Questo metodo implementa il metodo IMediaSeeking::QueryPreferredFormat.
ms.assetid: 8637448f-6b53-4ec9-9671-43bc8b713668
title: Metodo CPosPassThru.QueryPreferredFormat (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.QueryPreferredFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6744516f52a22bf322670388295c55f15f19d19c1b3e5896bba1a66e0668a30
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757041"
---
# <a name="cpospassthruquerypreferredformat-method"></a>Metodo CPosPassThru.QueryPreferredFormat

Il `QueryPreferredFormat` metodo recupera il formato di ora preferito per il flusso. Questo metodo implementa il [**metodo IMediaSeeking::QueryPreferredFormat.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat)

## <a name="syntax"></a>Sintassi


```C++
HRESULT QueryPreferredFormat(
   GUID *pFormat
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFormat* 
</dt> <dd>

Puntatore a una variabile che riceve un GUID in formato ora.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il **valore HRESULT** dal pin connesso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> <dt>

[**GUID di formato ora**](time-format-guids.md)
</dt> </dl>

 

 




