---
description: Il metodo SetDefaultEffectB imposta l'effetto predefinito. Questo metodo è equivalente a IAMTimeline::SetDefaultEffect, ma accetta un valore BSTR anziché un puntatore a un GUID.
ms.assetid: ffee9728-f69e-48a4-ac0a-d41347a20deb
title: Metodo IAMTimeline::SetDefaultEffectB (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetDefaultEffectB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 356874574fd0d960350ab991a97bfd9c6e2641d026da836ecf240bb4391c4a47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073125"
---
# <a name="iamtimelinesetdefaulteffectb-method"></a>Metodo IAMTimeline::SetDefaultEffectB

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `SetDefaultEffectB` metodo imposta l'effetto predefinito. Questo metodo equivale a [**IAMTimeline::SetDefaultEffect,**](iamtimeline-setdefaulteffect.md)ma accetta un valore BSTR anziché un puntatore a un GUID.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetDefaultEffectB(
   BSTR pGuid
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pGuid* 
</dt> <dd>

Valore BSTR che rappresenta il GUID dell'effetto predefinito.

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

 

 




