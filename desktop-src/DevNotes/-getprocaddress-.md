---
description: Ottiene l'indirizzo di una funzione da una DLL.
ms.assetid: e425948c-5588-4a4f-994c-4e608af18439
title: _GetProcAddress_ (funzione)
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
ms.openlocfilehash: 0d717036b92e79056fd3b1bf69f1fd17784db713
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331972"
---
# <a name="_getprocaddress_-function"></a>\_GetProcAddress ( \_ funzione)

\[Questa funzione è un wrapper per la funzione **GetProcAddress** . Questa funzione può essere modificata o non disponibile in futuro. Le applicazioni devono chiamare direttamente **GetProcAddress** .\]

Ottiene l'indirizzo di una funzione da una DLL. Vedere [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress).

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

 

 
