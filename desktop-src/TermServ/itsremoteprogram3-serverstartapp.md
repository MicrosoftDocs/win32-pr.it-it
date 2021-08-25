---
title: Metodo ITSRemoteProgram3 ServerStartApp
description: Specifica un'app da avviare nella sessione remota.
ms.assetid: 55a05d05-66d5-48a1-b3a6-f087aeb62925
ms.tgt_platform: multiple
keywords:
- Metodo ServerStartApp Servizi Desktop remoto
- Metodo ServerStartApp Servizi Desktop remoto, interfaccia ITSRemoteProgram3
- ItsRemoteProgram3 interface Servizi Desktop remoto , Metodo ServerStartApp
topic_type:
- apiref
api_name:
- ITSRemoteProgram3.ServerStartApp
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e162f220c59f8dfaca1d1f5666fb691ca02b8f53b5fcfe0476bf188d55b25d6e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072231"
---
# <a name="itsremoteprogram3serverstartapp-method"></a>Metodo ITSRemoteProgram3::ServerStartApp

Specifica un'app da avviare nella sessione remota.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ServerStartApp(
  [in] BSTR         bstrAppUserModelId,
  [in] BSTR         bstrArguments,
  [in] VARIANT_BOOL vbExpandEnvVarInArgumentsOnServer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrAppUserModelId* \[ Pollici\]
</dt> <dd></dd> <dt>

*bstrArguments* \[ Pollici\]
</dt> <dd></dd> <dt>

*VbExpandEnvVarInArgumentsOnServer* \[ Pollici\]
</dt> <dd></dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITSRemoteProgram3**](itsremoteprogram3.md)
</dt> </dl>

 

 





