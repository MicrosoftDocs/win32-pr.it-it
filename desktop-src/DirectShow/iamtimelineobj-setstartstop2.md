---
description: Il metodo SetStartStop2 imposta l'ora di inizio e di arresto dell'oggetto rispetto all'elemento padre dell'oggetto. Questo metodo è equivalente a IAMTimelineObj::SetStartStop, ma accetta valori REFTIME.
ms.assetid: 0fc79c82-d8e1-4b87-9e59-6d9e6ca614f3
title: Metodo IAMTimelineObj::SetStartStop2 (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetStartStop2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 30e7f9e6ce54cb86e2eee486937841842311dd498b42ec42e101128612bf16d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086831"
---
# <a name="iamtimelineobjsetstartstop2-method"></a>Metodo IAMTimelineObj::SetStartStop2

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `SetStartStop2` metodo imposta l'ora di inizio e di arresto dell'oggetto rispetto all'elemento padre dell'oggetto. Questo metodo è equivalente a [**IAMTimelineObj::SetStartStop,**](iamtimelineobj-setstartstop.md)ma accetta [**valori REFTIME.**](reftime.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetStartStop2(
   REFTIME Start,
   REFTIME Stop
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Inizia* 
</dt> <dd>

Nuova ora di inizio, in secondi, o -1 per mantenere l'ora di inizio esistente.

</dd> <dt>

*Stop* 
</dt> <dd>

Nuova ora di arresto, in secondi, o -1 per mantenere l'ora di arresto esistente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** seguenti:



| Codice restituito                                                                                  | Descrizione                  |
|----------------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Operazione completata.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Argomento non valido.<br/> |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>    | Non implementato.<br/>  |



 

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

[**Interfaccia IAMTimelineObj**](iamtimelineobj.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




