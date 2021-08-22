---
description: Installa un catalogo in una directory.
ms.assetid: 9741f8e3-d9db-46cd-886d-587f332b0ab8
title: Funzione InstallCatalog
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallCatalog
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 240754024135b5bd5aa48529d49080afbdb04e170987102346cdda2c59b12427
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955930"
---
# <a name="installcatalog-function"></a>Funzione InstallCatalog

\[Questa funzione non è supportata e non deve essere usata.\]

Installa un catalogo in una directory.

## <a name="syntax"></a>Sintassi


```C++
DWORD InstallCatalog(
  _In_      LPCTSTR                  CatalogFullPath,
  _In_opt_  LPCTSTR                  NewBaseName,
  _Out_opt_ ecount_(MAX_Path) LPTSTR NewCatalogFullPath
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*CatalogFullPath* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa che rappresenta il percorso completo del catalogo prima dell'installazione.

</dd> <dt>

*NewBaseName* \[ in, facoltativo\]
</dt> <dd>

Puntatore al nuovo nome di base.

</dd> <dt>

*NewCatalogFullPath* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una stringa che rappresenta il percorso completo del catalogo dopo l'installazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non è attualmente implementata, quindi non restituisce un valore effettivo.

## <a name="remarks"></a>Commenti

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
