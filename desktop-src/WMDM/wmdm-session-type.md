---
title: Enumerazione WMDM_SESSION_TYPE
description: Il tipo di \_ enumerazione del tipo di sessione WMDM \_ definisce il tipo di sessione.
ms.assetid: e4ed41c0-521f-4da0-8361-287b64d74d77
keywords:
- Enumerazione WMDM_SESSION_TYPE Windows Media Gestione dispositivi
topic_type:
- apiref
api_name:
- WMDM_SESSION_TYPE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84322986266143e5ff4ecc469c56504f29de9e3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325271"
---
# <a name="wmdm_session_type-enumeration"></a>Enumerazione del tipo di \_ sessione WMDM \_

Il tipo di enumerazione del **\_ \_ tipo di sessione WMDM** definisce il tipo di sessione.

## <a name="syntax"></a>Sintassi


```C++
typedef enum tagWMDM_SESSION_TYPE { 
  WMDM_SESSION_NONE,
  WMDM_SESSION_TRANSFER_TO_DEVICE,
  WMDM_SESSION_TRANSFER_FROM_DEVICE,
  WMDM_SESSION_DELETE,
  WMDM_SESSION_CUSTOM
} WMDM_SESSION_TYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="WMDM_SESSION_NONE"></span><span id="wmdm_session_none"></span>**WMDM \_ sessione \_ None**
</dt> <dd>

La sessione non è definita.

</dd> <dt>

<span id="WMDM_SESSION_TRANSFER_TO_DEVICE"></span><span id="wmdm_session_transfer_to_device"></span>**\_trasferimento della sessione WMDM \_ \_ al \_ dispositivo**
</dt> <dd>

La sessione viene definita come trasferimento dei dati al dispositivo.

</dd> <dt>

<span id="WMDM_SESSION_TRANSFER_FROM_DEVICE"></span><span id="wmdm_session_transfer_from_device"></span>**\_ \_ trasferimento della sessione WMDM \_ dal \_ dispositivo**
</dt> <dd>

La sessione viene definita come trasferimento dei dati dal dispositivo.

</dd> <dt>

<span id="WMDM_SESSION_DELETE"></span><span id="wmdm_session_delete"></span>**\_eliminazione della sessione WMDM \_**
</dt> <dd>

La sessione è definita come eliminazione dei dati.

</dd> <dt>

<span id="WMDM_SESSION_CUSTOM"></span><span id="wmdm_session_custom"></span>**\_personalizzata della sessione WMDM \_**
</dt> <dd>

La sessione viene definita come sessione personalizzata.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Tipi di enumerazione**](enumeration-types.md)
</dt> </dl>

 

 





