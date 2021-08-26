---
description: Il metodo EffectsEnabled determina se gli effetti sono abilitati. Se gli effetti sono disabilitati, rimangono nella sequenza temporale ma non ne viene eseguito il rendering.
ms.assetid: fd8bb2aa-9c10-4a85-9e9d-1b342fbce03b
title: Metodo IAMTimeline::EffectsEnabled (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.EffectsEnabled
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e63561c62f3cbaf7a3a257179167e657ee4d10c6206b6d74062039362b272aef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905281"
---
# <a name="iamtimelineeffectsenabled-method"></a>Metodo IAMTimeline::EffectsEnabled

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `EffectsEnabled` metodo determina se gli effetti sono abilitati. Se gli effetti sono disabilitati, rimangono nella sequenza temporale ma non ne viene eseguito il rendering.

## <a name="syntax"></a>Sintassi


```C++
HRESULT EffectsEnabled(
   BOOL *pfEnabled
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pfEnabled* 
</dt> <dd>

Riceve un valore booleano che indica se gli effetti sono abilitati. Se **TRUE,** gli effetti sono abilitati. Se **FALSE,** gli effetti sono disabilitati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

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

[**Interfaccia IAMTimeline**](iamtimeline.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




