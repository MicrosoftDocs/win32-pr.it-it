---
description: 'Il metodo CheckCapabilities esegue una query per determinare se un flusso ha specificato funzionalità di ricerca. Questo metodo implementa il metodo IMediaSeeking:: CheckCapabilities.'
ms.assetid: 48096af6-bbce-4a1f-be9a-fd150ed4536e
title: Metodo CPosPassThru. CheckCapabilities (Ctlutil. h)
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
ms.openlocfilehash: 33f7a685684667d2f5d465b14070a595c70b178c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329518"
---
# <a name="cpospassthrucheckcapabilities-method"></a>CPosPassThru. CheckCapabilities, metodo

Il `CheckCapabilities` metodo esegue una query per determinare se un flusso ha specificato funzionalità di ricerca. Questo metodo implementa il metodo [**IMediaSeeking:: CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) .

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

Puntatore a una combinazione bit per bit di uno o più attributi per la [**\_ ricerca di \_ \_ funzionalità**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) . Quando il metodo restituisce un risultato, il valore indica quale di questi attributi sono disponibili.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore **HRESULT** dal pin connesso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 




