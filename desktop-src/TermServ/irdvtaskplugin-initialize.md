---
title: Metodo IRDVTaskPlugin Initialize
description: Chiamato per inizializzare l'agente attività.
ms.assetid: eef813e6-ecca-400a-a9f3-efca6bd81161
ms.tgt_platform: multiple
keywords:
- Inizializzare il Servizi Desktop remoto
- Inizializzare il Servizi Desktop remoto, interfaccia IRDVTaskPlugin
- Interfaccia IRDVTaskPlugin Servizi Desktop remoto , metodo Initialize
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.Initialize
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c14f4a002a0b33e403c02dba74385edd21e211fb27bcfb144c7a9ddc080a40fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606104"
---
# <a name="irdvtaskplugininitialize-method"></a>Metodo IRDVTaskPlugin::Initialize

Chiamato per inizializzare l'agente attività.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Initialize(
  [in] IRDVTaskPluginNotifySink *pNotifySink
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pNotifySink* \[ Pollici\]
</dt> <dd>

Tipo: **[ **IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md)\***

Puntatore a [**un'interfaccia IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md) utilizzata dall'agente attività per comunicare con l'agente trigger. È necessario rilasciare questa interfaccia quando non è più necessaria.

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

[**IRDVTaskPlugin**](irdvtaskplugin.md)
</dt> </dl>

 

 





