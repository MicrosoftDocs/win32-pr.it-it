---
description: La funzione DestroyHandoffTable Elimina una tabella di continuità creata con CreateHandoffTable.
ms.assetid: 01ae9899-4f7c-4706-a2ce-9f55b112351d
title: Funzione DestroyHandoffTable (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyHandoffTable
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7afccfd1932c57b2a0d77dbb5467afc31726c6fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967400"
---
# <a name="destroyhandofftable-function"></a>DestroyHandoffTable (funzione)

La funzione **DestroyHandoffTable** Elimina una tabella di continuità creata con **CreateHandoffTable**.

## <a name="syntax"></a>Sintassi


```C++
VOID WINAPI DestroyHandoffTable(
  _In_ LPHANDOFFTABLE hTable
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hTable* \[ in\]
</dt> <dd>

Handle per la tabella di continuità eliminata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessuna.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




