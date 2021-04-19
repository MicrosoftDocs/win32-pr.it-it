---
description: 'Il metodo StopAt informa il PIN quando interrompere la distribuzione dei dati. Questo metodo implementa il metodo IAMStreamControl:: StopAt.'
ms.assetid: cc9f0fdc-253b-4feb-95ce-56ebc575a49b
title: Metodo CBaseStreamControl. StopAt (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.StopAt
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8e6b794f5f05721f403d943252c2aabd48614519
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324026"
---
# <a name="cbasestreamcontrolstopat-method"></a>CBaseStreamControl. StopAt, metodo

Il `StopAt` metodo informa il PIN quando interrompere la distribuzione dei dati. Questo metodo implementa il metodo [**IAMStreamControl:: STOPAT**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT StopAt(
   const REFERENCE_TIME *ptStop = NULL,
         BOOL           bSendExtra = FALSE,
         DWORD          dwCookie = 0
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ptStop* 
</dt> <dd>

Puntatore a un valore di [**\_ ora di riferimento**](reference-time.md) che specifica quando il PIN deve interrompere la distribuzione dei dati.

</dd> <dt>

*bSendExtra* 
</dt> <dd>

Specifica un valore booleano che indica se inviare un campione aggiuntivo dopo l'ora di arresto pianificata. Se **true**, il pin Invia un campione aggiuntivo.

</dd> <dt>

*dwCookie* 
</dt> <dd>

Specifica un valore da inviare insieme alla notifica di avvio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Strmctl. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseStreamControl**](cbasestreamcontrol.md)
</dt> </dl>

 

 




