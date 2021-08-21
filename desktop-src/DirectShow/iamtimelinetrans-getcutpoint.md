---
description: Il metodo GetCutPoint recupera il punto di taglio.
ms.assetid: f54ef17e-3407-4164-911d-3dc7fad656ed
title: Metodo IAMTimelineTrans::GetCutPoint (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetCutPoint
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0582446a3f88b3692b50ca97d033a85d1dfca475051e3538c39d41003e788ebc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154795"
---
# <a name="iamtimelinetransgetcutpoint-method"></a>Metodo IAMTimelineTrans::GetCutPoint

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `GetCutPoint` metodo recupera il punto di taglio. Se si esegue il rendering di una transizione come taglio, il punto di taglio è il momento in cui la transizione si interrompe da un'origine a quella successiva. Per impostazione predefinita, questo valore è il centro della transizione. Ad esempio, in una transizione che si estende su un secondo, il punto di taglio predefinito è 0,5 secondi nella transizione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetCutPoint(
   REFERENCE_TIME *pTLTime
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pTLTime* 
</dt> <dd>

Riceve il punto di taglio, relativo all'ora di inizio della transizione, in unità di 100 nanosecondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** seguenti:



| Codice restituito                                                                               | Descrizione                                                                    |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>   | Il punto di taglio non è stato impostato. Il valore restituito è il valore predefinito.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>      | Il punto di taglio è stato impostato su un valore diverso da quello predefinito.<br/>            |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl> | Argomento del puntatore **NULL.**<br/>                                          |



 

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

[**Interfaccia IAMTimelineTrans**](iamtimelinetrans.md)
</dt> <dt>

[**IAMTimelineTrans::SetCutPoint**](iamtimelinetrans-setcutpoint.md)
</dt> <dt>

[**IAMTimelineTrans::GetCutsOnly**](iamtimelinetrans-getcutsonly.md)
</dt> <dt>

[**IAMTimeline::TransitionsEnabled**](iamtimeline-transitionsenabled.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




