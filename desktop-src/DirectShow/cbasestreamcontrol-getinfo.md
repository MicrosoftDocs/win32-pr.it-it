---
description: 'Il metodo GetInfo recupera informazioni sulle impostazioni correnti del controllo del flusso, incluse le ore di inizio e di fine. Questo metodo implementa il metodo IAMStreamControl:: GetInfo.'
ms.assetid: 3bc9bb32-eb33-4752-b22c-9033c28b41f7
title: Metodo CBaseStreamControl. GetInfo (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.GetInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ab0ba31fa5692a6bc92372860ec1a28ab776206f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331649"
---
# <a name="cbasestreamcontrolgetinfo-method"></a>CBaseStreamControl. GetInfo, metodo

Il `GetInfo` metodo recupera informazioni sulle impostazioni correnti del controllo del flusso, incluse le ore di inizio e di fine. Questo metodo implementa il metodo [**IAMStreamControl:: GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-getinfo) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetInfo(
   AM_STREAM_INFO *pInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pInfo* 
</dt> <dd>

Puntatore a una struttura di [**\_ \_ informazioni del flusso AM**](/windows/desktop/api/strmif/ns-strmif-am_stream_info) , allocata dal chiamante, che riceve le impostazioni correnti del controllo di flusso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un \_ puntatore S OK o e \_ .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Strmctl. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseStreamControl**](cbasestreamcontrol.md)
</dt> </dl>

 

 




