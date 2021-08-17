---
description: Chiama la funzione GetLastError e converte il codice restituito in un HRESULT.
ms.assetid: 7b8eab85-212b-44bc-9d1b-60587652380d
title: Funzione SignError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignError
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: f48f96ed867e6db41240a300d30e1f3a585e8b03a129d138c11a14ebf44ad42c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898435"
---
# <a name="signerror-function"></a>Funzione SignError

> [!IMPORTANT]
> Questa API è deprecata. Microsoft potrà rimuovere questa API nelle versioni future.

 

La **funzione SignError** chiama la [**funzione GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) e converte il codice restituito in **HRESULT.**

> [!Note]  
> A questa funzione non è associato alcun file di intestazione o libreria di importazione. Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e usare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per il collegamento dinamico a Mssign32.dll.

 

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI SignError(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce **S \_ OK**.

Se il metodo ha esito negativo, restituisce un **valore HRESULT** che indica l'errore. Per un elenco dei codici di errore comuni, vedere [Valori HRESULT comuni.](common-hresult-values.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
