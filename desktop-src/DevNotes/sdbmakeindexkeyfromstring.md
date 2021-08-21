---
description: Crea una chiave da una stringa.
ms.assetid: 107138b9-96f0-4144-a4bc-7115b6deab60
title: Funzione SdbMakeIndexKeyFromString
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbMakeIndexKeyFromString
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 3298b0e038218aecb9676c596e7dbad09acbbdd4441d0f1cd79c3ec2a0188720
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161224"
---
# <a name="sdbmakeindexkeyfromstring-function"></a>Funzione SdbMakeIndexKeyFromString

Crea una chiave da una stringa.

## <a name="syntax"></a>Sintassi


```C++
ULONGLONG WINAPI SdbMakeIndexKeyFromString(
  _In_ LPCTSTR pwszKey
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pwszKey* \[ Pollici\]
</dt> <dd>

Stringa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce la chiave o 0 se si verifica un errore.

## <a name="remarks"></a>Commenti

La chiave di indice standard è i primi otto caratteri della stringa, convertiti in lettere maiuscole, quindi viene eseguito il cast in un **valore ULONGLONG.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




