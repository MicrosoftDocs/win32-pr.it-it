---
description: Il metodo CheckCapabilities esegue una query se un flusso ha specificato funzionalità di ricerca. Questo metodo implementa il metodo IMediaSeeking::CheckCapabilities.
ms.assetid: 48096af6-bbce-4a1f-be9a-fd150ed4536e
title: Metodo CPosPassThru.CheckCapabilities (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CheckCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f1146e11097dbb2d717bd025d414b4510a219cc5f131e2fa7d56687128ddfd98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108421"
---
# <a name="cpospassthrucheckcapabilities-method"></a>Metodo CPosPassThru.CheckCapabilities

Il `CheckCapabilities` metodo esegue una query se un flusso ha specificato funzionalità di ricerca. Questo metodo implementa il [**metodo IMediaSeeking::CheckCapabilities.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities)

## <a name="syntax"></a>Sintassi


```C++
HRESULT CheckCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pCapabilities* 
</dt> <dd>

Puntatore a una combinazione bit per bit di uno o più [**attributi AM \_ \_ SEEKING SEEKING \_ CAPABILITIES.**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) Quando il metodo viene restituito, il valore indica quali attributi sono disponibili.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il **valore HRESULT** dal pin connesso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 




