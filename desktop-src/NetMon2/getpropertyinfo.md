---
description: La funzione GetPropertyInfo restituisce un puntatore alle informazioni sulle proprietà di un protocollo specificato.
ms.assetid: f65166ba-1d94-4d65-b9d7-edb84ada0826
title: Funzione GetPropertyInfo (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPropertyInfo
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 007332a85f170f865604526199681cad6d68cdcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878650"
---
# <a name="getpropertyinfo-function"></a>Funzione GetPropertyInfo

La funzione **GetPropertyInfo** restituisce un puntatore alle informazioni sulle proprietà di un protocollo specificato.

## <a name="syntax"></a>Sintassi


```C++
LPPROPERTYINFO WINAPI GetPropertyInfo(
  _In_ HPROPERTY hProperty
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hProperty* \[ in\]
</dt> <dd>

Handle per una proprietà.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un puntatore alla proprietà.

Se la funzione ha esito negativo, il valore restituito è **null**.

## <a name="remarks"></a>Commenti

Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **GetPropertyInfo** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




