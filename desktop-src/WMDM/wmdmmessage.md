---
title: Enumerazione WMDMMessage
description: Il tipo di enumerazione WMDMMessage definisce i tipi e gli Stati dei messaggi.
ms.assetid: 49a77100-8890-4e40-852f-c6fd436f22c5
keywords:
- Enumerazione WMDMMessage Windows Media Gestione dispositivi
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
ms.openlocfilehash: 7489dc7059f10e1a6f61d1a290f8f664a385f96c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325005"
---
# <a name="wmdmmessage-enumeration"></a>Enumerazione WMDMMessage

Il tipo di enumerazione **WMDMMessage** definisce i tipi e gli Stati dei messaggi.

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

<span id="WMDM_MSG_DEVICE_ARRIVAL"></span><span id="wmdm_msg_device_arrival"></span>**\_arrivo del \_ dispositivo \_ msg WMDM**
</dt> <dd>

Un dispositivo Windows Media Gestione dispositivi è stato collegato.

</dd> <dt>

<span id="WMDM_MSG_DEVICE_REMOVAL"></span><span id="wmdm_msg_device_removal"></span>**\_rimozione del \_ dispositivo \_ msg WMDM**
</dt> <dd>

Un dispositivo Windows Media Gestione dispositivi è stato rimosso.

</dd> <dt>

<span id="WMDM_MSG_MEDIA_ARRIVAL"></span><span id="wmdm_msg_media_arrival"></span>**\_arrivo del \_ supporto \_ messaggi WMDM**
</dt> <dd>

Il supporto è stato inserito in un dispositivo Windows Media Gestione dispositivi.

</dd> <dt>

<span id="WMDM_MSG_MEDIA_REMOVAL"></span><span id="wmdm_msg_media_removal"></span>**\_rimozione del \_ supporto \_ messaggi WMDM**
</dt> <dd>

Il supporto è stato rimosso da un dispositivo Windows Media Gestione dispositivi.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Tipi di enumerazione**](enumeration-types.md)
</dt> </dl>

 

 





