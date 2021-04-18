---
description: Gestisce il \_ messaggio WM CTLCOLOR per le applicazioni che usano CTL3D.
ms.assetid: 8626a559-4856-4e7d-bf9c-edc48613b8f4
title: Ctl3dCtlColorEx (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dCtlColorEx
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 57df7ed5e439d75b2edbf71e743cac069f0ed75b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331469"
---
# <a name="ctl3dctlcolorex-function"></a>Ctl3dCtlColorEx (funzione)

Gestisce il messaggio **WM \_ CTLCOLOR** per le applicazioni che usano CTL3D.

## <a name="syntax"></a>Sintassi


```C++
HBRUSH Ctl3dCtlColorEx(
   UINT   wm,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wm* 
</dt> <dd>

Messaggio **WM \_ CTLCOLOR** per l'applicazione.

</dd> <dt>

*wParam* 
</dt> <dd>

Handle per il contesto di visualizzazione (DC).

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per una finestra figlio (controllo).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un handle al pennello appropriato se la funzione ha esito positivo; in caso contrario, restituisce `(HBRUSH)(0)` un valore che indica che si è verificato un errore.

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
