---
description: Inviato per verificare l'esistenza di un comando di menu.
title: DFM_VALIDATECMD messaggio (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 97ff3cdf-ed0c-4813-8d5a-b5141636d32c
api_name:
- DFM_VALIDATECMD
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3fd647d5cd6e171cc71e0968abb29d80e7aef5900d43fe4bd4b88f5f49bbdc7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118721947"
---
# <a name="dfm_validatecmd-message"></a>Messaggio DFM \_ VALIDATECMD

Inviato per verificare l'esistenza di un comando di menu.


```C++
DFM_INVOKECOMMAND

    wParam = (WPARAM)(WPARAM) idCmd;            

    lParam = (LPARAM)(LPARAM) lParam = 0;

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*idCmd* 
</dt> <dd>Offset dell'identificatore del comando di menu.</dd> <dt>

*lParam* 
</dt> <dd>Non usato. Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK se il comando esiste oppure S FALSE in caso \_ contrario.

## <a name="remarks"></a>Commenti

Questo messaggio viene inviato alla funzione di callback o all'oggetto callback a seconda della modalità di costruzione dell'oggetto menu di scelta rapida predefinito. Per la costruzione sono disponibili due API, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).

[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) è una versione estesa di questo messaggio e fornisce altre informazioni al callback. Usare **DFM \_ INVOKECOMMANDEX** se le informazioni aggiuntive fornite da tale interfaccia sono necessarie nell'implementazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                      |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 




