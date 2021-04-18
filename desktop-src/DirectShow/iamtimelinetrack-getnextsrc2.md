---
description: "Il metodo GetNextSrc2 Cerca nella traccia la successiva origine visualizzata all'ora specificata o successiva. Questo metodo è equivalente a IAMTimelineTrack:: GetNextSrc, ma accetta un valore REFTIME."
ms.assetid: f3f7b000-ec73-4ae9-802b-a9bc6f1840b3
title: 'Metodo IAMTimelineTrack:: GetNextSrc2 (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetNextSrc2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c934cfd6c4f58c5fca59e78e120fee89af3f73a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325638"
---
# <a name="iamtimelinetrackgetnextsrc2-method"></a>Metodo IAMTimelineTrack:: GetNextSrc2

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `GetNextSrc2` metodo cerca nella traccia la successiva origine visualizzata all'ora specificata o successiva. Questo metodo è equivalente a [**IAMTimelineTrack:: GetNextSrc**](iamtimelinetrack-getnextsrc.md), ma accetta un valore [**REFTIME**](reftime.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetNextSrc2(
  [out] IAMTimelineObj **ppSrc,
        REFTIME        *pInOut
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppSrc* \[ out\]
</dt> <dd>

Riceve un puntatore all'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) dell'oggetto di origine.

</dd> <dt>

*pInOut* 
</dt> <dd>

In input, contiene l'ora di inizio della ricerca, in secondi. Se il metodo recupera un'origine, imposta il valore sull'ora di arresto dell'origine. Se il metodo non recupera un'origine, il valore diventa non valido e non deve essere usato dall'applicazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se il metodo recupera un'origine o \_ false in caso contrario.

## <a name="remarks"></a>Commenti

> [!Note]  
> Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IAMTimelineTrack**](iamtimelinetrack.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




