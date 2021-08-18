---
description: Il metodo GetSrcAtTime recupera l'oggetto di origine più vicino all'ora specificata, in base alle condizioni limite specificate.
ms.assetid: 0469c0c2-13df-49f7-95b2-15d3069c5b1c
title: Metodo IAMTimelineTrack::GetSrcAtTime (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetSrcAtTime
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fde7d4d1e1a92c4f403c4d6ae38517bd715cf6d474f22f8a2e262d69fc57139a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052331"
---
# <a name="iamtimelinetrackgetsrcattime-method"></a>Metodo IAMTimelineTrack::GetSrcAtTime

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `GetSrcAtTime` metodo recupera l'oggetto di origine più vicino all'ora specificata, in base alle condizioni limite specificate.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSrcAtTime(
  [out] IAMTimelineObj **ppSrc,
        REFERENCE_TIME Time,
        long           SearchDirection
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppSrc* \[ Cambio\]
</dt> <dd>

Riceve un puntatore [**all'interfaccia IAMTimelineObj**](iamtimelineobj.md) dell'oggetto di origine.

</dd> <dt>

*Time* 
</dt> <dd>

Ora di inizio della ricerca, in unità di 100 nanosecondi.

</dd> <dt>

*SearchDirection* 
</dt> <dd>

Membro del tipo [**enumerato TRACK \_ SEARCH FLAGS \_ \_ CHE**](dexterf-track-search-flags.md) specifica le condizioni limite per la ricerca.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** seguenti:



| Codice restituito                                                                                  | Descrizione                                |
|----------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>      | Non è stato individuato un oggetto di origine.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>         | Individua un oggetto di origine.<br/>        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Argomento non valido.<br/>               |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>    | Argomento del puntatore **NULL.**<br/>      |



 

## <a name="remarks"></a>Commenti

Se il metodo restituisce S \_ OK, **l'interfaccia IAMTimelineObj** restituita ha un conteggio dei riferimenti in sospeso. Assicurarsi di rilasciare l'interfaccia al termine dell'uso.

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare [Microsoft Windows SDK Update per Windows Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IAMTimelineTrack**](iamtimelinetrack.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




