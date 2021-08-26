---
description: Il metodo GetDefaultTransitionB recupera la transizione predefinita. Questo metodo equivale a IAMTimeline::GetDefaultTransition, ma riceve un valore BSTR anziché un GUID.
ms.assetid: ed743766-e970-4bd9-a9a0-8b5d9fec2d80
title: Metodo IAMTimeline::GetDefaultTransitionB (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultTransitionB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 39725fc4e4f5c9f02dcd092fddba632262c3b8a0aa85e27afd7df1afb9bb314c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107841"
---
# <a name="iamtimelinegetdefaulttransitionb-method"></a>Metodo IAMTimeline::GetDefaultTransitionB

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il `GetDefaultTransitionB` metodo recupera la transizione predefinita. Questo metodo equivale a [**IAMTimeline::GetDefaultTransition**](iamtimeline-getdefaulttransition.md), ma riceve un valore BSTR, anziché un GUID.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDefaultTransitionB(
  [out, retval] BSTR *pGuid
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pGuid* \[ out, retval\]
</dt> <dd>

Riceve un **valore BSTR** che rappresenta il GUID della transizione predefinita.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Il metodo alloca memoria per la stringa. L'applicazione deve **chiamare SysFreeString** per liberare la memoria.

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare l'aggiornamento di Microsoft Windows SDK per Windows [Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

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

 

 




