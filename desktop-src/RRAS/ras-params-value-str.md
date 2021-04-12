---
title: Unione RAS_PARAMS_VALUE (rassapi. h)
description: L' \_ Unione del valore params RAS \_ viene utilizzata nella \_ struttura dei parametri RAS per archiviare i dati associati a un parametro specifico del supporto.
ms.assetid: 43284ee4-9bd4-4019-860f-0fb7ff3f38ee
keywords:
- RAS Unione RAS_PARAMS_VALUE
topic_type:
- apiref
api_name:
- RAS_PARAMS_VALUE
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6f8cc6d693b32b1bbe6f05e8d32ca31a48cfb29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104118938"
---
# <a name="ras_params_value-union"></a>\_Unione valore params RAS \_

\[L'Unione del **\_ \_ valore params RAS** non è supportata a partire da Windows Vista.\]

L'Unione del **\_ \_ valore params RAS** viene utilizzata nella struttura dei [**\_ parametri RAS**](ras-parameters-str.md) per archiviare i dati associati a un parametro specifico del supporto. Il membro di **\_ tipo P** della struttura dei **\_ parametri RAS** usa un valore dell'enumerazione del [**\_ \_ formato params RAS**](ras-params-format-str.md) per indicare il tipo di valore attualmente archiviato **nel \_ \_ valore params RAS**.

## <a name="syntax"></a>Sintassi


```C++
typedef union RAS_PARAMS_VALUE {
  DWORD  Number;
  struct {
    DWORD Length;
    PCHAR Data;
  } String;
} RAS_PARAMS_VALUE;
```



## <a name="members"></a>Members

<dl> <dt>

**Number**
</dt> <dd>

Se il membro di **\_ tipo P** della struttura dei [**\_ parametri RAS**](ras-parameters-str.md) è ParamNumber, il membro **Number** contiene il valore del parametro specifico del supporto. Ad esempio, il parametro MAXCONNECTBPS è di tipo ParamNumber e il valore potrebbe essere 19200.

Se il membro di **\_ tipo P** della struttura dei [**\_ parametri RAS**](ras-parameters-str.md) è ParamNumber, il membro **Number** contiene il valore del parametro specifico del supporto. Ad esempio, il parametro MAXCONNECTBPS è di tipo ParamNumber e il valore potrebbe essere 19200.

</dd> <dt>

**Stringa**
</dt> <dd>

Se il membro di **\_ tipo P** della struttura dei [**\_ parametri RAS**](ras-parameters-str.md) è ParamString, il membro della **stringa** contiene il valore del parametro specifico del supporto.

<dl> <dt>

**Length**
</dt> <dd>

Specifica la lunghezza, in caratteri, della stringa a cui punta il membro **dati** .

</dd> <dt>

**Dati**
</dt> <dd>

Puntatore a un buffer che contiene il valore stringa di un parametro specifico del supporto.

</dd> </dl> </dd> </dl>

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

[Unione di amministrazione del server RAS](ras-server-administration-union.md)
</dt> <dt>

[**\_parametri RAS**](ras-parameters-str.md)
</dt> <dt>

[**\_formato params \_ RAS**](ras-params-format-str.md)
</dt> </dl>

 

 





