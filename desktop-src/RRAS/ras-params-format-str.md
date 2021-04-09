---
title: Enumerazione RAS_PARAMS_FORMAT (rassapi. h)
description: Il \_ \_ tipo di enumerazione del formato params RAS viene usato nella \_ struttura dei parametri RAS per indicare il tipo di dati associato a una chiave specifica del supporto.
ms.assetid: dd2c0110-1f27-4a8f-bc61-f15588ebc4ca
keywords:
- RAS enumerazione RAS_PARAMS_FORMAT
topic_type:
- apiref
api_name:
- RAS_PARAMS_FORMAT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00065f3781fd2ada420f67367e84e0863fe3b446
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120246"
---
# <a name="ras_params_format-enumeration"></a>\_Enumerazione del formato params RAS \_

\[L'enumerazione del **\_ \_ formato params RAS** non è supportata in Windows Vista.\]

Il tipo di enumerazione del **\_ \_ formato params RAS** viene usato nella struttura dei [**\_ parametri RAS**](ras-parameters-str.md) per indicare il tipo di dati associato a una chiave specifica del supporto.

## <a name="syntax"></a>Sintassi


```C++
typedef enum RAS_PARAMS_FORMAT { 
  ParamNumber  = 0,
  ParamString  = 1
} RAS_PARAMS_FORMAT;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="ParamNumber"></span><span id="paramnumber"></span><span id="PARAMNUMBER"></span>**ParamNumber**
</dt> <dd>

Indica che i dati associati alla chiave sono numerici.

</dd> <dt>

<span id="ParamString"></span><span id="paramstring"></span><span id="PARAMSTRING"></span>**ParamString**
</dt> <dd>

Indica che i dati associati alla chiave sono una stringa.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Rassapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica del servizio di accesso remoto (RAS)](about-remote-access-service.md)
</dt> <dt>

[Enumerazioni di amministrazione del server RAS](ras-server-administration-enumerations.md)
</dt> <dt>

[**\_parametri RAS**](ras-parameters-str.md)
</dt> </dl>

 

 





