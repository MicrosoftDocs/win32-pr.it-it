---
description: Termina il monitoraggio dell'inattività.
ms.assetid: 26e52341-77cd-46cd-8b32-e786dfac870e
title: Funzione EndIdleDetection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EndIdleDetection
api_type:
- DllExport
api_location:
- Msidle.dll
ms.openlocfilehash: a2ba6732b9221d4d4d43e670d0d42d39363d50dffc0d2d4b0daf378b10dd292e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691411"
---
# <a name="endidledetection-function"></a>Funzione EndIdleDetection

\[Questa funzione non è supportata e potrebbe essere modificata o non disponibile in futuro. Usare invece la **funzione GetLastInputInfo.**\]

Termina il monitoraggio dell'inattività.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI EndIdleDetection(
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

Restituisce **TRUE se** la funzione ha esito positivo. In caso contrario, restituisce **FALSE.**

## <a name="remarks"></a>Commenti

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) Questa funzione non viene esportata in base al nome. Specificare il numero ordinale 4 quando si **chiama GetProcAddress**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msidle.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetLastInputInfo**](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
</dt> </dl>

 

 
