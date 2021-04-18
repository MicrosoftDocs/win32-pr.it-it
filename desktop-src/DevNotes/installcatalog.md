---
description: Installa un catalogo in una directory.
ms.assetid: 9741f8e3-d9db-46cd-886d-587f332b0ab8
title: InstallCatalog (funzione)
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
ms.openlocfilehash: 57b2a9d29b72db6c04673f30f41f26c44701c69c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331190"
---
# <a name="installcatalog-function"></a>InstallCatalog (funzione)

\[Questa funzione non è supportata e non deve essere utilizzata.\]

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

*CatalogFullPath* \[ in\]
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

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
