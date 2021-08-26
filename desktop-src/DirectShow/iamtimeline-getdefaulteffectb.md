---
description: Il metodo GetDefaultEffectB recupera l'effetto predefinito. Questo metodo è equivalente a IAMTimeline::GetDefaultEffect, ma riceve un valore BSTR anziché un GUID.
ms.assetid: 62c37a61-9875-4140-8552-83d82c060715
title: Metodo IAMTimeline::GetDefaultEffectB (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultEffectB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5f0abfac297817b4e93b4eabe5bd2517c22ab363498bbbe35f2b5ae449524ecd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997771"
---
# <a name="iamtimelinegetdefaulteffectb-method"></a>Metodo IAMTimeline::GetDefaultEffectB

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `GetDefaultEffectB` metodo recupera l'effetto predefinito. Questo metodo equivale a [**IAMTimeline::GetDefaultEffect,**](iamtimeline-getdefaulteffect.md)ma riceve un **valore BSTR** anziché un GUID.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDefaultEffectB(
  [out, retval] BSTR *pGuid
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pGuid* \[ out, retval\]
</dt> <dd>

Riceve un **valore BSTR** che rappresenta il GUID dell'effetto predefinito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Il metodo alloca memoria per la stringa. L'applicazione deve **chiamare SysFreeString** per liberare la memoria.

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

 

 




