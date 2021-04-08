---
title: Proprietà IRDVTaskPlugin pluginName (Tspubplugincom. h)
description: Contiene il nome visualizzato dell'agente attività.
ms.assetid: 6f414270-e90b-4075-80fe-f918acbdd205
ms.tgt_platform: multiple
keywords:
- Proprietà pluginName Servizi Desktop remoto
- Servizi Desktop remoto proprietà pluginName, interfaccia IRDVTaskPlugin
- Interfaccia IRDVTaskPlugin Servizi Desktop remoto, proprietà pluginName
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.PluginName
- IRDVTaskPlugin.get_PluginName
api_location:
- tspubplugincom.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0262472e37a8ff3e5b9bb153d2e94f4e52029b14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742074"
---
# <a name="irdvtaskpluginpluginname-property"></a>IRDVTaskPlugin::P proprietà luginName

Contiene il nome visualizzato dell'agente attività. Questo nome viene utilizzato solo a scopo di registrazione.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_PluginName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Valore proprietà

Nome visualizzato dell'agente attività.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 Enterprise<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Tspubplugincom. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IRDVTaskPlugin**](irdvtaskplugin.md)
</dt> </dl>

 

 





