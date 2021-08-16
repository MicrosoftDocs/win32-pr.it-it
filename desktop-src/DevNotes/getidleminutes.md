---
description: Ottiene l'intervallo di tempo, in minuti, dall'ultima attività dell'utente.
ms.assetid: 2d1e68ad-6f65-4e64-afbf-505b2c9d3423
title: Funzione GetIdleMinutes
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetIdleMinutes
api_type:
- DllExport
api_location:
- Msidle.dll
ms.openlocfilehash: d3397de5d792181958891eef9693d29b2d7d4e56f9bbc7f7e1cfef19171625b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118404584"
---
# <a name="getidleminutes-function"></a>Funzione GetIdleMinutes

\[Questa funzione non è supportata e potrebbe essere modificata o non disponibile in futuro. Usare invece la **funzione GetLastInputInfo.**\]

Ottiene l'intervallo di tempo, in minuti, dall'ultima attività dell'utente.

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPI GetIdleMinutes(
   DWORD dwReserved
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwReserved* 
</dt> <dd>

Questo parametro deve essere impostato su zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il numero di minuti dall'ultima attività dell'utente.

## <a name="remarks"></a>Commenti

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) Questa funzione non viene esportata in base al nome. specificare l'ordinale 8 quando si **chiama GetProcAddress**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msidle.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetLastInputInfo**](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
</dt> </dl>

 

 
