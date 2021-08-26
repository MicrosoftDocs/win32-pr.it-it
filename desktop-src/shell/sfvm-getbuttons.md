---
description: Consente all'oggetto callback di specificare i pulsanti da aggiungere alla barra degli strumenti. Usato da IShellFolderViewCB::MessageSFVCB.
ms.assetid: 0c0dbf61-9da9-4bcc-bad9-92c3f78db78f
title: SFVM_GETBUTTONS messaggio (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 299641ef45d17a6ad1e4d709c3250abe220e297daedabcb563eeba9dcf56262a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008981"
---
# <a name="sfvm_getbuttons-message"></a>Messaggio \_ SFVM GETBUTTONS

Consente all'oggetto callback di specificare i pulsanti da aggiungere alla barra degli strumenti. Usato da [**IShellFolderViewCB::MessageSFVCB.**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)


```C++
SFVM_GETBUTTONS 

    wParam = (WPARAM)(DWORD) idCmdFirst,cbtnMax;

    lParam = (LPARAM)(LPTBBUTTON) pbtn;

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*idCmdFirst \_ cbtnMax* \[ in\]
</dt> <dd>

Contiene due valori a 16 bit contenuti nel parametro con la macro [**MAKEWPARAM.**](/windows/win32/api/winuser/nf-winuser-makewparam) La parola più bassa contiene l'ID comando iniziale. La parola di ordine superiore contiene il numero di pulsanti da aggiungere, come specificato nel messaggio [**\_ SFVM GETBUTTONINFO**](sfvm-getbuttoninfo.md) precedente.

</dd> <dt>

*pbtn* \[ Cambio\]
</dt> <dd>

Indirizzo di una matrice di [**strutture TBBUTTON,**](/windows/win32/api/commctrl/ns-commctrl-tbbutton) una per ogni pulsante da aggiungere alla barra degli strumenti.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo messaggio è preceduto da un [**messaggio \_ SFVM GETBUTTONINFO.**](sfvm-getbuttoninfo.md) L'oggetto callback deve gestire il messaggio per specificare il numero di pulsanti e la posizione in cui devono essere posizionati sulla barra degli strumenti. A seconda del modo in cui l'oggetto callback risponde al messaggio **\_ SFVM GETBUTTONINFO,** i pulsanti specificati dal parametro *pbtn* verranno accodati o anteposti ai pulsanti standard dell'oggetto visualizzazione cartella di sistema oppure sostituiranno il set standard.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
