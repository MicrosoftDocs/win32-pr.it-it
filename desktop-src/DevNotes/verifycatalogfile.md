---
description: Verifica un singolo file di catalogo.
ms.assetid: 4b2de733-ef95-4b0a-8f53-7bc73ffaa2c2
title: VerifyCatalogFile (funzione)
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
ms.openlocfilehash: 52083b23041f7f21aa51e326bc00d4cabc76eca7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324435"
---
# <a name="verifycatalogfile-function"></a>VerifyCatalogFile (funzione)

\[Questa funzione non è supportata e non deve essere utilizzata.\]

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

Se la funzione ha esito positivo, viene restituito l' **errore \_ esito positivo**; in caso contrario, viene restituito l'errore da [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust).

Se il catalogo è un catalogo con firma Authenticode, questa funzione restituisce l' **errore di \_ \_ \_ autore attendibile Authenticode** se ha esito positivo; in caso contrario, restituisce l' **errore di \_ \_ attendibilità Authenticode \_ non \_ stabilito**.

Se la funzione non è in grado di determinare se il server di pubblicazione è attendibile, potrebbe inoltre restituire un errore non **\_ identificato \_**.

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
