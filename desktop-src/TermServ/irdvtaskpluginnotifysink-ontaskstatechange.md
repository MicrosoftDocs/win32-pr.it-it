---
title: Metodo IRDVTaskPluginNotifySink OnTaskStateChange
description: Utilizzato per notificare all'agente del trigger che lo stato di un'attività è stato modificato.
ms.assetid: 3021ea7a-2627-48d1-8df5-c40e7a9b51c5
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnTaskStateChange
- Metodo OnTaskStateChange Servizi Desktop remoto, interfaccia IRDVTaskPluginNotifySink
- Interfaccia IRDVTaskPluginNotifySink Servizi Desktop remoto, metodo OnTaskStateChange
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.OnTaskStateChange
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c3e3acf1a2d47b1721ef90554f7a11714c02e6df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302574"
---
# <a name="irdvtaskpluginnotifysinkontaskstatechange-method"></a>Metodo IRDVTaskPluginNotifySink:: OnTaskStateChange

Utilizzato per notificare all'agente del trigger che lo stato di un'attività è stato modificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT OnTaskStateChange(
  [in] BSTR            bstrIdentifier,
  [in] RDV_TASK_STATUS status
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrIdentifier* \[ in\]
</dt> <dd>

Tipo: **BSTR**

Identificatore dell'attività. Si tratta dell'identificatore passato al metodo [**StartTask**](irdvtaskplugin-starttask.md) .

</dd> <dt>

*stato* \[ di in\]
</dt> <dd>

Tipo: **[ **\_ \_ stato attività RDV**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status)**

Valore dell'enumerazione dello [**\_ \_ stato dell'attività RDV**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) che specifica il nuovo stato dell'attività.

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

[**\_stato attività \_ RDV**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status)
</dt> <dt>

[**IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

 





