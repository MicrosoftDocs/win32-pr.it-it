---
description: Restituisce l'indirizzo di una funzione di callback di errore di caricamento ritardato per la DLL e il processo specificati.
ms.assetid: db1d34cb-800a-4984-b4a3-d1ce1c6ee86c
title: DelayLoadFailureHook (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DelayLoadFailureHook
api_type:
- DllExport
api_location:
- kernel32.dll
- API-MS-Win-Core-DelayLoad-l1-1-0.dll
- kernelbase.dll
- mincoredload.dll
- minkernelbase.dll
- API-MS-Win-Core-DelayLoad-l1-1-1.dll
ms.openlocfilehash: f4986b70332a2581580d7e3b274e9d3cdcd96532
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327456"
---
# <a name="delayloadfailurehook-function"></a>DelayLoadFailureHook (funzione)

Restituisce l'indirizzo di una funzione di callback di errore di caricamento ritardato per la DLL e il processo specificati.

## <a name="syntax"></a>Sintassi


```C++
FARPROC WINAPI DelayLoadFailureHook(
  _In_ LPCSTR pszDllName,
  _In_ LPCSTR pszProcName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pszDllName* \[ in\]
</dt> <dd>

Nome della DLL.

</dd> <dt>

*pszProcName* \[ in\]
</dt> <dd>

Nome del processo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Indirizzo della funzione di callback.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Libreria<br/> | <dl> <dt>Kernel32.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Hook di errore](https://msdn.microsoft.com/library/sfcfb0a3(v=VS.71).aspx)
</dt> </dl>

 

 




