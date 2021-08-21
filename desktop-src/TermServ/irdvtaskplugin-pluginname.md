---
title: Proprietà PluginName IRDVTaskPlugin (Tspubplugincom.h)
description: Contiene il nome visualizzato dell'agente attività.
ms.assetid: 6f414270-e90b-4075-80fe-f918acbdd205
ms.tgt_platform: multiple
keywords:
- Proprietà PluginName Servizi Desktop remoto
- Proprietà PluginName Servizi Desktop remoto, interfaccia IRDVTaskPlugin
- Interfaccia IRDVTaskPlugin Servizi Desktop remoto , proprietà PluginName
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
ms.openlocfilehash: 078934c8f19085bf233df78501798a8416ceadf7ba6a0b663cb14b8a8c46b223
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129332"
---
# <a name="irdvtaskpluginpluginname-property"></a>Proprietà IRDVTaskPlugin::P luginName

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
| Intestazione<br/>                   | <dl> <dt>Tspubplugincom.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IRDVTaskPlugin**](irdvtaskplugin.md)
</dt> </dl>

 

 





