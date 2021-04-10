---
description: Chiama la funzione GetLastError e converte il codice restituito in un valore HRESULT.
ms.assetid: 7b8eab85-212b-44bc-9d1b-60587652380d
title: SignError (funzione)
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
ms.openlocfilehash: 7a405bef4666721e485e8b5ad6905209b2244bef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049549"
---
# <a name="signerror-function"></a>SignError (funzione)

> [!IMPORTANT]
> Questa API è deprecata. Microsoft può rimuovere questa API nelle versioni future.

 

La funzione **SignError** chiama la funzione [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) e converte il codice restituito in un valore **HRESULT**.

> [!Note]  
> A questa funzione non è associato alcun file di intestazione o libreria di importazione. Per chiamare questa funzione, è necessario creare un file di intestazione definito dall'utente e utilizzare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI SignError(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce **S \_ OK**.

Se il metodo ha esito negativo, restituisce un valore **HRESULT** che indica l'errore. Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
