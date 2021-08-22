---
title: WMDM_SESSION_TYPE enumerazione
description: Il tipo di enumerazione \_ WMDM SESSION TYPE definisce il tipo di \_ sessione.
ms.assetid: e4ed41c0-521f-4da0-8361-287b64d74d77
keywords:
- WMDM_SESSION_TYPE enumerazione windows Media Device Manager
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
ms.openlocfilehash: e4e3d3d774667ca0c7026caa05609efd69443e00c0c2e273a1e6ad0ac086aa9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055529"
---
# <a name="wmdm_session_type-enumeration"></a>Enumerazione SESSION \_ \_ TYPE WMDM

Il **tipo di enumerazione \_ WMDM SESSION \_ TYPE** definisce il tipo di sessione.

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

<span id="WMDM_SESSION_NONE"></span><span id="wmdm_session_none"></span>**SESSIONE WMDM \_ \_ NESSUNA**
</dt> <dd>

La sessione non è definita.

</dd> <dt>

<span id="WMDM_SESSION_TRANSFER_TO_DEVICE"></span><span id="wmdm_session_transfer_to_device"></span>**TRASFERIMENTO DI SESSIONE WMDM \_ \_ AL \_ \_ DISPOSITIVO**
</dt> <dd>

La sessione è definita come trasferimento di dati al dispositivo.

</dd> <dt>

<span id="WMDM_SESSION_TRANSFER_FROM_DEVICE"></span><span id="wmdm_session_transfer_from_device"></span>**TRASFERIMENTO DI SESSIONE WMDM \_ \_ DAL \_ \_ DISPOSITIVO**
</dt> <dd>

La sessione è definita come trasferimento di dati dal dispositivo.

</dd> <dt>

<span id="WMDM_SESSION_DELETE"></span><span id="wmdm_session_delete"></span>**ELIMINAZIONE SESSIONE \_ WMDM \_**
</dt> <dd>

La sessione è definita come eliminazione di dati.

</dd> <dt>

<span id="WMDM_SESSION_CUSTOM"></span><span id="wmdm_session_custom"></span>**SESSIONE WMDM \_ \_ PERSONALIZZATA**
</dt> <dd>

La sessione è definita come sessione personalizzata.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Tipi di enumerazione**](enumeration-types.md)
</dt> </dl>

 

 





