---
description: Registra un'applicazione come client di CTL3D.
ms.assetid: 38a4a04a-6322-4eb8-b272-ae9b90f84e0f
title: Ctl3dRegister (funzione)
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
ms.openlocfilehash: 4b855c162d9d5f1c43a15d1ebd7219da6f847f37
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331669"
---
# <a name="ctl3dregister-function"></a>Ctl3dRegister (funzione)

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

Restituisce **true** se gli effetti 3D sono attivi; in caso contrario, restituisce **false**.

## <a name="remarks"></a>Commenti

Un'applicazione che usa CTL3D deve chiamare questa funzione in WinMain.

gli effetti 3D non sono disponibili nei sistemi con una risoluzione inferiore a VGA.

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
