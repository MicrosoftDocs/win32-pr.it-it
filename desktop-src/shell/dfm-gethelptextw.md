---
description: "DFM_GETHELPTEXTW messaggio: consente all'oggetto callback di specificare una stringa di testo della Guida."
title: DFM_GETHELPTEXTW messaggio (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 85bdd1d0-5b68-44a5-a1b0-4845b5be34d0
api_name:
- DFM_GETHELPTEXTW
- DFM_GETHELPTEXTW
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6271b150bead5be4715259c68711ee67417f6395
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097039"
---
# <a name="dfm_gethelptextw-message"></a>Messaggio DFM \_ GETHELPTEXTW

Consente all'oggetto callback di specificare una stringa di testo della Guida.


```C++
DFM_GETHELPTEXTW 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(WPTSTR) pszText;

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*idCmd \_ cchMax* \[ in\]
</dt> <dd>

La parola più bassa di questo parametro contiene l'ID del comando. La parola più alta contiene il numero di caratteri nel buffer *pszText.*

</dd> <dt>

*pszText* \[ Cambio\]
</dt> <dd>

Stringa Unicode con terminazione Null contenente il testo della Guida.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo messaggio viene inviato alla funzione di callback o all'oggetto callback a seconda di come viene costruito l'oggetto del menu di scelta rapida predefinito. Per la costruzione sono disponibili due API, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).

[**DFM \_ INVOKECOMMANDEX è**](dfm-invokecommandex.md) una versione estesa di questo messaggio e fornisce altre informazioni al callback. Usare **DFM \_ INVOKECOMMANDEX** se le informazioni aggiuntive fornite da tale interfaccia sono necessarie nell'implementazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows Vista \[\]<br/>                                      |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2008 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **DFM \_ GETHELPTEXTW** (Unicode)<br/>                                          |



 

 




