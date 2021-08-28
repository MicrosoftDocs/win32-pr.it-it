---
description: Ottiene l'indirizzo di una funzione da una DLL.
ms.assetid: e425948c-5588-4a4f-994c-4e608af18439
title: _Funzione GetProcAddress_
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetProcAddress_
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: d35d623ff7c7873534bd835c138dba490274e5caddf839fc71765cda59b9f00f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053201"
---
# <a name="_getprocaddress_-function"></a>\_Funzione GetProcAddress \_

\[Questa funzione è un wrapper sulla **funzione GetProcAddress.** Questa funzione potrebbe essere modificata o non disponibile in futuro. Le applicazioni devono **chiamare direttamente GetProcAddress.**\]

Ottiene l'indirizzo di una funzione da una DLL. Vedere [**GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="syntax"></a>Sintassi


```C++
FARPROC _GetProcAddress_(
    ...
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*...* 
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> </dl>

 

 
