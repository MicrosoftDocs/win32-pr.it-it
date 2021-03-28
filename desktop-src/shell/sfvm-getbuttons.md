---
description: "Consente all'oggetto callback di specificare i pulsanti da aggiungere alla barra degli strumenti. Usato da IShellFolderViewCB:: MessageSFVCB."
ms.assetid: 0c0dbf61-9da9-4bcc-bad9-92c3f78db78f
title: Messaggio SFVM_GETBUTTONS (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ad4ced86909c37ec77bf0470b46a40954f5b61c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883425"
---
# <a name="sfvm_getbuttons-message"></a>\_Messaggio GETbuttons SFVM

Consente all'oggetto callback di specificare i pulsanti da aggiungere alla barra degli strumenti. Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETBUTTONS 

    wParam = (WPARAM)(DWORD) idCmdFirst,cbtnMax;

    lParam = (LPARAM)(LPTBBUTTON) pbtn;

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*idCmdFirst \_ cbtnMax* \[\]
</dt> <dd>

Contiene i valori a 2 16 bit compressi nel parametro con la macro [**MAKEWPARAM**](/windows/win32/api/winuser/nf-winuser-makewparam) . La parola di ordine inferiore contiene l'ID del comando iniziale. La parola di ordine superiore contiene il numero di pulsanti da aggiungere, come specificato nel messaggio [**SFVM \_ GETBUTTONINFO**](sfvm-getbuttoninfo.md) precedente.

</dd> <dt>

*pBtn* \[ out\]
</dt> <dd>

Indirizzo di una matrice di strutture [**TBBUTTON**](/windows/win32/api/commctrl/ns-commctrl-tbbutton) , una per ogni pulsante da aggiungere alla barra degli strumenti.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo messaggio è preceduto da un messaggio [**SFVM \_ GETBUTTONINFO**](sfvm-getbuttoninfo.md) . L'oggetto callback deve gestire il messaggio per specificare il numero di pulsanti e la posizione in cui devono essere posizionati sulla barra degli strumenti. A seconda del modo in cui l'oggetto callback risponde al messaggio **SFVM \_ GETBUTTONINFO** , i pulsanti specificati dal parametro *pBtn* verranno accodati o anteposti ai pulsanti standard dell'oggetto visualizzazione cartella di sistema o sostituiranno il set standard.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
