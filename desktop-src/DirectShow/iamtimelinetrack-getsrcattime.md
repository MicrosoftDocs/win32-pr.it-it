---
description: Il metodo GetSrcAtTime recupera l'oggetto di origine più vicino al tempo specificato, in base alle condizioni di limite specificate.
ms.assetid: 0469c0c2-13df-49f7-95b2-15d3069c5b1c
title: 'Metodo IAMTimelineTrack:: GetSrcAtTime (qedit. h)'
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
ms.openlocfilehash: 4b726d26efd0550df364200a27d536d60d38274a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325633"
---
# <a name="iamtimelinetrackgetsrcattime-method"></a>Metodo IAMTimelineTrack:: GetSrcAtTime

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `GetSrcAtTime` metodo recupera l'oggetto di origine più vicino al tempo specificato, in base alle condizioni di limite specificate.

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

*ppSrc* \[ out\]
</dt> <dd>

Riceve un puntatore all'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) dell'oggetto di origine.

</dd> <dt>

*Time* 
</dt> <dd>

Ora di inizio della ricerca, in unità di 100 nanosecondi.

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

 

 




