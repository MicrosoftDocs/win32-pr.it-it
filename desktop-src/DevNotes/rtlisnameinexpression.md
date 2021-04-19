---
description: Determina se una stringa Unicode corrisponde al modello specificato.
ms.assetid: 9b220cb8-4402-4094-8209-59a9af004b4a
title: RtlIsNameInExpression (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlIsNameInExpression
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: ac6142b364a135b62505841963fa799ce6603dbe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304654"
---
# <a name="rtlisnameinexpression-function"></a>RtlIsNameInExpression (funzione)

Determina se una stringa Unicode corrisponde al modello specificato.

## <a name="syntax"></a>Sintassi


```C++
 BOOLEAN  RtlIsNameInExpression(
  _In_     PUNICODE_STRING Expression,
  _In_     PUNICODE_STRING Name,
  _In_     BOOLEAN         IgnoreCase,
  _In_opt_ PWCH            UpcaseTable
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Espressione* \[ in\]
</dt> <dd>

Puntatore alla stringa del modello. Questa stringa può contenere caratteri jolly. Se il parametro *IgnoreCase* è true, la stringa deve contenere solo caratteri maiuscoli.

</dd> <dt>

*Nome* \[ in\]
</dt> <dd>

Puntatore alla stringa da confrontare con il modello. Questa stringa non può contenere caratteri jolly.

</dd> <dt>

*IgnoreCase* \[ in\]
</dt> <dd>

**True** per la corrispondenza senza distinzione tra maiuscole e minuscole o **false** per corrispondenza con distinzione tra maiuscole e minuscole

</dd> <dt>

*UpcaseTable* \[ in, facoltativo\]
</dt> <dd>

Puntatore facoltativo a una tabella caratteri maiuscola da usare per la corrispondenza senza distinzione tra maiuscole e minuscole. Se questo parametro è NULL, viene utilizzata la tabella dei caratteri maiuscoli di sistema predefinita.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se la stringa corrisponde al modello. Se la stringa non corrisponde al modello, la funzione restituisce **false**.

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file di intestazione. La libreria di importazione associata, Ntdll. lib, è disponibile in Microsoft Windows Driver Kit (WDK). È anche possibile chiamare questa funzione usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Ntdll.dll.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                           |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                              |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
