---
description: Sottoclassi di un singolo controllo, a meno che il controllo non venga visualizzato in una finestra di dialogo.
ms.assetid: 07a2bce1-4c69-4f8d-bb24-b17351f5e771
title: Funzione Ctl3dSubclassCtl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dSubclassCtl
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: f1d25bdc189ad80f1976ee76cc7f9909d099f34c8a88b83771ebf3f297c78934
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654481"
---
# <a name="ctl3dsubclassctl-function"></a>Funzione Ctl3dSubclassCtl

Sottoclassi di un singolo controllo, a meno che il controllo non venga visualizzato in una finestra di dialogo.

## <a name="syntax"></a>Sintassi


```C++
BOOL Ctl3dSubclassCtl(
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

[**Ctl3dUnsubclassCtl**](ctl3dunsubclassctl.md)
</dt> </dl>

 

 
