---
description: Il metodo GetNextSrc2 cerca l'origine successiva che viene visualizzata all'ora specificata o in un secondo momento. Questo metodo è equivalente a IAMTimelineTrack::GetNextSrc, ma accetta un valore REFTIME.
ms.assetid: f3f7b000-ec73-4ae9-802b-a9bc6f1840b3
title: Metodo IAMTimelineTrack::GetNextSrc2 (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetNextSrc2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ca9b18ba6ddd56771ac738f0ff831e4ea284d995fb28582a578386321e7ef856
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154822"
---
# <a name="iamtimelinetrackgetnextsrc2-method"></a>Metodo IAMTimelineTrack::GetNextSrc2

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `GetNextSrc2` metodo cerca nella traccia l'origine successiva visualizzata all'ora specificata o in un secondo momento. Questo metodo equivale a [**IAMTimelineTrack::GetNextSrc,**](iamtimelinetrack-getnextsrc.md)ma accetta un [**valore REFTIME.**](reftime.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetNextSrc2(
  [out] IAMTimelineObj **ppSrc,
        REFTIME        *pInOut
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

In input, contiene l'ora di inizio della ricerca, in secondi. Se il metodo recupera un'origine, imposta il valore sull'ora di arresto dell'origine. Se il metodo non recupera un'origine, il valore diventa non valido e l'applicazione non deve usarlo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK se il metodo recupera un'origine oppure S FALSE in caso \_ contrario.

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

 

 




