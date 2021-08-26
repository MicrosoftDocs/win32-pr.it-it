---
description: Avvia il monitoraggio dell'inattività.
ms.assetid: fed5e4ae-2c2b-4b00-9230-b71aec9335c8
title: Funzione BeginIdleDetection
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
ms.openlocfilehash: 1bbb27114177a6f64f471b0122832bc09180988019bc23a63343920eb76221f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002321"
---
# <a name="beginidledetection-function"></a>Funzione BeginIdleDetection

\[Questa funzione non è supportata e potrebbe essere modificata o non disponibile in futuro. Usare invece la **funzione GetLastInputInfo.**\]

Avvia il monitoraggio dell'inattività.

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

Funzione chiamata quando cambia lo stato di inattività. Questo callback viene definito come segue:

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

Restituisce 0 se la funzione ha esito positivo. In caso contrario, restituisce un codice di errore. Ad esempio, se *dwReserved* è diverso da 0, **viene restituito ERROR \_ INVALID \_ DATA.**

## <a name="remarks"></a>Commenti

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) Questa funzione non viene esportata in base al nome. specificare l'ordinale 3 quando si **chiama GetProcAddress**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msidle.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetLastInputInfo**](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
</dt> </dl>

 

 
