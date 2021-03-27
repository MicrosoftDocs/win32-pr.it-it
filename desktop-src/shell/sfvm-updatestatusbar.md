---
description: "Notifica all'oggetto di callback che la barra di stato è in fase di aggiornamento. Usato da IShellFolderViewCB:: MessageSFVCB."
title: Messaggio SFVM_UPDATESTATUSBAR (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: f1bac364-1011-4308-8b9b-8ed1800dd30d
api_name:
- SFVM_UPDATESTATUSBAR
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 14045c797d7292099c1c7b2c67f5958609d8d6b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994813"
---
# <a name="sfvm_updatestatusbar-message"></a>\_Messaggio SFVM UPDATESTATUSBAR

Notifica all'oggetto di callback che la barra di stato è in fase di aggiornamento. Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_UPDATESTATUSBAR 

    wParam = (WPARAM)(BOOL) fInitialize;

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*fInitialize* \[ in\]
</dt> <dd>

Valore **bool** che è impostato su **true** se la barra di stato è in fase di inizializzazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando si riceve la notifica:

-   Restituisce \_ OK se si gestirà l'aggiornamento.
-   Return MAKE \_ HRESULT (SEverity \_ Success, 0, 1) per fare in modo che l'oggetto visualizzazione cartella di sistema imposti il testo della barra di stato.
-   Return E \_ non consentono all'oggetto visualizzazione cartella di sistema di gestire la barra di stato.

Il testo della barra di stato predefinito è il seguente.



| Stato                      | Testo barra di stato                         |
|-----------------------------|-----------------------------------------|
| Nessun elemento selezionato           | " \# \# oggetti" (nella cartella)          |
| Un elemento selezionato           | Infotip per l'elemento, se disponibile. |
| Più di un elemento selezionato | " \# \# oggetti selezionati"                 |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
