---
description: Disattiva la sottoclasse per il controllo specificato.
ms.assetid: d4d34624-7d85-4c53-8318-b3e5d6f95f7a
title: Funzione Ctl3dUnsubclassCtl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dUnsubclassCtl
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: db0f87b7aec956a74a0c54871da4019c1ddd4f1bcd57fce3806218003fcb70bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162122"
---
# <a name="ctl3dunsubclassctl-function"></a>Funzione Ctl3dUnsubclassCtl

Disattiva la sottoclasse per il controllo specificato.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI Ctl3dUnsubclassCtl(
   HWND hwnd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Hwnd* 
</dt> <dd>

Handle per la finestra di controllo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** il controllo è sottoclassato correttamente; In caso contrario, restituisce **FALSE.**

## <a name="remarks"></a>Commenti

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Ctl3dSubclassCtl**](ctl3dsubclassctl.md)
</dt> </dl>

 

 
