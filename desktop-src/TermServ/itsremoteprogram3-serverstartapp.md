---
title: Metodo ITSRemoteProgram3 ServerStartApp
description: Specifica un'app da avviare nella sessione remota.
ms.assetid: 55a05d05-66d5-48a1-b3a6-f087aeb62925
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo ServerStartApp
- Metodo ServerStartApp Servizi Desktop remoto, interfaccia ITSRemoteProgram3
- Interfaccia ITSRemoteProgram3 Servizi Desktop remoto, metodo ServerStartApp
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
ms.openlocfilehash: ef1822fa98094870ebebe607528cdc69a8a201f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302455"
---
# <a name="itsremoteprogram3serverstartapp-method"></a>Metodo ITSRemoteProgram3:: ServerStartApp

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

*bstrAppUserModelId* \[ in\]
</dt> <dd></dd> <dt>

*bstrArguments* \[ in\]
</dt> <dd></dd> <dt>

*vbExpandEnvVarInArgumentsOnServer* \[ in\]
</dt> <dd></dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                            |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITSRemoteProgram3**](itsremoteprogram3.md)
</dt> </dl>

 

 





