---
description: Recupera informazioni sullo spazio utilizzato dalla cache File offline dati.
ms.assetid: 3a6fa548-0e9a-4138-a5ec-cde0aeb2b811
title: Funzione CSCGetSpaceUsageW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCGetSpaceUsageW
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 8dd6d12c4e0267c97b93a812a4b66d3bd14a408dff0191686d4949ccbc958723
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667954"
---
# <a name="cscgetspaceusagew-function"></a>Funzione CSCGetSpaceUsageW

\[Questa funzione non è supportata e non deve essere usata.\]

Recupera informazioni sullo spazio utilizzato dalla cache File offline dati.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI CSCGetSpaceUsageW(
  _Inout_ LPTSTR  lptzLocation,
  _In_    DWORD   dwSize,
  _Inout_ LPDWORD lpdwMaxSpaceHigh,
  _Inout_ LPDWORD lpdwMaxSpaceLow,
  _Inout_ LPDWORD lpdwCurrentSpaceHigh,
  _Inout_ LPDWORD lpdwCurrentSpaceLow,
  _Inout_ LPDWORD lpcntTotalFiles,
  _Inout_ LPDWORD lpcntTotalDirs
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lptzLocation* \[ in, out\]
</dt> <dd>

Percorso della directory della cache.

</dd> <dt>

*dwSize* \[ Pollici\]
</dt> <dd>

Dimensione del buffer *lptzLocation,* in caratteri.

</dd> <dt>

*lpdwMaxSpaceHigh* \[ in, out\]
</dt> <dd>

Valore **DWORD** di ordine elevato del numero massimo di byte disponibili nella cache.

</dd> <dt>

*lpdwMaxSpaceLow* \[ in, out\]
</dt> <dd>

Valore **DWORD** di ordine basso del numero massimo di byte disponibili nella cache.

</dd> <dt>

*lpdwCurrentSpaceHigh* \[ in, out\]
</dt> <dd>

DWORD di ordine **elevato** del numero corrente di byte disponibili nella cache.

</dd> <dt>

*lpdwCurrentSpaceLow* \[ in, out\]
</dt> <dd>

Valore **DWORD** di ordine basso del numero corrente di byte disponibili nella cache.

</dd> <dt>

*lpcntTotalFiles* \[ in, out\]
</dt> <dd>

Numero totale di file nella cache.

</dd> <dt>

*lpcntTotalDirs* \[ in, out\]
</dt> <dd>

Numero totale di directory nella cache.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce **TRUE** se ha esito positivo; In caso contrario, restituisce **FALSE.**

## <a name="remarks"></a>Commenti

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cscmig.dll</dt> </dl> |



 

 
