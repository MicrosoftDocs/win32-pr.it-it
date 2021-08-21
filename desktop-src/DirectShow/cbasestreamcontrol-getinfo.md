---
description: Il metodo GetInfo recupera informazioni sulle impostazioni correnti del controllo di flusso, incluse le ore di inizio e di arresto. Questo metodo implementa il metodo IAMStreamControl::GetInfo.
ms.assetid: 3bc9bb32-eb33-4752-b22c-9033c28b41f7
title: Metodo CBaseStreamControl.GetInfo (Strmctl.h)
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
ms.openlocfilehash: 96bc59b6dc55d73aa16b08f53f831428ae2d2fb7b181d3bb255b61a323b236a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157218"
---
# <a name="cbasestreamcontrolgetinfo-method"></a>Metodo CBaseStreamControl.GetInfo

Il `GetInfo` metodo recupera informazioni sulle impostazioni correnti del controllo di flusso, incluse le ore di inizio e di arresto. Questo metodo implementa il [**metodo IAMStreamControl::GetInfo.**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-getinfo)

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

Puntatore a [**una struttura AM STREAM \_ \_ INFO,**](/windows/desktop/api/strmif/ns-strmif-am_stream_info) allocata dal chiamante, che riceve le impostazioni correnti del controllo di flusso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK o \_ PUNTATORE E.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Strmctl.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseStreamControl**](cbasestreamcontrol.md)
</dt> </dl>

 

 




