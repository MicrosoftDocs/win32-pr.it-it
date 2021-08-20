---
description: Verifica un singolo file di catalogo.
ms.assetid: 4b2de733-ef95-4b0a-8f53-7bc73ffaa2c2
title: Funzione VerifyCatalogFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VerifyCatalogFile
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: eb4012a04b4da9e353a5d771f9b9e61d4bfba8b45ed6a7d5c65a81c197ff9be8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075745"
---
# <a name="verifycatalogfile-function"></a>Funzione VerifyCatalogFile

\[Questa funzione non è supportata e non deve essere usata.\]

Verifica un singolo file di catalogo.

## <a name="syntax"></a>Sintassi


```C++
DWORD VerifyCatalogFile(
   LPCTSTR CatalogFullPath
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*CatalogFullPath* 
</dt> <dd>

Percorso completo del file di catalogo da verificare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce **ERROR \_ SUCCESS;** in caso contrario, restituisce l'errore [**da WinVerifyTrust.**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust)

Se il catalogo è con firma Authenticode, questa funzione restituisce **ERROR \_ AUTHENTICODE \_ TRUSTED \_ PUBLISHER** se ha esito positivo; in caso contrario, restituisce **ERROR \_ AUTHENTICODE \_ TRUST NOT \_ \_ ESTABLISHED**.

Se la funzione non è in grado di determinare se il server di pubblicazione è attendibile, può anche restituire **ERROR \_ UNIDENTIFIED \_ ERROR**.

## <a name="remarks"></a>Commenti

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
