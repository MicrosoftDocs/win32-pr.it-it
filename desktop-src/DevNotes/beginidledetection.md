---
description: Inizia il monitoraggio dell'inattività.
ms.assetid: fed5e4ae-2c2b-4b00-9230-b71aec9335c8
title: BeginIdleDetection (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BeginIdleDetection
api_type:
- DllExport
api_location:
- Msidle.dll
ms.openlocfilehash: 06cd016dc4102ef2f5b0f351aa4836a7f9980645
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329890"
---
# <a name="beginidledetection-function"></a>BeginIdleDetection (funzione)

\[Questa funzione non è supportata e può essere modificata o non disponibile in futuro. Usare invece la funzione **GetLastInputInfo** .\]

Inizia il monitoraggio dell'inattività.

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPI BeginIdleDetection(
   _IDLECALLBACK pfnCallback,
   DWORD         dwIdleMin,
   DWORD         dwReserved
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pfnCallback* 
</dt> <dd>

Funzione chiamata quando lo stato di inattività viene modificato. Questo callback viene definito come segue:

``` syntax
typedef void (WINAPI* _IDLECALLBACK) (DWORD dwState);

#define STATE_USER_IDLE_BEGIN       1
#define STATE_USER_IDLE_END         2
```

</dd> <dt>

*dwIdleMin* 
</dt> <dd>

Numero di minuti di inattività prima che venga effettuata la chiamata alla funzione di callback.

</dd> <dt>

*dwReserved* 
</dt> <dd>

Questo parametro deve essere impostato su zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 se la funzione ha esito positivo; in caso contrario, restituisce un codice di errore. Se, ad esempio, il valore di *dwReserved* è diverso da 0, vengono restituiti **\_ \_ dati non validi** .

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) . Questa funzione non viene esportata per nome; specificare il numero ordinale 3 quando si chiama **GetProcAddress**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msidle.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetLastInputInfo**](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
</dt> </dl>

 

 
