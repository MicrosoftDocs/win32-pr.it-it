---
title: Metodo IRDVTaskPluginNotifySink DeleteSchedule
description: Chiamato dall'agente attività per eliminare un'attività pianificata.
ms.assetid: 67a9493e-367a-48c9-8f94-276d696406b7
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del Metodo DeleteSchedule
- Metodo DeleteSchedule Servizi Desktop remoto, interfaccia IRDVTaskPluginNotifySink
- Interfaccia IRDVTaskPluginNotifySink Servizi Desktop remoto, Metodo DeleteSchedule
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.DeleteSchedule
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f00bcc740f87acb7f051decd5f2fc9b55ffbf642
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121430"
---
# <a name="irdvtaskpluginnotifysinkdeleteschedule-method"></a>IRDVTaskPluginNotifySink::D Metodo eleteSchedule

Chiamato dall'agente attività per eliminare un'attività pianificata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DeleteSchedule(
  [in] BSTR bstrIdentifier
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrIdentifier* \[ in\]
</dt> <dd>

Identificatore dell'attività pianificata.

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

[**IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

 





