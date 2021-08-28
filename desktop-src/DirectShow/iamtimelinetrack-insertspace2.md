---
description: Il metodo InsertSpace2 suddivide tutti gli oggetti esistenti all'ora specificata e inserisce spazio tra di essi. Questo metodo è equivalente a IAMTimelineTrack::InsertSpace, ma accetta valori REFTIME.
ms.assetid: 818a1dad-0c8d-4728-82d6-cd52c6c830a2
title: Metodo IAMTimelineTrack::InsertSpace2 (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.InsertSpace2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2f851e6bdccb755977210fcd67e7ce0bb6cb270ec3ff6a4f1fed4806a035a11a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052251"
---
# <a name="iamtimelinetrackinsertspace2-method"></a>Metodo IAMTimelineTrack::InsertSpace2

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `InsertSpace2` metodo suddivide tutti gli oggetti esistenti all'ora specificata e inserisce uno spazio tra di essi. Questo metodo è equivalente a [**IAMTimelineTrack::InsertSpace,**](iamtimelinetrack-insertspace.md)ma accetta [**valori REFTIME.**](reftime.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT InsertSpace2(
   REFTIME rtStart,
   REFTIME rtEnd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*rtStart* 
</dt> <dd>

Ora in cui creare la divisione e il punto iniziale dello spazio inserito, in secondi.

</dd> <dt>

*rtEnd* 
</dt> <dd>

Punto finale dello spazio inserito, espresso in secondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori restituiti possibili sono i seguenti:



| Codice restituito                                                                                   | Descrizione                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>       | Non sono presenti oggetti all'ora specificata.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione completata.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Argomento non valido.<br/>                           |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente.<br/>                        |



 

## <a name="remarks"></a>Commenti

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

 

 




