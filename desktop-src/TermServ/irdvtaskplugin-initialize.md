---
title: Metodo Initialize IRDVTaskPlugin
description: Chiamato per inizializzare l'agente attività.
ms.assetid: eef813e6-ecca-400a-a9f3-efca6bd81161
ms.tgt_platform: multiple
keywords:
- Inizializzare il metodo Servizi Desktop remoto
- Metodo Initialize Servizi Desktop remoto, interfaccia IRDVTaskPlugin
- Interfaccia IRDVTaskPlugin Servizi Desktop remoto, metodo Initialize
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.Initialize
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9530be7334e1f3fefa7f73007334e448362a95ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400373"
---
# <a name="irdvtaskplugininitialize-method"></a>Metodo IRDVTaskPlugin:: Initialize

Chiamato per inizializzare l'agente attività.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Initialize(
  [in] IRDVTaskPluginNotifySink *pNotifySink
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pNotifySink* \[ in\]
</dt> <dd>

Tipo: **[**IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md) \** _

Puntatore a un'interfaccia [_ *IRDVTaskPluginNotifySink* *](irdvtaskpluginnotifysink.md) che l'agente attività utilizza per comunicare con l'agente di trigger. È necessario rilasciare questa interfaccia quando non è più necessaria.

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

[**IRDVTaskPlugin**](irdvtaskplugin.md)
</dt> </dl>

 

 





