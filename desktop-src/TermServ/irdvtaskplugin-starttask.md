---
title: Metodo IRDVTaskPlugin StartTask
description: Chiamato per avviare l'attività di aggiornamento nella macchina virtuale.
ms.assetid: c1e9f18b-1e83-4a29-8646-8adde94e8c14
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo StartTask
- Metodo StartTask Servizi Desktop remoto, interfaccia IRDVTaskPlugin
- Interfaccia IRDVTaskPlugin Servizi Desktop remoto, metodo StartTask
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.StartTask
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 51c499549378700a90d8fc78d075bc07c1f874cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477428"
---
# <a name="irdvtaskpluginstarttask-method"></a>Metodo IRDVTaskPlugin:: StartTask

Chiamato per avviare l'attività di aggiornamento nella macchina virtuale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT StartTask(
  [in] BSTR            Label,
  [in] BSTR            Identifier,
  [in] SAFEARRAY(BYTE) *Context
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Etichetta* \[ di in\]
</dt> <dd>

Etichetta per l'attività. Si tratta dell'etichetta passata all'agente trigger nel metodo [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) .

</dd> <dt>

*Identificatore* \[ di in\]
</dt> <dd>

Identificatore dell'attività. Si tratta dell'identificatore passato all'agente trigger nel metodo [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) .

</dd> <dt>

*Contesto* \[ in\]
</dt> <dd>

Dati facoltativi per l'attività. Si tratta dei dati passati all'agente trigger nel metodo [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) .

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

 

 





