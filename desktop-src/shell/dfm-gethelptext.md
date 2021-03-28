---
description: Consente all'oggetto callback di specificare una stringa di testo della guida.
title: Messaggio DFM_GETHELPTEXT (Shlobj. h)
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
ms.openlocfilehash: b9aefb1c3a12ff00294ccc536464794a17fccfc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525363"
---
# <a name="dfm_gethelptext-message"></a>\_Messaggio DFM GETHELPTEXT

Consente all'oggetto callback di specificare una stringa di testo della guida.


```C++
DFM_GETHELPTEXT 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(LPTSTR) pszText;

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*idCmd \_ cchMax* \[\]
</dt> <dd>

La parola di basso livello di questo parametro include l'ID del comando. La parola più ordinata include il numero di caratteri nel buffer di *pszText* .

</dd> <dt>

*pszText* \[ out\]
</dt> <dd>

Stringa ANSI con terminazione null contenente il testo della guida.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo messaggio viene inviato alla funzione di callback o all'oggetto callback a seconda del modo in cui viene costruito l'oggetto menu di scelta rapida predefinito. Sono disponibili due API per la relativa costruzione, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).

[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) è una versione estesa di questo messaggio e fornisce ulteriori informazioni al callback. Usare **DFM \_ INVOKECOMMANDEX** se nell'implementazione sono necessarie informazioni aggiuntive fornite da tale interfaccia.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **DFM \_ GETHELPTEXT** (ANSI)<br/>                                              |



 

 




