---
description: Inviato alla finestra proprietaria di un controllo o di una voce di menu quando viene creato il controllo o il menu.
ms.assetid: 4584a3da-6c92-4ecd-8cf2-e4afc1b8321d
title: Messaggio DFM_WM_MEASUREITEM (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61c4ad79acf221ecaabf9060940ad2514422bef1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401617"
---
# <a name="dfm_wm_measureitem-message"></a>DFM \_ WM \_ MeasureItem messaggio

Inviato alla finestra proprietaria di un controllo o di una voce di menu quando viene creato il controllo o il menu.


```C++
DFM_WM_MEASUREITEM 

    wParam = (WPARAM);

    lParam = (LPARAM)(LPMEASUREITEMSTRUCT) lpMeasureItem;

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Valore del membro **CtlID** della struttura [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) a cui punta il parametro *lpMeasureItem* . Questo valore identifica il controllo che ha inviato il messaggio **DFM \_ WM \_ MeasureItem** .

</dd> <dt>

*lpMeasureItem* \[ out\]
</dt> <dd>

Puntatore a una struttura [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) che contiene le dimensioni del controllo creato dal proprietario o della voce di menu.

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando la finestra proprietaria riceve il messaggio **DFM \_ WM \_ MeasureItem** , il proprietario compila la struttura [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) a cui punta il parametro *lpMeasureItem* del messaggio e restituisce; in questo modo si informa il sistema delle dimensioni del controllo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
