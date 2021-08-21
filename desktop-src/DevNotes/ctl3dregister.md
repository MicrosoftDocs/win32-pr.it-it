---
description: Registra un'applicazione come client di CTL3D.
ms.assetid: 38a4a04a-6322-4eb8-b272-ae9b90f84e0f
title: Funzione Ctl3dRegister
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dRegister
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 9f58236891b8a673102905e0ef0c108ac9da6e6192788abea9c6e79baf8acfcc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162159"
---
# <a name="ctl3dregister-function"></a>Funzione Ctl3dRegister

Registra un'applicazione come client di CTL3D.

## <a name="syntax"></a>Sintassi


```C++
BOOL Ctl3dRegister(
   HANDLE hinstApp
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hinstApp* 
</dt> <dd>

Handle per l'applicazione da registrare come client.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** gli effetti 3D sono attivi; In caso contrario, restituisce **FALSE.**

## <a name="remarks"></a>Commenti

Un'applicazione che usa CTL3D deve chiamare questa funzione in WinMain.

Gli effetti 3D non sono disponibili nei sistemi con risoluzione inferiore a VGA.

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
