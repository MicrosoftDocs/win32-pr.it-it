---
title: Enumerazione MP_FASTPATH_TYPE (MpClient. h)
description: Tipo FastPath.
ms.assetid: BD72228F-DCC0-435E-A408-BD7FB02E55E1
keywords:
- Funzionalità dell'ambiente Windows legacy dell'enumerazione MP_FASTPATH_TYPE
- Caratteristiche dell'ambiente Windows legacy del puntatore di enumerazione PMP_FASTPATH_TYPE
topic_type:
- apiref
api_name:
- MP_FASTPATH_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e89db79c54b166a833369ff52e47473463e0a2b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121170"
---
# <a name="mp_fastpath_type-enumeration"></a>\_Enumerazione del \_ tipo MP FastPath

Tipo FastPath.

## <a name="syntax"></a>Sintassi


```C++
typedef enum tagMP_FASTPATH_TYPE { 
  MP_FASTPATH_UNKNOWN   = 0,
  MP_FASTPATH_VDM       = 1,
  MP_FASTPATH_DISABLED  = 2
} MP_FASTPATH_TYPE, *PMP_FASTPATH_TYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="MP_FASTPATH_UNKNOWN"></span><span id="mp_fastpath_unknown"></span>**MP \_ FastPath \_ sconosciuto**
</dt> <dd>

Sconosciuto.

</dd> <dt>

<span id="MP_FASTPATH_VDM"></span><span id="mp_fastpath_vdm"></span>**\_VDM FastPath \_ MP**
</dt> <dd>

Aggiornamento di VDM.

</dd> <dt>

<span id="MP_FASTPATH_DISABLED"></span><span id="mp_fastpath_disabled"></span>**\_FastPath MP \_ disabilitato**
</dt> <dd>

Notifica di disabilitazione della firma.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





