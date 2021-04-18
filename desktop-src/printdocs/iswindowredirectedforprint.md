---
description: La funzione IsWindowRedirectedForPrint determina se la finestra specificata è attualmente reindirizzata per la stampa.
ms.assetid: 49FD0D63-0F7F-48C6-81B6-25715294E7B7
title: IsWindowRedirectedForPrint (funzione)
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
ms.openlocfilehash: b6648e5638ec6f05a2677ce279b0c3d7b160b49b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318371"
---
# <a name="iswindowredirectedforprint-function"></a>IsWindowRedirectedForPrint (funzione)

La funzione **IsWindowRedirectedForPrint** determina se la finestra specificata è attualmente reindirizzata per la stampa.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI IsWindowRedirectedForPrint(
  _In_   HWND hWnd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HWND* \[ in\]
</dt> <dd>

Handle della finestra.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la finestra è attualmente reindirizzata per la stampa, la funzione restituisce un valore diverso da zero. in caso contrario, restituisce zero.

## <a name="remarks"></a>Commenti

Una finestra viene reindirizzata per la stampa quando elabora una chiamata a [**PrintWindow**](/windows/desktop/api/Winuser/nf-winuser-printwindow). In una chiamata a **PrintWindow**, una finestra esegue il rendering del contenuto in un contesto di dispositivo fuori schermo.

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>User32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PrintWindow**](/windows/desktop/api/Winuser/nf-winuser-printwindow)
</dt> <dt>

[**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[**\_stampa WM**](/windows/desktop/gdi/wm-print)
</dt> <dt>

[**\_PRINTCLIENT WM**](/windows/desktop/gdi/wm-printclient)
</dt> </dl>

 

