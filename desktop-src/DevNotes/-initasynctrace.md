---
description: Inizializza la traccia.
ms.assetid: d2708e29-920d-4b13-8917-a6f2065ba58c
title: InitAsyncTrace (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InitAsyncTrace
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: f79137fe4e832a193bafa59a573e5eb541884a2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325691"
---
# <a name="initasynctrace-function"></a>InitAsyncTrace (funzione)

Inizializza la traccia.

## <a name="syntax"></a>Sintassi


```C++
BOOL InitAsyncTrace(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce **true** se la funzione ha esito positivo; in caso contrario, restituisce **false**.

## <a name="remarks"></a>Commenti

Exstrace.dll è un componente facoltativo che viene installato con il Simple Mail Transfer Protocol (SMTP) e il protocollo NNTP (Network News Transfer Protocol).

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Exstrace.dll</dt> </dl> |



 

 
