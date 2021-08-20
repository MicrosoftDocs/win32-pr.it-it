---
description: Verifica se i controlli possono usare effetti 3D.
ms.assetid: fb7b892f-2580-41ac-b2ef-938da3cc1dc2
title: Funzione Ctl3dEnabled
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dEnabled
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 0d8a234736631517a0e77f5ab23f07688e3d80aa4c8b74a3b2ee51351beece90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654591"
---
# <a name="ctl3denabled-function"></a>Funzione Ctl3dEnabled

Verifica se i controlli possono usare effetti 3D.

## <a name="syntax"></a>Sintassi


```C++
BOOL Ctl3dEnabled(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** i controlli possono usare effetti 3D. In caso contrario, restituisce **FALSE.**

## <a name="remarks"></a>Commenti

In Windows 4.0 o versioni **successive, Ctl3dEnabled** e [**Ctl3dRegister**](ctl3dregister.md) restituiscono **FALSE.**

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
