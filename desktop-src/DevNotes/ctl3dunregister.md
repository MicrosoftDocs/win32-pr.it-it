---
description: Annulla la registrazione di un'applicazione come client di CTL3D.
ms.assetid: 21990A79-F90D-4AE1-AB02-2B33583B47F5
title: Ctl3dUnregister (funzione)
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
ms.openlocfilehash: 85cd45062da9c01ef8af5a312a855bfaab6a6bf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331830"
---
# <a name="ctl3dunregister-function"></a>Ctl3dUnregister (funzione)

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

Restituisce **true** se viene annullata la registrazione dell'applicazione come client di CTL3D; in caso contrario, restituisce **false**.

## <a name="remarks"></a>Commenti

Un'applicazione che usa CTL3D deve chiamare questa funzione in WinMain.

gli effetti 3D non sono disponibili nei sistemi con una risoluzione inferiore a VGA.

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
