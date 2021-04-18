---
description: Annulla la registrazione di una classe di finestra registrata da LinkWindow \_ registerClass.
ms.assetid: 9e5c4326-efd1-43ca-a087-a436fe3f9bbd
title: Funzione LinkWindow_UnregisterClass
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
ms.openlocfilehash: 604cea299156444a1fedf34a46c50b5b397a65da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980018"
---
# <a name="linkwindow_unregisterclass-function"></a>LinkWindow \_ UnregisterClass-funzione

\[Questa funzione è disponibile tramite Windows XP con Service Pack 2 (SP2) e Windows Server 2003. Potrebbe essere modificato o non disponibile nelle versioni successive di Windows.\]

Annulla la registrazione di una classe di finestra registrata da [**LinkWindow \_ registerClass**](linkwindow-registerclass.md).

## <a name="syntax"></a>Sintassi


```C++
BOOL LinkWindow_UnregisterClass(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **bool**

Restituisce **true** se l'operazione è stata eseguita correttamente. In caso contrario, **false** .

## <a name="remarks"></a>Commenti

Questa funzione non dispone di un file di intestazione o di libreria associato, quindi deve essere chiamata in base al valore ordinale. Chiamare [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) con il nome della dll Shell32.dll per ottenere un handle del modulo. Chiamare quindi [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) con tale handle di modulo e il numero ordinale 259 per usare questa funzione.

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

 

 
