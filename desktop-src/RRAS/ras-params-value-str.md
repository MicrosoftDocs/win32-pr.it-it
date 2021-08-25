---
title: RAS_PARAMS_VALUE union (Rassapi.h)
description: L'unione VALORE PARAMS RAS viene usata nella struttura PARAMETRI RAS per archiviare i dati \_ associati a un parametro specifico del \_ \_ supporto.
ms.assetid: 43284ee4-9bd4-4019-860f-0fb7ff3f38ee
keywords:
- RAS_PARAMS_VALUE ras dell'unione
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
ms.openlocfilehash: 07453b707012c966fc298cc61973cb056b42d741d861a22204c17eec5265317f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909601"
---
# <a name="ras_params_value-union"></a>Unione DI VALORI DI RAS \_ PARAMS \_

\[**L'unione DI \_ VALORI \_ PARAMS RAS** non è supportata a Windows Vista.\]

**\_ L'unione \_ VALORE PARAMS RAS** viene usata nella [**struttura \_ PARAMETRI RAS**](ras-parameters-str.md) per archiviare i dati associati a un parametro specifico del supporto. Il **membro P \_ Type** della **struttura RAS \_ PARAMETERS** usa un valore dell'enumerazione [**RAS \_ PARAMS \_ FORMAT**](ras-params-format-str.md) per indicare il tipo di valore attualmente archiviato in **RAS \_ PARAMS \_ VALUE**.

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

Se il **membro P \_ Type** della [**struttura RAS \_ PARAMETERS**](ras-parameters-str.md) è ParamNumber, il **membro Number** contiene il valore del parametro specifico del supporto. Ad esempio, il parametro MAXCONNECTBPS è di tipo ParamNumber e il valore potrebbe essere 19200.

Se il **membro P \_ Type** della [**struttura RAS \_ PARAMETERS**](ras-parameters-str.md) è ParamNumber, il **membro Number** contiene il valore del parametro specifico del supporto. Ad esempio, il parametro MAXCONNECTBPS è di tipo ParamNumber e il valore potrebbe essere 19200.

</dd> <dt>

**Stringa**
</dt> <dd>

Se il **membro \_ P Type** della struttura RAS [**\_ PARAMETERS**](ras-parameters-str.md) è ParamString, il **membro String** contiene il valore del parametro specifico del supporto.

<dl> <dt>

**Length**
</dt> <dd>

Specifica la lunghezza, in caratteri, della stringa a cui punta il **membro** Dati.

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
| Intestazione<br/>                   | <dl> <dt>Rassapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica del servizio di accesso remoto (RAS)](about-remote-access-service.md)
</dt> <dt>

[Unione amministrazione server RAS](ras-server-administration-union.md)
</dt> <dt>

[**PARAMETRI \_ RAS**](ras-parameters-str.md)
</dt> <dt>

[**FORMATO \_ PARAMS \_ RAS**](ras-params-format-str.md)
</dt> </dl>

 

 





