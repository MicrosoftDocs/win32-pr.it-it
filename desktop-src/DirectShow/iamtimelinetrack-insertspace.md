---
description: Il metodo InsertSpace suddivide tutti gli oggetti esistenti al momento specificato e inserisce uno spazio tra di essi.
ms.assetid: f9e48f58-1867-405c-b208-1ab781912aa1
title: 'Metodo IAMTimelineTrack:: InsertSpace (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.InsertSpace
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 84d8076f6f89ee5e890db0047d47ade283b1e333
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325631"
---
# <a name="iamtimelinetrackinsertspace-method"></a>Metodo IAMTimelineTrack:: InsertSpace

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `InsertSpace` metodo suddivide tutti gli oggetti esistenti al momento specificato e inserisce uno spazio tra di essi.

## <a name="syntax"></a>Sintassi


```C++
HRESULT InsertSpace(
   REFERENCE_TIME rtStart,
   REFERENCE_TIME rtEnd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*rtStart* 
</dt> <dd>

Ora in cui creare la divisione e il punto iniziale dello spazio inserito, in unità di 100 nanosecondi.

</dd> <dt>

*rtEnd* 
</dt> <dd>

Punto finale dello spazio inserito, in unità di 100 nanosecondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . Tra i possibili valori restituiti sono inclusi i seguenti:



| Codice restituito                                                                                   | Descrizione                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>       | Nessun oggetto all'ora specificata.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>          | Esito positivo.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Argomento non valido.<br/>                           |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Memoria insufficiente.<br/>                        |



 

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

 

 




