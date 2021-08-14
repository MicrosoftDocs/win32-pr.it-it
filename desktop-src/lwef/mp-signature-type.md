---
title: MP_SIGNATURE_TYPE enumerazione (MpClient.h)
description: Tipi di firma possibili.
ms.assetid: 44B195A8-866D-4B87-9576-54E00658F9B3
keywords:
- MP_SIGNATURE_TYPE di enumerazione Legacy Windows Environment Features
- PMP_SIGNATURE_TYPE puntatore di enumerazione Legacy Windows Environment Features
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
ms.openlocfilehash: 3289f0cbc3eeb85f553adf97078b7d3c5c53a686e914f86a4edb80c5244f72af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883714"
---
# <a name="mp_signature_type-enumeration"></a>Enumerazione \_ MP SIGNATURE \_ TYPE

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

<span id="MP_SIGNATURE_ANTIMALWARE"></span><span id="mp_signature_antimalware"></span>**\_ANTIMALWARE DI \_ FIRMA MP**
</dt> <dd>

Firme antivirus e antispyware.

</dd> <dt>

<span id="MP_SIGNATURE_ANTIVIRUS"></span><span id="mp_signature_antivirus"></span>**\_ANTIVIRUS PER LA FIRMA \_ MP**
</dt> <dd>

Solo firme antivirus.

</dd> <dt>

<span id="MP_SIGNATURE_ANTISPYWARE"></span><span id="mp_signature_antispyware"></span>**\_ \_ ANTISPYWARE PER LA FIRMA MP**
</dt> <dd>

Solo firme antispyware.

</dd> <dt>

<span id="MP_SIGNATURE_NIS"></span><span id="mp_signature_nis"></span>**NIS \_ DI \_ FIRMA MP**
</dt> <dd>

Firme NIS.

</dd> <dt>

<span id="MP_SIGNATURE_TYPES_MAXVALUE"></span><span id="mp_signature_types_maxvalue"></span>**MAXVALUE \_ TIPI \_ DI FIRMA \_ MP**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





