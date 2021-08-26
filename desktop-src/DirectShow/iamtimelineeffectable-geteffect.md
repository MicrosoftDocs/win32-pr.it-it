---
description: Il metodo GetEffect recupera l'effetto al livello di priorità specificato.
ms.assetid: 8606c457-1c4d-4a20-b674-aaf82abeb451
title: Metodo IAMTimelineEffectable::GetEffect (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable.GetEffect
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d53ecc7c3d5291ddb6b894b24835eeb236f036e94eb166383da907a9f469c960
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905181"
---
# <a name="iamtimelineeffectablegeteffect-method"></a>Metodo IAMTimelineEffectable::GetEffect

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il **metodo GetEffect** recupera l'effetto al livello di priorità specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetEffect(
  [out] IAMTimelineObj **ppFX,
        long           Which
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppFX* \[ Cambio\]
</dt> <dd>

Riceve l'interfaccia [**IAMTimelineObj dell'effetto.**](iamtimelineobj.md)

</dd> <dt>

*Che* 
</dt> <dd>

Livello di priorità dell'effetto da recuperare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore HRESULT. I possibili valori sono i seguenti:



| Codice restituito                                                                               | Descrizione                                     |
|-------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>   | Nessun effetto con la priorità specificata.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>      | Operazione completata.<br/>                             |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl> | Argomento del puntatore **NULL.**<br/>           |



 

## <a name="remarks"></a>Commenti

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

[**Interfaccia IAMTimelineEffectable**](iamtimelineeffectable.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




