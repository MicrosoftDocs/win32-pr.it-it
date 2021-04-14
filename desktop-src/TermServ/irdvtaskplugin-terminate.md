---
title: Metodo Terminate IRDVTaskPlugin
description: Chiamato quando l'agente attività viene arrestato.
ms.assetid: b693a318-1da7-4207-8046-a62b7ccca471
ms.tgt_platform: multiple
keywords:
- Termina il metodo Servizi Desktop remoto
- Metodo Terminate Servizi Desktop remoto, interfaccia IRDVTaskPlugin
- Interfaccia IRDVTaskPlugin Servizi Desktop remoto, metodo Terminate
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.Terminate
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 178f0a7c054169d972acb6b60a9cc80578fd13e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400731"
---
# <a name="irdvtaskpluginterminate-method"></a>Metodo IRDVTaskPlugin:: terminate

Chiamato quando l'agente attività viene arrestato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Terminate(
  [in] HRESULT hr
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*risorse umane* \[ in\]
</dt> <dd>

Indica se l'arresto è dovuto a un arresto normale o a un errore. Se l'arresto è normale, questo contiene **S \_ OK**. In caso contrario, contiene un codice di errore **HRESULT** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------|
| Client minimo supportato<br/> | Windows 7 Enterprise<br/>   |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IRDVTaskPlugin**](irdvtaskplugin.md)
</dt> </dl>

 

 





