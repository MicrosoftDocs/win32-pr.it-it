---
description: Chiude un handle di ricerca.
ms.assetid: 2e6a547f-26a7-401a-b1e4-3f085ce82729
title: Funzione CSCFindClose
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCFindClose
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 862159ed74d6c7c9ddbe4d6f97bede37bab7dca949e6d3259715737de07b8df5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758721"
---
# <a name="cscfindclose-function"></a>Funzione CSCFindClose

\[Questa funzione non è supportata e non deve essere usata.\]

Chiude un handle di ricerca.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI CSCFindClose(
  _In_ HANDLE hFind
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hFind* \[ Pollici\]
</dt> <dd>

Handle di ricerca restituito dalla [**funzione CSCFindFirstFileW.**](cscfindfirstfilew.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce **TRUE** se ha esito positivo; In caso contrario, restituisce **FALSE.**

## <a name="remarks"></a>Commenti

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cscmig.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CSCFindFirstFileW**](cscfindfirstfilew.md)
</dt> </dl>

 

 
