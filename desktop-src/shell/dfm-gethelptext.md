---
description: "DFM_GETHELPTEXT messaggio: consente all'oggetto callback di specificare una stringa di testo della Guida."
title: DFM_GETHELPTEXT messaggio (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 40ed981b-6d03-4c4f-9e70-1a01d49edcb0
api_name:
- DFM_GETHELPTEXT
- DFM_GETHELPTEXT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2428fe6696ff5949a0b25487437c8f3408b95f65
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097069"
---
# <a name="dfm_gethelptext-message"></a>Messaggio DFM \_ GETHELPTEXT

Consente all'oggetto callback di specificare una stringa di testo della Guida.


```C++
DFM_GETHELPTEXT 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(LPTSTR) pszText;

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*idCmd \_ cchMax* \[ in\]
</dt> <dd>

La parola più bassa di questo parametro contiene l'ID del comando. La parola più alta contiene il numero di caratteri nel buffer *pszText.*

</dd> <dt>

*pszText* \[ Cambio\]
</dt> <dd>

Stringa ANSI con terminazione Null contenente il testo della Guida.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo messaggio viene inviato alla funzione di callback o all'oggetto callback a seconda di come viene costruito l'oggetto del menu di scelta rapida predefinito. Per la costruzione sono disponibili due API, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).

[**DFM \_ INVOKECOMMANDEX è**](dfm-invokecommandex.md) una versione estesa di questo messaggio e fornisce ulteriori informazioni al callback. Usare **DFM \_ INVOKECOMMANDEX** se le informazioni aggiuntive fornite da tale interfaccia sono necessarie nell'implementazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows Vista \[\]<br/>                                      |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2008 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **DFM \_ GETHELPTEXT** (ANSI)<br/>                                              |



 

 




