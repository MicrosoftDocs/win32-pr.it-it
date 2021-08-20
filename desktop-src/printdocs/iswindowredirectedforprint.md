---
description: La funzione IsWindowRedirectedForPrint determina se la finestra specificata è attualmente reindirizzata per la stampa.
ms.assetid: 49FD0D63-0F7F-48C6-81B6-25715294E7B7
title: Funzione IsWindowRedirectedForPrint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsWindowRedirectedForPrint
api_type:
- DllExport
api_location:
- user32.dll
ms.openlocfilehash: f797f46bd0bb6458ad1d2393b87f3350064d3efa1adf836569bfc1042de62bf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117686527"
---
# <a name="iswindowredirectedforprint-function"></a>Funzione IsWindowRedirectedForPrint

La **funzione IsWindowRedirectedForPrint** determina se la finestra specificata è attualmente reindirizzata per la stampa.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI IsWindowRedirectedForPrint(
  _In_   HWND hWnd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hWnd* \[ Pollici\]
</dt> <dd>

Handle della finestra.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la finestra è attualmente reindirizzata per la stampa, la funzione restituisce un valore diverso da zero. In caso contrario, restituisce zero.

## <a name="remarks"></a>Commenti

Una finestra viene reindirizzata per la stampa quando elabora una chiamata a [**PrintWindow.**](/windows/desktop/api/Winuser/nf-winuser-printwindow) In una chiamata a **PrintWindow,** una finestra esegue il rendering del contenuto in un contesto di dispositivo fuori schermo.

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>User32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Finestra di stampa**](/windows/desktop/api/Winuser/nf-winuser-printwindow)
</dt> <dt>

[**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[**WM \_ PRINT**](/windows/desktop/gdi/wm-print)
</dt> <dt>

[**WM \_ PRINTCLIENT**](/windows/desktop/gdi/wm-printclient)
</dt> </dl>

 

