---
description: La funzione GetDllVersion recupera il numero di versione di Cabinet.dll.
ms.assetid: b324d5cd-1ede-473e-a10f-249c95eda057
title: Funzione GetDllVersion
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
ms.openlocfilehash: 14f2da8c6f8c786042c2abd5f41e02bdfab6f33d9b8aa42a5b5f90a6c4357103
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119390711"
---
# <a name="getdllversion-function"></a>Funzione GetDllVersion

\[Questa funzione non è più supportata, pertanto il relativo comportamento non può essere garantito. \]

La **funzione GetDllVersion** recupera il numero di versione di Cabinet.dll.

## <a name="syntax"></a>Sintassi


```C++
LPCSTR WINAPI GetDllVersion(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Numero di versione del file (vedere [risorsa VERSIONINFO).](../menurc/versioninfo-resource.md)

## <a name="remarks"></a>Commenti

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cabinet.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DllGetVersion**](dllgetversion.md)
</dt> </dl>

 

 
