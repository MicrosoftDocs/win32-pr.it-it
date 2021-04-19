---
description: Disattiva la sottoclasse per il controllo specificato.
ms.assetid: d4d34624-7d85-4c53-8318-b3e5d6f95f7a
title: Ctl3dUnsubclassCtl (funzione)
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
ms.openlocfilehash: ec62c2ecab6d8c90a9c9b7b2570bf5d76afd0589
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331827"
---
# <a name="ctl3dunsubclassctl-function"></a>Ctl3dUnsubclassCtl (funzione)

Disattiva la sottoclasse per il controllo specificato.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI Ctl3dUnsubclassCtl(
   HWND hwnd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HWND* 
</dt> <dd>

Handle per la finestra del controllo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se il controllo è sottoclassato correttamente; in caso contrario, restituisce **false**.

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Ctl3dSubclassCtl**](ctl3dsubclassctl.md)
</dt> </dl>

 

 
