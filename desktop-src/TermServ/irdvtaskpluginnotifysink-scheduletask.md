---
title: Metodo IRDVTaskPluginNotifySink ScheduleTask
description: Chiamato dall'agente attività per pianificare un'attività.
ms.assetid: 06793439-cf16-40ca-8a91-08acc22c73ed
ms.tgt_platform: multiple
keywords:
- Metodo ScheduleTask Servizi Desktop remoto
- Metodo ScheduleTask Servizi Desktop remoto, interfaccia IRDVTaskPluginNotifySink
- Interfaccia IRDVTaskPluginNotifySink Servizi Desktop remoto , metodo ScheduleTask
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.ScheduleTask
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fdcecba38b1fd5eb773e5076f5485ae900e5423267a3a311091bf01e0ed86ac0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512021"
---
# <a name="irdvtaskpluginnotifysinkscheduletask-method"></a>Metodo IRDVTaskPluginNotifySink::ScheduleTask

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

*ftStartTime* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**

Ora di inizio meno recente dell'attività, in formato UTC.

</dd> <dt>

*ftEndTime* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**

Ora di fine dell'attività, in formato UTC. Passare un [**valore FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) impostato su tutti gli zeri se non viene specificata alcuna ora di fine.

</dd> <dt>

*ftDeadline* \[ Pollici\]
</dt> <dd>

Tipo: **[ **FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**

Scadenza dell'attività, in formato UTC. Viene usato per impostare la priorità per più attività all'interno della finestra iniziale. Se devono essere avviate più attività, verrà avviata per prima quella con la scadenza meno recente.

</dd> <dt>

*bstrLabel* \[ Pollici\]
</dt> <dd>

Tipo: **BSTR**

Etichetta per l'attività. Viene passato al [**metodo StartTask.**](irdvtaskplugin-starttask.md)

</dd> <dt>

*bstrIdentifier* \[ Pollici\]
</dt> <dd>

Tipo: **BSTR**

Identificatore dell'attività. Viene passato al [**metodo StartTask.**](irdvtaskplugin-starttask.md)

</dd> <dt>

*saContext* \[ Pollici\]
</dt> <dd>

Tipo: **SAFEARRAY(BYTE)**

Dati facoltativi per l'attività. Viene passato al [**metodo StartTask.**](irdvtaskplugin-starttask.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------|
| Client minimo supportato<br/> | Windows 7 Enterprise<br/>   |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

