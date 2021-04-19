---
description: 'Il metodo GetDefaultTransitionB recupera la transizione predefinita. Questo metodo è equivalente a IAMTimeline:: GetDefaultTransition, ma riceve un valore BSTR anziché un GUID.'
ms.assetid: ed743766-e970-4bd9-a9a0-8b5d9fec2d80
title: 'Metodo IAMTimeline:: GetDefaultTransitionB (qedit. h)'
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
ms.openlocfilehash: f150ca0fafff6b250776a38b7ec68beb470e9d6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332694"
---
# <a name="iamtimelinegetdefaulttransitionb-method"></a>Metodo IAMTimeline:: GetDefaultTransitionB

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `GetDefaultTransitionB` metodo recupera la transizione predefinita. Questo metodo è equivalente a [**IAMTimeline:: GetDefaultTransition**](iamtimeline-getdefaulttransition.md), ma riceve un valore BSTR anziché un GUID.

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

Riceve un valore **BSTR** che rappresenta il GUID della transizione predefinita.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Il metodo alloca memoria per la stringa. Per liberare la memoria, l'applicazione deve chiamare **SysFreeString** .

> [!Note]  
> Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IAMTimeline**](iamtimeline.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




