---
description: La funzione GetDllVersion Recupera il numero di versione di Cabinet.dll.
ms.assetid: b324d5cd-1ede-473e-a10f-249c95eda057
title: GetDllVersion (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDllVersion
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: 1b1142bd2ece965a3f2fc58b6bb2f90586a8b391
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326674"
---
# <a name="getdllversion-function"></a>GetDllVersion (funzione)

\[Questa funzione non è più supportata, pertanto non è possibile garantirne il comportamento. \]

La funzione **GetDllVersion** Recupera il numero di versione di Cabinet.dll.

## <a name="syntax"></a>Sintassi


```C++
LPCSTR WINAPI GetDllVersion(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Il numero di versione del file (vedere la [risorsa VERSIONINFO](../menurc/versioninfo-resource.md)).

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cabinet.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DllGetVersion**](dllgetversion.md)
</dt> </dl>

 

 
