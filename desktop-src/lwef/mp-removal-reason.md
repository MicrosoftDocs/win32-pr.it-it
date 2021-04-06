---
title: Enumerazione MP_REMOVAL_REASON (MpClient. h)
description: Motivo della rimozione della firma FastPath.
ms.assetid: A09B4903-E53C-4DA1-BD0B-6DE0124FCAB3
keywords:
- Funzionalità dell'ambiente Windows legacy dell'enumerazione MP_REMOVAL_REASON
- Caratteristiche dell'ambiente Windows legacy del puntatore di enumerazione PMP_REMOVAL_REASON
topic_type:
- apiref
api_name:
- MP_REMOVAL_REASON
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03ce70f46bd95d4183343990b40594326ed5d3b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743186"
---
# <a name="mp_removal_reason-enumeration"></a>Enumerazione del motivo della \_ rimozione MP \_

Motivo della rimozione della firma FastPath.

## <a name="syntax"></a>Sintassi


```C++
typedef enum tagMP_REMOVAL_REASON { 
  MP_REMOVAL_UNKNOWN    = 0,
  MP_REMOVAL_MANUAL     = 1,
  MP_REMOVAL_AUTOMATIC  = 2
} MP_REMOVAL_REASON, *PMP_REMOVAL_REASON;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="MP_REMOVAL_UNKNOWN"></span><span id="mp_removal_unknown"></span>**\_rimozione MP \_ sconosciuta**
</dt> <dd>

Sconosciuto.

</dd> <dt>

<span id="MP_REMOVAL_MANUAL"></span><span id="mp_removal_manual"></span>**\_Manuale di rimozione MP \_**
</dt> <dd>

manuale.

</dd> <dt>

<span id="MP_REMOVAL_AUTOMATIC"></span><span id="mp_removal_automatic"></span>**\_rimozione MP \_ automatica**
</dt> <dd>

Automatico.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





