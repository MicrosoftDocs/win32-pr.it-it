---
description: Consente al callback di aggiungere voci al menu.
title: DFM_MERGECONTEXTMENU messaggio (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2fd779ac-7dd6-4b81-86dc-8930db27ae59
api_name:
- DFM_MERGECONTEXTMENU
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2ddd071e40d3c017a513eb0e85efb634df530a8686afaf7df59b922602d37f22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119455971"
---
# <a name="dfm_mergecontextmenu-message"></a>Messaggio DFM \_ MERGECONTEXTMENU

Consente al callback di aggiungere voci al menu.


```C++
DFM_MERGECONTEXTMENU

    lParam = (LPARAM)(LPQCMINFO) pqcminfo;

    wParam = (WPARAM)(UINT) uFlags;         

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pqcminfo* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura QCMINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) contenente le informazioni usate nell'unione.

</dd> <dt>

*uFlags* \[ Pollici\]
</dt> <dd>

Flag che specificano la modalità di modifica del menu di scelta rapida. Questo parametro usa i valori CMF \_ \* descritti in [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).

</dd> </dl>

## <a name="remarks"></a>Commenti

Se gli elementi vengono aggiunti al menu di scelta rapida, devono essere supportati con routine che rispondono in modo appropriato quando uno di tali elementi viene richiamato tramite [**DFM \_ INVOKECOMMAND**](dfm-invokecommand.md).

Questo messaggio viene inviato alla funzione di callback o all'oggetto callback a seconda della modalità di implementazione dell'oggetto menu di scelta rapida predefinito. Esistono due API per l'implementazione, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).

[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) è una versione estesa di questo messaggio e fornisce altre informazioni al callback. Usare **DFM \_ INVOKECOMMANDEX** se le informazioni aggiuntive fornite da tale interfaccia sono necessarie nell'implementazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 




