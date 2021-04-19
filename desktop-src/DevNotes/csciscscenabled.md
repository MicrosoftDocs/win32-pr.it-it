---
description: Determina se File offline è abilitato.
ms.assetid: c7d3173d-ed51-4de6-ad07-4c5e6906b0f4
title: CSCIsCSCEnabled (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCIsCSCEnabled
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 13db7ebbb11f678c00a5a755ffe8114f8684b315
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331193"
---
# <a name="csciscscenabled-function"></a>CSCIsCSCEnabled (funzione)

\[Questa funzione non è supportata e non deve essere utilizzata.\]

Determina se File offline è abilitato.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI CSCIsCSCEnabled(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce **true** se file offline è abilitato e **false** in caso contrario.

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cscmig.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CSCQueryDatabaseStatus**](cscquerydatabasestatus.md)
</dt> </dl>

 

 
