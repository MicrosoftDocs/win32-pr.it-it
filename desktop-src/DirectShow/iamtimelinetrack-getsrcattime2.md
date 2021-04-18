---
description: "Il metodo GetSrcAtTime2 recupera l'oggetto di origine più vicino al tempo specificato, in base alle condizioni di limite specificate. Questo metodo è equivalente a IAMTimelineTrack:: GetSrcAtTime, ma accetta un valore REFTIME."
ms.assetid: 11f6545b-478b-4ffd-8344-2bf8585db2a5
title: 'Metodo IAMTimelineTrack:: GetSrcAtTime2 (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetSrcAtTime2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7140644f64c66b204d6a50cb8e88cb5beca41dae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325632"
---
# <a name="iamtimelinetrackgetsrcattime2-method"></a>Metodo IAMTimelineTrack:: GetSrcAtTime2

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `GetSrcAtTime2` metodo recupera l'oggetto di origine più vicino al tempo specificato, in base alle condizioni di limite specificate. Questo metodo è equivalente a [**IAMTimelineTrack:: GetSrcAtTime**](iamtimelinetrack-getsrcattime.md), ma accetta un valore [**REFTIME**](reftime.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSrcAtTime2(
  [out] IAMTimelineObj **ppSrc,
        REFTIME        Time,
        long           SearchDirection
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppSrc* \[ out\]
</dt> <dd>

Riceve un puntatore all'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) dell'oggetto di origine.

</dd> <dt>

*Time* 
</dt> <dd>

Ora di inizio della ricerca, in secondi.

</dd> <dt>

*SearchDirection* 
</dt> <dd>

Membro del tipo enumerato [**DEXTERF \_ Track \_ Search \_ Flags**](dexterf-track-search-flags.md) che specifica le condizioni limite per la ricerca.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei seguenti valori **HRESULT** :



| Codice restituito                                                                                  | Descrizione                                |
|----------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>      | Impossibile trovare un oggetto di origine.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>         | Si trova un oggetto di origine.<br/>        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Argomento non valido.<br/>               |
| <dl> <dt>**\_puntatore E**</dt> </dl>    | Argomento puntatore **null** .<br/>      |



 

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

 

 




