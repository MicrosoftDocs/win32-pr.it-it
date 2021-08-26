---
description: Il metodo GetNextSrc cerca l'origine successiva che viene visualizzata all'ora specificata o in un secondo momento.
ms.assetid: e87d8978-7b45-41a3-a74d-b5dd231d1d85
title: Metodo IAMTimelineTrack::GetNextSrc (Qedit.h)
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
ms.openlocfilehash: dd0257fa614a6581cc31f5416e6f1c2395fcb9444721d3668c9f2d2498e52088
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904641"
---
# <a name="iamtimelinetrackgetnextsrc-method"></a>Metodo IAMTimelineTrack::GetNextSrc

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `GetNextSrc` metodo cerca nella traccia l'origine successiva visualizzata all'ora specificata o in un secondo momento.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetNextSrc(
  [out] IAMTimelineObj **ppSrc,
        REFERENCE_TIME *pInOut
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppSrc* \[ Cambio\]
</dt> <dd>

Riceve un puntatore all'interfaccia [**IAMTimelineObj**](iamtimelineobj.md) dell'oggetto di origine.

</dd> <dt>

*Pinout* 
</dt> <dd>

Puntatore a una variabile che contiene l'ora di inizio della ricerca, in unità di 100 nanosecondi. Se il metodo recupera un'origine, imposta il valore sull'ora di arresto dell'origine. Se il metodo non recupera un'origine, il valore diventa non valido e l'applicazione non deve usarlo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK se il metodo recupera un'origine oppure S FALSE in caso \_ contrario.

## <a name="remarks"></a>Commenti

Se l'ora specificata da *pInOut* è compresa tra l'ora di inizio e di arresto di un'origine, il metodo recupera tale origine.

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

 

 




