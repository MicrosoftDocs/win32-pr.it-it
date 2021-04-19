---
description: 'Il metodo GetTransAtTime2 recupera la transizione più vicina al tempo specificato, in base alle condizioni di limite specificate. Questo metodo è equivalente a IAMTimelineTransable:: GetTransAtTime, ma accetta un parametro REFTIME.'
ms.assetid: b51b53ec-4b56-4900-98b5-427d752354b0
title: 'Metodo IAMTimelineTransable:: GetTransAtTime2 (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetTransAtTime2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6b3de498791a634ea651da46ba9c95557ca12b87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332967"
---
# <a name="iamtimelinetransablegettransattime2-method"></a>Metodo IAMTimelineTransable:: GetTransAtTime2

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `GetTransAtTime2` metodo recupera la transizione più vicina al tempo specificato, in base alle condizioni di limite specificate. Questo metodo è equivalente a [**IAMTimelineTransable:: GetTransAtTime**](iamtimelinetransable-gettransattime.md), ma accetta un parametro [**REFTIME**](reftime.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetTransAtTime2(
  [out] IAMTimelineObj **ppObj,
        REFTIME        Time,
        long           SearchDirection
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppObj* \[ out\]
</dt> <dd>

Riceve un puntatore all'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) della transizione.

</dd> <dt>

*Time* 
</dt> <dd>

Tempo da cui iniziare la ricerca, in secondi.

</dd> <dt>

*SearchDirection* 
</dt> <dd>

Membro del tipo enumerato [**DEXTERF \_ Track \_ Search \_ Flags**](dexterf-track-search-flags.md) che specifica le condizioni limite per la ricerca.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei seguenti valori **HRESULT** :



| Codice restituito                                                                                  | Descrizione                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>      | Non è stata trovata alcuna transizione.<br/>   |
| <dl> <dt>**\_OK**</dt> </dl>         | È stata trovata una transizione.<br/>      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Argomento non valido.<br/>          |
| <dl> <dt>**\_puntatore E**</dt> </dl>    | Argomento puntatore **null** .<br/> |



 

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

[**Interfaccia IAMTimelineTransable**](iamtimelinetransable.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




