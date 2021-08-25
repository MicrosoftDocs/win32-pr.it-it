---
title: Enumerazione WMDMMessage
description: Il tipo di enumerazione WMDMMessage definisce i tipi di messaggio e gli stati.
ms.assetid: 49a77100-8890-4e40-852f-c6fd436f22c5
keywords:
- Enumerazione WMDMMessage windows Media Device Manager
topic_type:
- apiref
api_name:
- WMDMMessage
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 348092e079428e0b147d8143411cee7766365913115f968ed0e112b209383077
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862661"
---
# <a name="wmdmmessage-enumeration"></a>Enumerazione WMDMMessage

Il **tipo di enumerazione WMDMMessage** definisce i tipi di messaggio e gli stati.

## <a name="syntax"></a>Sintassi


```C++
enum WMDMMessage {
  WMDM_MSG_DEVICE_ARRIVAL, 
  WMDM_MSG_DEVICE_REMOVAL, 
  WMDM_MSG_MEDIA_ARRIVAL, 
  WMDM_MSG_MEDIA_REMOVAL 

};
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="WMDM_MSG_DEVICE_ARRIVAL"></span><span id="wmdm_msg_device_arrival"></span>**ARRIVO DEL DISPOSITIVO \_ WMDM MSG \_ \_**
</dt> <dd>

È Windows un dispositivo di Gestione dispositivi multimediali collegato.

</dd> <dt>

<span id="WMDM_MSG_DEVICE_REMOVAL"></span><span id="wmdm_msg_device_removal"></span>**RIMOZIONE DEL DISPOSITIVO MSG WMDM \_ \_ \_**
</dt> <dd>

È Windows un dispositivo di Gestione dispositivi multimediali.

</dd> <dt>

<span id="WMDM_MSG_MEDIA_ARRIVAL"></span><span id="wmdm_msg_media_arrival"></span>**WMDM \_ MSG \_ MEDIA \_ ARRIVAL**
</dt> <dd>

Il supporto è stato inserito in un Windows Gestione dispositivi multimediali.

</dd> <dt>

<span id="WMDM_MSG_MEDIA_REMOVAL"></span><span id="wmdm_msg_media_removal"></span>**RIMOZIONE DI SUPPORTI \_ WMDM MSG \_ \_**
</dt> <dd>

Il supporto è stato rimosso da un Windows Gestione dispositivi multimediali.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Tipi di enumerazione**](enumeration-types.md)
</dt> </dl>

 

 





