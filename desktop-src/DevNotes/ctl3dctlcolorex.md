---
description: Gestisce il messaggio \_ WM CTLCOLOR per le applicazioni che usano CTL3D.
ms.assetid: 8626a559-4856-4e7d-bf9c-edc48613b8f4
title: Funzione Ctl3dCtlColorEx
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
ms.openlocfilehash: 46fe35fd507f20e41e0a9b563ded5c9cf46e9c557893bc9287d65cbdf651b24f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691641"
---
# <a name="ctl3dctlcolorex-function"></a>Funzione Ctl3dCtlColorEx

Gestisce il **messaggio \_ WM CTLCOLOR** per le applicazioni che usano CTL3D.

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

Handle per il contesto di visualizzazione.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per una finestra figlio (controllo ).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un handle al pennello appropriato se la funzione ha esito positivo; In caso contrario, restituisce `(HBRUSH)(0)` che indica che si è verificato un errore.

## <a name="remarks"></a>Commenti

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
