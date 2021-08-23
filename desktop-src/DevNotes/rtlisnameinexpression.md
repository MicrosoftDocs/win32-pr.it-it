---
description: Determina se una stringa Unicode corrisponde al modello specificato.
ms.assetid: 9b220cb8-4402-4094-8209-59a9af004b4a
title: Funzione RtlIsNameInExpression
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
ms.openlocfilehash: 8d59968bd32a7ab60d5a739f6c4be2d99d5a9ed63e13069fe1824e9b41e029ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119541491"
---
# <a name="rtlisnameinexpression-function"></a>Funzione RtlIsNameInExpression

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

*Espressione* \[ Pollici\]
</dt> <dd>

Puntatore alla stringa del modello. Questa stringa può contenere caratteri jolly. Se il *parametro IgnoreCase* è TRUE, la stringa deve contenere solo caratteri maiuscoli.

</dd> <dt>

*Nome* \[ Pollici\]
</dt> <dd>

Puntatore alla stringa da confrontare con il modello. Questa stringa non può contenere caratteri jolly.

</dd> <dt>

*IgnoreCase* \[ Pollici\]
</dt> <dd>

**TRUE per** la corrispondenza senza distinzione tra maiuscole e minuscole o **FALSE** per la corrispondenza con distinzione tra maiuscole e minuscole.

</dd> <dt>

*UpcaseTable* \[ in, facoltativo\]
</dt> <dd>

Puntatore facoltativo a una tabella di caratteri maiuscoli da utilizzare per la corrispondenza senza distinzione tra maiuscole e minuscole. Se questo parametro è NULL, viene usata la tabella dei caratteri maiuscoli di sistema predefinita.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE** se la stringa corrisponde al criterio. Se la stringa non corrisponde al modello, questa funzione restituisce **FALSE.**

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file di intestazione. La libreria di importazione associata, Ntdll.lib, è disponibile in Microsoft Windows Driver Kit (WDK). È anche possibile chiamare questa funzione usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegarsi dinamicamente Ntdll.dll.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                              |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
