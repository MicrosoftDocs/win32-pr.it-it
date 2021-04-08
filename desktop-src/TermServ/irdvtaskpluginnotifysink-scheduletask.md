---
title: Metodo IRDVTaskPluginNotifySink ScheduleTask
description: Chiamato dall'agente attività per pianificare un'attività.
ms.assetid: 06793439-cf16-40ca-8a91-08acc22c73ed
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del Metodo ScheduleTask
- Metodo ScheduleTask Servizi Desktop remoto, interfaccia IRDVTaskPluginNotifySink
- Interfaccia IRDVTaskPluginNotifySink Servizi Desktop remoto, Metodo ScheduleTask
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.ScheduleTask
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c9bde92992eec9c4ab3d4151c59e6d687ec2f3fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874506"
---
# <a name="irdvtaskpluginnotifysinkscheduletask-method"></a>Metodo IRDVTaskPluginNotifySink:: ScheduleTask

Chiamato dall'agente attività per pianificare un'attività.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ScheduleTask(
  [in] FILETIME        ftStartTime,
  [in] FILETIME        ftEndTime,
  [in] FILETIME        ftDeadline,
  [in] BSTR            bstrLabel,
  [in] BSTR            bstrIdentifier,
  [in] SAFEARRAY(BYTE) saContext
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ftStartTime* \[ in\]
</dt> <dd>

Tipo: **[ **FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**

Ora di inizio dell'attività più recente, in formato UTC.

</dd> <dt>

*ftEndTime* \[ in\]
</dt> <dd>

Tipo: **[ **FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**

Ora di fine dell'attività, in formato UTC. Passare un oggetto [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) impostato su tutti gli zeri se non viene specificata alcuna ora di fine.

</dd> <dt>

*ftDeadline* \[ in\]
</dt> <dd>

Tipo: **[ **FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**

Scadenza dell'attività, in formato UTC. Viene usato per impostare la priorità per più attività che si trovano all'interno della finestra di avvio. Se deve essere avviata più di un'attività, quella con la prima scadenza verrà avviata per prima.

</dd> <dt>

*bstrLabel* \[ in\]
</dt> <dd>

Tipo: **BSTR**

Etichetta per l'attività. Viene passato al metodo [**StartTask**](irdvtaskplugin-starttask.md) .

</dd> <dt>

*bstrIdentifier* \[ in\]
</dt> <dd>

Tipo: **BSTR**

Identificatore dell'attività. Viene passato al metodo [**StartTask**](irdvtaskplugin-starttask.md) .

</dd> <dt>

*saContext* \[ in\]
</dt> <dd>

Tipo: **SAFEARRAY (byte)**

Dati facoltativi per l'attività. Viene passato al metodo [**StartTask**](irdvtaskplugin-starttask.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------|
| Client minimo supportato<br/> | Windows 7 Enterprise<br/>   |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

