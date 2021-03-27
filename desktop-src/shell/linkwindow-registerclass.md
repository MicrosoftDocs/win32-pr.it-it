---
description: Registra una classe della finestra che consente l'uso del controllo comune SysLink in una finestra.
ms.assetid: 1e6dd741-81be-40bb-a8b5-d565f593c4e9
title: Funzione LinkWindow_RegisterClass
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
ms.openlocfilehash: 7b5bfd2e1a45ff3f65df7cf3d3cae41bf4926aaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980023"
---
# <a name="linkwindow_registerclass-function"></a>\_Funzione LinkWindow registerClass

\[Questa funzione è disponibile tramite Windows XP con Service Pack 2 (SP2) e Windows Server 2003. Potrebbe essere modificato o non disponibile nelle versioni successive di Windows. In alternativa, usare [**InitCommonControlsEx**](/windows/win32/api/commctrl/nf-commctrl-initcommoncontrolsex) .\]

Registra una classe della finestra che consente l'uso del controllo comune [Syslink](../controls/syslink-overview.md) in una finestra.

## <a name="syntax"></a>Sintassi


```C++
BOOL LinkWindow_RegisterClass(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **bool**

Restituisce **true** se la registrazione è stata eseguita correttamente. In caso contrario, **false** .

## <a name="remarks"></a>Commenti

Questa funzione non dispone di un file di intestazione o di libreria associato, quindi deve essere chiamata in base al valore ordinale. Chiamare [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) con il nome della dll Shell32.dll per ottenere un handle del modulo. Chiamare quindi [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) con tale handle di modulo e il numero ordinale 258 per usare questa funzione.

Utilizzare [**LinkWindow \_ UnregisterClass**](linkwindow-unregisterclass.md) per annullare la registrazione della classe dopo l'utilizzo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5,0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica dei controlli SysLink](../controls/syslink-overview.md)
</dt> </dl>

 

 
