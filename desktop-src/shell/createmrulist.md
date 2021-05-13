---
description: Crea un nuovo elenco degli elementi usati più di recente.
title: Funzione CreateMRUListW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateMRUListW
- CreateMRUListW
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: b2d9e3c7-8151-45ef-9658-bd33a87b4c9c
ms.openlocfilehash: 34cd3dd9e5b9e62bbdd13b31d95e7205e4427de6
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843382"
---
# <a name="createmrulistw-function"></a>Funzione CreateMRUListW

Crea un nuovo elenco degli elementi usati più di recente.

## <a name="syntax"></a>Sintassi


```C++
int CreateMRUListW(
  _In_ LPMRUINFO lpmi
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpmi* \[ Pollici\]
</dt> <dd>

Tipo: **LPMRUINFO**

Puntatore a una [**struttura MRUINFO**](mruinfo.md) che definisce l'elenco MRU.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **int**

Restituisce un handle per il nuovo elenco MRU oppure 0 in caso di errore.

## <a name="remarks"></a>Commenti

Questa funzione non è inclusa in un'intestazione o in una libreria pubblica. È possibile accedervi tramite [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) o estrarlo da comctl32.dll ordinale, ovvero 400 per **CreateMRUListW.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                     |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (versione 5.0 o successiva)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **CreateMRUListW** (Unicode)<br/>                                                                        |



 

 
