---
description: Recupera le informazioni sullo spazio utilizzato dalla cache File offline.
ms.assetid: 3a6fa548-0e9a-4138-a5ec-cde0aeb2b811
title: CSCGetSpaceUsageW (funzione)
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
ms.openlocfilehash: 608fd7736093ae1f8d131ede777a691e467de9de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331197"
---
# <a name="cscgetspaceusagew-function"></a>CSCGetSpaceUsageW (funzione)

\[Questa funzione non è supportata e non deve essere utilizzata.\]

Recupera le informazioni sullo spazio utilizzato dalla cache File offline.

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

*lptzLocation* \[ in uscita\]
</dt> <dd>

Percorso della directory della cache.

</dd> <dt>

*dwSize* \[ in\]
</dt> <dd>

Dimensioni del buffer *lptzLocation* , in caratteri.

</dd> <dt>

*lpdwMaxSpaceHigh* \[ in uscita\]
</dt> <dd>

**Valore DWORD** di ordine superiore del numero massimo di byte disponibili nella cache.

</dd> <dt>

*lpdwMaxSpaceLow* \[ in uscita\]
</dt> <dd>

**Valore DWORD** di ordine inferiore del numero massimo di byte disponibili nella cache.

</dd> <dt>

*lpdwCurrentSpaceHigh* \[ in uscita\]
</dt> <dd>

**Valore DWORD** di ordine superiore del numero corrente di byte disponibili nella cache.

</dd> <dt>

*lpdwCurrentSpaceLow* \[ in uscita\]
</dt> <dd>

**Valore DWORD** di ordine inferiore del numero corrente di byte disponibili nella cache.

</dd> <dt>

*lpcntTotalFiles* \[ in uscita\]
</dt> <dd>

Numero totale di file nella cache.

</dd> <dt>

*lpcntTotalDirs* \[ in uscita\]
</dt> <dd>

Numero totale di directory nella cache.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce **true** se ha esito positivo; in caso contrario, restituisce **false**.

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cscmig.dll</dt> </dl> |



 

 
