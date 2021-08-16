---
description: Registra una classe finestra che consente l'uso del controllo comune SysLink in una finestra.
ms.assetid: 1e6dd741-81be-40bb-a8b5-d565f593c4e9
title: LinkWindow_RegisterClass funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LinkWindow_RegisterClass
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 75936c918a930698ef803b02743b935660e876b0d87d7f6d5eddce91d4f4c0a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968960"
---
# <a name="linkwindow_registerclass-function"></a>Funzione LinkWindow \_ RegisterClass

\[Questa funzione è disponibile tramite Windows XP con Service Pack 2 (SP2) e Windows Server 2003. Potrebbe essere modificato o non disponibile nelle versioni successive di Windows. In [**alternativa, usare InitCommonControlsEx.**](/windows/win32/api/commctrl/nf-commctrl-initcommoncontrolsex)\]

Registra una classe finestra che consente l'uso del controllo comune [SysLink](../controls/syslink-overview.md) in una finestra.

## <a name="syntax"></a>Sintassi


```C++
BOOL LinkWindow_RegisterClass(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **BOOL**

Restituisce **TRUE se** la registrazione ha avuto esito positivo. **FALSE in** caso contrario.

## <a name="remarks"></a>Commenti

Questa funzione non ha un file di intestazione o di libreria associato, quindi deve essere chiamata dal valore ordinale. Chiamare [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) con il nome della DLL Shell32.dll per ottenere un handle del modulo. Chiamare quindi [**GetProcAddress con**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) l'handle del modulo e il numero ordinale 258 per usare questa funzione.

Usare [**LinkWindow \_ UnregisterClass**](linkwindow-unregisterclass.md) per annullare la registrazione della classe dopo l'uso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5.0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica dei controlli SysLink](../controls/syslink-overview.md)
</dt> </dl>

 

 
