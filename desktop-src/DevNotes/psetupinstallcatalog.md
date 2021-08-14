---
description: Installa un file di catalogo.
ms.assetid: bea74e91-1a87-4785-b983-5fec87e03499
title: Funzione pSetupInstallCatalog
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupInstallCatalog
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 344b88be84e2be2b3a199b4cac6bbf1c7bc6d7d0e7082276cee43933ecc7d1ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119386491"
---
# <a name="psetupinstallcatalog-function"></a>Funzione pSetupInstallCatalog

\[Questa funzione non è più supportata da Microsoft. Gli sviluppatori devono **usare CryptCATAdminAddCatalog**.\]

Installa un file di catalogo.

## <a name="syntax"></a>Sintassi


```C++
DWORD pSetupInstallCatalog(
  _In_      LPCTSTR CatalogFullPath,
  _In_      LPCTSTR NewBaseName,
  _Out_opt_ LPTSTR  NewCatalogFullPath
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*CatalogFullPath* \[ Pollici\]
</dt> <dd>

Percorso completo del catalogo da installare nel sistema.

</dd> <dt>

*NewBaseName* \[ Pollici\]
</dt> <dd>

Nuovo nome di base da utilizzare quando il file di catalogo viene copiato nell'archivio cataloghi.

</dd> <dt>

*NewCatalogFullPath* \[ out, facoltativo\]
</dt> <dd>

Riceve facoltativamente il percorso completo del file di catalogo all'interno dell'archivio del catalogo. Il buffer deve essere almeno **MAX \_ PATH** bytes (versione ANSI) o chars (versione Unicode).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce **NO \_ ERROR;** in caso contrario, restituisce un codice di errore Win32 che indica la causa dell'errore.

## <a name="remarks"></a>Commenti

Il file viene copiato dal sistema in una directory speciale ed eventualmente rinominato.

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CryptCATAdminAddCatalog**](/windows/win32/api/mscat/nf-mscat-cryptcatadminaddcatalog)
</dt> </dl>

 

 
