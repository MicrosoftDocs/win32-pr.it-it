---
description: Carica una versione specificata di una DLL della libreria .NET Framework.
ms.assetid: f001774d-ea9a-4820-aec0-99ce958b1e1d
title: LoadLibraryShim (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadLibraryShim
api_type:
- DllExport
api_location:
- Mscoree.dll
ms.openlocfilehash: 3a2fd8ab6aef8d0309748cbbf37d56ccd032b050
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324696"
---
# <a name="loadlibraryshim-function"></a>LoadLibraryShim (funzione)

Carica una versione specificata di una DLL della libreria .NET Framework.

## <a name="syntax"></a>Sintassi


```C++
HRESULT LoadLibraryShim(
  _In_  LPCWSTR szDllName,
  _In_  LPCWSTR szVersion,
        LPVOID  pvReserved,
  _Out_ HMODULE *phModDll
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*szDllName* \[ in\]
</dt> <dd>

Nome della DLL da caricare dal .NET Framework.

</dd> <dt>

*szVersion* \[ in\]
</dt> <dd>

Versione della DLL da caricare. Se *szVersion* è **null**, viene caricata la versione più recente della DLL specificata.

</dd> <dt>

*pvReserved* 
</dt> <dd>

Riservato.

</dd> <dt>

*phModDll* \[ out\]
</dt> <dd>

Handle per il modulo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Questa funzione viene utilizzata per caricare le dll della libreria incluse nel pacchetto ridistribuibile .NET Framework, non nelle DLL generate dall'utente.

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Mscoree.dll</dt> </dl> |



 

 
