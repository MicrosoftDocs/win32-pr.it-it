---
description: Consente al callback di aggiungere elementi al menu.
title: Messaggio DFM_MERGECONTEXTMENU (Shlobj. h)
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
ms.openlocfilehash: d469f9764b5e377e5f47227d3414f246441d3505
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977274"
---
# <a name="dfm_mergecontextmenu-message"></a>\_Messaggio DFM MERGECONTEXTMENU

Consente al callback di aggiungere elementi al menu.


```C++
DFM_MERGECONTEXTMENU

    lParam = (LPARAM)(LPQCMINFO) pqcminfo;

    wParam = (WPARAM)(UINT) uFlags;         

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pqcminfo* \[ in\]
</dt> <dd>

Puntatore a una struttura [**QCMINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) contenente le informazioni utilizzate nell'Unione.

</dd> <dt>

*uFlags* \[ in\]
</dt> <dd>

Flag che specificano il modo in cui il menu di scelta rapida può essere modificato. Questo parametro usa i \_ \* valori CMF descritti in [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).

</dd> </dl>

## <a name="remarks"></a>Commenti

Se gli elementi vengono aggiunti al menu di scelta rapida, è necessario che siano supportati con routine che rispondono in modo appropriato quando uno di questi elementi viene richiamato usando [**DFM \_ INVOKECOMMAND**](dfm-invokecommand.md).

Questo messaggio viene inviato alla funzione di callback o all'oggetto callback a seconda della modalità di implementazione dell'oggetto menu di scelta rapida predefinito. Sono disponibili due API per la relativa implementazione, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).

[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) è una versione estesa di questo messaggio e fornisce ulteriori informazioni al callback. Usare **DFM \_ INVOKECOMMANDEX** se nell'implementazione sono necessarie informazioni aggiuntive fornite da tale interfaccia.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 




