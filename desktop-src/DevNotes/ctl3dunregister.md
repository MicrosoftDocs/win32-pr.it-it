---
description: Annulla la registrazione di un'applicazione come client di CTL3D.
ms.assetid: 21990A79-F90D-4AE1-AB02-2B33583B47F5
title: Funzione Ctl3dUnregister
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dUnregister
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 32a954efceba7400692ad92c91bedb47283587827739c19f23e7802e1481fbe6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691501"
---
# <a name="ctl3dunregister-function"></a>Funzione Ctl3dUnregister

Annulla la registrazione di un'applicazione come client di CTL3D.

## <a name="syntax"></a>Sintassi


```C++
BOOL Ctl3dUnregister(
   HANDLE hinstApp
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hinstApp* 
</dt> <dd>

Handle per l'applicazione di cui annullare la registrazione come client.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE** se la registrazione dell'applicazione viene annullata come client di CTL3D; In caso contrario, restituisce **FALSE.**

## <a name="remarks"></a>Commenti

Un'applicazione che usa CTL3D deve chiamare questa funzione in WinMain.

Gli effetti 3D non sono disponibili nei sistemi con risoluzione inferiore a VGA.

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
