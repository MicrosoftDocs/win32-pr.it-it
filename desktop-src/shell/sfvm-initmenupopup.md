---
description: "Consente all'oggetto callback di modificare un menu a comparsa di Esplora risorse prima che venga visualizzato. Usato da IShellFolderViewCB:: MessageSFVCB."
title: Messaggio SFVM_INITMENUPOPUP (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9d7e96e9-c52e-43bd-945b-05db33c8dfd0
api_name:
- SFVM_INITMENUPOPUP
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1f9a2a169b232fe3ad16eeee8816536ed81c74dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980834"
---
# <a name="sfvm_initmenupopup-message"></a>\_Messaggio SFVM INITMENUPOPUP

Consente all'oggetto callback di modificare un menu a comparsa di Esplora risorse prima che venga visualizzato. Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_INITMENUPOPUP 

    wParam = (WPARAM)(int) idCmd,nIndex;

    lParam = (LPARAM)(HMENU) hmenu;

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*idCmd \_ nIndex* \[\]
</dt> <dd>

La parola più bassa di questo parametro include il valore del primo ID comando riservato per i comandi client. La parola più ordinata include l'indice del menu.

</dd> <dt>

*HMENU* \[ in uscita\]
</dt> <dd>

Handle del menu.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'oggetto visualizzazione cartella di sistema invia questo messaggio quando viene selezionato un menu, ma prima che venga visualizzato. Elaborare questo messaggio se, ad esempio, è necessario abilitare o disabilitare i comandi di menu. Il menu popup può essere:

-   Menu file, modifica o Visualizza.
-   Menu di primo livello definito dal client.
-   Sottomenu definito dal client.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_MERGEMENU SFVM**](sfvm-mergemenu.md)
</dt> </dl>

 

 
