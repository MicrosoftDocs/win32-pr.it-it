---
description: Installa un file di catalogo.
ms.assetid: bea74e91-1a87-4785-b983-5fec87e03499
title: pSetupInstallCatalog (funzione)
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
ms.openlocfilehash: 1fc3948233fe2716bd4a0a6d720a3f285a5476cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330418"
---
# <a name="psetupinstallcatalog-function"></a>pSetupInstallCatalog (funzione)

\[Questa funzione non è più supportata da Microsoft. Gli sviluppatori devono usare **CryptCATAdminAddCatalog**.\]

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

*CatalogFullPath* \[ in\]
</dt> <dd>

Percorso completo del catalogo da installare nel sistema.

</dd> <dt>

*NewBaseName* \[ in\]
</dt> <dd>

Nuovo nome di base da utilizzare quando il file di catalogo viene copiato nell'archivio del catalogo.

</dd> <dt>

*NewCatalogFullPath* \[ out, facoltativo\]
</dt> <dd>

Riceve facoltativamente il percorso completo del file di catalogo nell'archivio del catalogo. Questo buffer deve essere almeno il **numero \_ massimo** di byte di percorso (versione ANSI) o chars (versione Unicode).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, non viene restituito **alcun \_ errore**. in caso contrario, restituisce un codice di errore Win32 che indica la motivo dell'errore.

## <a name="remarks"></a>Commenti

Il file viene copiato dal sistema in una directory speciale ed eventualmente rinominato.

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CryptCATAdminAddCatalog**](/windows/win32/api/mscat/nf-mscat-cryptcatadminaddcatalog)
</dt> </dl>

 

 
