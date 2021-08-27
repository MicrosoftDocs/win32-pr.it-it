---
title: MPHEALTH_DATA struttura (MpClient.h)
description: Dati di notifica dell'integrità.
ms.assetid: 37A87F77-386A-4508-B338-ED2151518968
keywords:
- MPHEALTH_DATA struttura Legacy Windows Environment Features
- PMPHEALTH_DATA puntatore alla struttura Legacy Windows Environment Features
topic_type:
- apiref
api_name:
- MPHEALTH_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb04224d38e639d053b8e20370e2b0db0dc15f44cc647e7205911362112e4a49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976001"
---
# <a name="mphealth_data-structure"></a>Struttura MPHEALTH \_ DATA

Dati di notifica dell'integrità.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMPHEALTH_DATA {
  DWORD dwNotificationType;
  DWORD dwNotificationFlag;
} MPHEALTH_DATA, *PMPHEALTH_DATA;
```



## <a name="members"></a>Members

<dl> <dt>

**dwNotificationType**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Tipo di notifica.

</dd> <dt>

**dwNotificationFlag**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Non utilizzato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





