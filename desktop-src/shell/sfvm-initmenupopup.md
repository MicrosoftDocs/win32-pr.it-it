---
description: Consente all'oggetto callback di modificare Windows menu a comparsa di Esplora risorse prima che venga visualizzato. Usato da IShellFolderViewCB::MessageSFVCB.
title: SFVM_INITMENUPOPUP messaggio (Shlobj.h)
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
ms.openlocfilehash: fd69d19f753c1c72c1e0c143a0aface2cdb234cb2ace8c87d559834b97bbf0f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592317"
---
# <a name="sfvm_initmenupopup-message"></a>Messaggio \_ SFVM INITMENUPOPUP

Consente all'oggetto callback di modificare Windows menu a comparsa di Esplora risorse prima che venga visualizzato. Usato da [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_INITMENUPOPUP 

    wParam = (WPARAM)(int) idCmd,nIndex;

    lParam = (LPARAM)(HMENU) hmenu;

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*idCmd \_ nIndex* \[ in\]
</dt> <dd>

La parola di ordine basso di questo parametro contiene il valore del primo ID comando riservato per i comandi client. La parola più alta contiene l'indice del menu.

</dd> <dt>

*hmenu* \[ in, out\]
</dt> <dd>

Handle del menu.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'oggetto visualizzazione cartella di sistema invia questo messaggio quando viene selezionato un menu, ma prima che venga visualizzato. Elaborare questo messaggio se, ad esempio, è necessario abilitare o disabilitare i comandi di menu. Il menu popup può essere:

-   Menu File, Modifica o Visualizza.
-   Menu di primo livello definito dal client.
-   Sottomenu definito dal client.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SFVM \_ MERGEMENU**](sfvm-mergemenu.md)
</dt> </dl>

 

 
