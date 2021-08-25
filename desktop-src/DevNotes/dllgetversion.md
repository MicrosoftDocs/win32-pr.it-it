---
description: La funzione DllGetVersion recupera il numero di versione Cabinet.dll usando la struttura CABINETDLLVERSIONINFO.
ms.assetid: 93f6c29e-6a62-46c2-a42b-8270fe522494
title: Funzione DllGetVersion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllGetVersion
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: 7671465d20987de9ebe526db5961513c81cea5b30d6ad095baf4d3df3d798194
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654041"
---
# <a name="dllgetversion-function"></a>Funzione DllGetVersion

\[Questa funzione non è più supportata, pertanto il relativo comportamento non può essere garantito.\]

La **funzione DllGetVersion** recupera il numero di versione Cabinet.dll usando la [**struttura CABINETDLLVERSIONINFO.**](cabinetdllversioninfo.md)

## <a name="syntax"></a>Sintassi


```C++
VOID WINAPI DllGetVersion(
   PCABINETDLLVERSIONINFO pcdvi
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pcdvi* 
</dt> <dd>

Puntatore alla [**struttura CABINETDLLVERSIONINFO**](cabinetdllversioninfo.md) che contiene le informazioni sulla versione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cabinet.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CABINETDLLVERSIONINFO**](cabinetdllversioninfo.md)
</dt> <dt>

[**GetDllVersion**](getdllversion.md)
</dt> </dl>

 

 
