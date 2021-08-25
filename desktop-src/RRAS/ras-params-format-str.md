---
title: RAS_PARAMS_FORMAT enumerazione (Rassapi.h)
description: Il tipo di enumerazione RAS PARAMS FORMAT viene usato nella struttura PARAMETRI RAS per indicare il tipo di dati \_ associati a una chiave specifica del \_ \_ supporto.
ms.assetid: dd2c0110-1f27-4a8f-bc61-f15588ebc4ca
keywords:
- RAS_PARAMS_FORMAT enumerazione RAS
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
ms.openlocfilehash: 92b798ef8a5257afcb4e4ad653801bda0d21691057abad970d6e8158f592146e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673181"
---
# <a name="ras_params_format-enumeration"></a>Enumerazione \_ RAS PARAMS \_ FORMAT

\[**\_ L'enumerazione \_ RAS PARAMS FORMAT** non è supportata a Windows Vista.\]

Il **tipo di enumerazione RAS \_ PARAMS \_ FORMAT** viene usato nella [**struttura \_ PARAMETRI RAS**](ras-parameters-str.md) per indicare il tipo di dati associati a una chiave specifica del supporto.

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

Indica che i dati associati alla chiave sono un numero.

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
| Intestazione<br/>                   | <dl> <dt>Rassapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica del servizio di accesso remoto (RAS)](about-remote-access-service.md)
</dt> <dt>

[Enumerazioni di amministrazione del server RAS](ras-server-administration-enumerations.md)
</dt> <dt>

[**PARAMETRI \_ RAS**](ras-parameters-str.md)
</dt> </dl>

 

 





