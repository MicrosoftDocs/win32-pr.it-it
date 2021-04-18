---
description: Termina il monitoraggio dell'inattività.
ms.assetid: 26e52341-77cd-46cd-8b32-e786dfac870e
title: EndIdleDetection (funzione)
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
ms.openlocfilehash: e50679c53123ad140324f7d159ef938367c02af0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328565"
---
# <a name="endidledetection-function"></a>EndIdleDetection (funzione)

\[Questa funzione non è supportata e può essere modificata o non disponibile in futuro. Usare invece la funzione **GetLastInputInfo** .\]

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

Restituisce **true** se la funzione ha esito positivo; in caso contrario, restituisce **false**.

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) . Questa funzione non viene esportata per nome; specificare il numero ordinale 4 quando si chiama **GetProcAddress**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msidle.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetLastInputInfo**](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
</dt> </dl>

 

 
