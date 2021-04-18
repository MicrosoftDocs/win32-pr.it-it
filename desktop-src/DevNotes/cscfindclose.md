---
description: Chiude un handle di ricerca.
ms.assetid: 2e6a547f-26a7-401a-b1e4-3f085ce82729
title: CSCFindClose (funzione)
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
ms.openlocfilehash: 69e3ea972ccd67a1db999c186709ef3aeff84be9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331201"
---
# <a name="cscfindclose-function"></a>CSCFindClose (funzione)

\[Questa funzione non è supportata e non deve essere utilizzata.\]

Chiude un handle di ricerca.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI CSCFindClose(
  _In_ HANDLE hFind
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hFind* \[ in\]
</dt> <dd>

Handle di ricerca restituito dalla funzione [**CSCFindFirstFileW**](cscfindfirstfilew.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce **true** se ha esito positivo; in caso contrario, restituisce **false**.

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cscmig.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CSCFindFirstFileW**](cscfindfirstfilew.md)
</dt> </dl>

 

 
