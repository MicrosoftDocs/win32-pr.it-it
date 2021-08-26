---
description: Carica una versione specificata di una DLL .NET Framework libreria.
ms.assetid: f001774d-ea9a-4820-aec0-99ce958b1e1d
title: Funzione LoadLibraryShim
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
ms.openlocfilehash: 123d4036713d6c1c5b7f7a08026d29d7d34126c28c5c2c1fceb94eb01baf9609
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001241"
---
# <a name="loadlibraryshim-function"></a>Funzione LoadLibraryShim

Carica una versione specificata di una DLL .NET Framework libreria.

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

*szDllName* \[ Pollici\]
</dt> <dd>

Nome della DLL da caricare dal .NET Framework.

</dd> <dt>

*szVersion* \[ Pollici\]
</dt> <dd>

Versione della DLL da caricare. Se *szVersion* è **NULL,** viene caricata la versione più recente della DLL specificata.

</dd> <dt>

*pvReserved* 
</dt> <dd>

Riservato.

</dd> <dt>

*phModDll* \[ Cambio\]
</dt> <dd>

Handle per il modulo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Questa funzione viene usata per caricare le DLL della libreria incluse nel pacchetto .NET Framework, non le DLL generate dall'utente.

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Mscoree.dll</dt> </dl> |



 

 
