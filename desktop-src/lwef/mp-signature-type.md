---
title: Enumerazione MP_SIGNATURE_TYPE (MpClient. h)
description: Tipi di firma possibili.
ms.assetid: 44B195A8-866D-4B87-9576-54E00658F9B3
keywords:
- Funzionalità dell'ambiente Windows legacy dell'enumerazione MP_SIGNATURE_TYPE
- Caratteristiche dell'ambiente Windows legacy del puntatore di enumerazione PMP_SIGNATURE_TYPE
topic_type:
- apiref
api_name:
- MP_SIGNATURE_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b99f7140706e9a6d3fa32e7eb346ef6478f3f26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476504"
---
# <a name="mp_signature_type-enumeration"></a>Enumerazione del tipo di \_ firma MP \_

Tipi di firma possibili.

## <a name="syntax"></a>Sintassi


```C++
typedef enum tagMP_SIGNATURE_TYPE { 
  MP_SIGNATURE_ANTIMALWARE     = 0,
  MP_SIGNATURE_ANTIVIRUS       = 1,
  MP_SIGNATURE_ANTISPYWARE     = 2,
  MP_SIGNATURE_NIS             = 3,
  MP_SIGNATURE_TYPES_MAXVALUE  = 3
} MP_SIGNATURE_TYPE, *PMP_SIGNATURE_TYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="MP_SIGNATURE_ANTIMALWARE"></span><span id="mp_signature_antimalware"></span>**\_antimalware firma MP \_**
</dt> <dd>

Firme antivirus e antispyware.

</dd> <dt>

<span id="MP_SIGNATURE_ANTIVIRUS"></span><span id="mp_signature_antivirus"></span>**ANTIVIRUS per la \_ firma MP \_**
</dt> <dd>

Solo le firme antivirus.

</dd> <dt>

<span id="MP_SIGNATURE_ANTISPYWARE"></span><span id="mp_signature_antispyware"></span>**\_antispyware firma MP \_**
</dt> <dd>

Solo le firme antispyware.

</dd> <dt>

<span id="MP_SIGNATURE_NIS"></span><span id="mp_signature_nis"></span>**\_NIS firma \_ MP**
</dt> <dd>

Firme NIS.

</dd> <dt>

<span id="MP_SIGNATURE_TYPES_MAXVALUE"></span><span id="mp_signature_types_maxvalue"></span>**\_tipi di firma MP \_ \_ MaxValue**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





