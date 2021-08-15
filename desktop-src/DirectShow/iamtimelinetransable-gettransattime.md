---
description: Il metodo GetTransAtTime recupera la transizione più vicina all'ora specificata, in base alle condizioni limite specificate.
ms.assetid: 33b3686b-5a9d-4eb2-bd40-4d6f569e7d89
title: Metodo IAMTimelineTransable::GetTransAtTime (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetTransAtTime
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: db81cf9a91f34699765e89f917ec31a902ebd188dc61dd77a1b909d10b09788c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118399208"
---
# <a name="iamtimelinetransablegettransattime-method"></a>Metodo IAMTimelineTransable::GetTransAtTime

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il `GetTransAtTime` metodo recupera la transizione più vicina all'ora specificata, in base alle condizioni limite specificate.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetTransAtTime(
  [out] IAMTimelineObj **ppObj,
        REFERENCE_TIME Time,
        long           SearchDirection
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppObj* \[ Cambio\]
</dt> <dd>

Riceve un puntatore all'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) della transizione.

</dd> <dt>

*Time* 
</dt> <dd>

Ora da cui iniziare la ricerca, in unità di 100 nanosecondi.

</dd> <dt>

*SearchDirection* 
</dt> <dd>

Membro del tipo [**enumerato DEXTERF \_ TRACK SEARCH \_ \_ FLAGS**](dexterf-track-search-flags.md) che specifica le condizioni limite per la ricerca.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** seguenti:



| Codice restituito                                                                                  | Descrizione                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>      | Non è stata trovata alcuna transizione.<br/>   |
| <dl> <dt>**S \_ OK**</dt> </dl>         | È stata trovata la transizione.<br/>      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Argomento non valido.<br/>          |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>    | Argomento del puntatore **NULL.**<br/> |



 

## <a name="remarks"></a>Commenti

Se il metodo restituisce S \_ OK, **l'interfaccia IAMTimelineObj** restituita ha un conteggio dei riferimenti in sospeso. Assicurarsi di rilasciare l'interfaccia al termine dell'uso.

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare l'aggiornamento di Microsoft Windows SDK per Windows [Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IAMTimelineTransable**](iamtimelinetransable.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




