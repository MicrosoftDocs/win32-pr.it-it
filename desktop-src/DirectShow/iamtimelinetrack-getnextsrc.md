---
description: Il metodo GetNextSrc Cerca nella traccia la successiva origine visualizzata all'ora specificata o successiva.
ms.assetid: e87d8978-7b45-41a3-a74d-b5dd231d1d85
title: 'Metodo IAMTimelineTrack:: GetNextSrc (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetNextSrc
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dd8ca25b2d5a551d803e79e69cf8d1095ee47511
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325174"
---
# <a name="iamtimelinetrackgetnextsrc-method"></a>Metodo IAMTimelineTrack:: GetNextSrc

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `GetNextSrc` metodo cerca nella traccia la successiva origine visualizzata all'ora specificata o successiva.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetNextSrc(
  [out] IAMTimelineObj **ppSrc,
        REFERENCE_TIME *pInOut
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

Puntatore a una variabile che contiene l'ora di inizio della ricerca, in unità di 100 nanosecondi. Se il metodo recupera un'origine, imposta il valore sull'ora di arresto dell'origine. Se il metodo non recupera un'origine, il valore diventa non valido e non deve essere usato dall'applicazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se il metodo recupera un'origine o \_ false in caso contrario.

## <a name="remarks"></a>Commenti

Se l'ora specificata dalla *piedinatura* è compresa tra l'ora di inizio e di fine di un'origine, il metodo recupera tale origine.

Se il metodo restituisce S \_ OK, l'interfaccia **IAMTimelineObj** restituita presenta un conteggio dei riferimenti in attesa. Assicurarsi di rilasciare l'interfaccia al termine dell'utilizzo.

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

 

 




