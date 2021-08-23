---
description: Indica la versione di CTL3D attualmente in esecuzione.
ms.assetid: 38c0842c-417f-4ca1-acc2-3bbadf45c804
title: Funzione Ctl3dGetVer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dGetVer
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: f29963020290686521d5e3bd165d2c8fac6e5e0c96f34552ad11f725d95567cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654501"
---
# <a name="ctl3dgetver-function"></a>Funzione Ctl3dGetVer

Indica la versione di CTL3D attualmente in esecuzione.

## <a name="syntax"></a>Sintassi


```C++
WORD Ctl3dGetVer(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un valore che contiene il numero di versione principale nel byte di ordine elevato e il numero di versione secondaria nel byte meno significativo.

## <a name="remarks"></a>Commenti

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
