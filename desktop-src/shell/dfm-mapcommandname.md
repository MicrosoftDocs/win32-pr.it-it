---
description: Inviato dall'implementazione predefinita del menu di scelta rapida per assegnare un nome a un comando di menu.
title: DFM_MAPCOMMANDNAME messaggio (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8aa764f7-d5d4-4a84-94d2-993265e1eb5a
api_name:
- DFM_MAPCOMMANDNAME
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1e3dac1cdb3c04397a59b26a2212fe1c46b611ce72ba029aabd25e0b01c9000b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459977"
---
# <a name="dfm_mapcommandname-message"></a>Messaggio MAPCOMMANDNAME DFM \_

Inviato dall'implementazione predefinita del menu di scelta rapida per assegnare un nome a un comando di menu.


```C++
DFM_MAPCOMMANDNAME

    lParam = (LPARAM)(int*) defaultID;

    wparam = (WPARAM)(LPTSTR) pszCommandName;

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*defaultID* \[ in, out\]
</dt> <dd>

Puntatore all'ID del comando di menu selezionato.

</dd> <dt>

*pszCommandName* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa Unicode contenente il nome del comando.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo messaggio viene inviato alla funzione di callback o all'oggetto callback a seconda della modalità di implementazione dell'oggetto menu di scelta rapida predefinito. Sono disponibili due API per l'implementazione, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).

[**DFM \_ INVOKECOMMANDEX è**](dfm-invokecommandex.md) una versione estesa di questo messaggio e fornisce ulteriori informazioni al callback. Usare **DFM \_ INVOKECOMMANDEX** se le informazioni aggiuntive fornite da tale interfaccia sono necessarie nell'implementazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                      |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 




