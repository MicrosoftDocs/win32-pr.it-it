---
description: Annulla la registrazione di una classe finestra registrata da LinkWindow \_ RegisterClass.
ms.assetid: 9e5c4326-efd1-43ca-a087-a436fe3f9bbd
title: LinkWindow_UnregisterClass funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LinkWindow_UnregisterClass
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 05a50d5f3af72c31ee04a1a9e8264acb22327c38f79f765ce2ad7a740086747e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968940"
---
# <a name="linkwindow_unregisterclass-function"></a>Funzione LinkWindow \_ UnregisterClass

\[Questa funzione è disponibile tramite Windows XP con Service Pack 2 (SP2) e Windows Server 2003. Potrebbe essere modificato o non disponibile nelle versioni successive di Windows.\]

Annulla la registrazione di una classe finestra registrata da [**LinkWindow \_ RegisterClass**](linkwindow-registerclass.md).

## <a name="syntax"></a>Sintassi


```C++
BOOL LinkWindow_UnregisterClass(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **BOOL**

Restituisce **TRUE se** l'operazione ha avuto esito positivo. **FALSE in** caso contrario.

## <a name="remarks"></a>Commenti

Questa funzione non ha un file di intestazione o di libreria associato, quindi deve essere chiamata dal valore ordinale. Chiamare [**LoadLibrary con**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) il nome della DLL Shell32.dll per ottenere un handle del modulo. Chiamare quindi [**GetProcAddress con**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) l'handle del modulo e il numero ordinale 259 per usare questa funzione.

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

 

 
