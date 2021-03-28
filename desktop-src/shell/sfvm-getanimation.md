---
description: "Consente all'oggetto callback di specificare che un'animazione deve essere visualizzata mentre gli elementi vengono enumerati in un thread in background. Usato da IShellFolderViewCB:: MessageSFVCB."
ms.assetid: 6f8b3894-f08f-4ebf-a645-87869e7d1b20
title: Messaggio SFVM_GETANIMATION (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60e4281689556e8315da7a9550fd69acc1a327a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131950"
---
# <a name="sfvm_getanimation-message"></a>\_Messaggio GETANIMATION SFVM

Consente all'oggetto callback di specificare che un'animazione deve essere visualizzata mentre gli elementi vengono enumerati in un thread in background. Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETANIMATION 

    wParam = (WPARAM)(HINSTANCE*) phinst;

    lParam = (LPARAM)(WCHAR*) pwszName;

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*phinst* \[ out\]
</dt> <dd>

Handle dell'istanza del modulo da cui deve essere caricata la risorsa.

</dd> <dt>

*pwszName* \[ out\]
</dt> <dd>

Puntatore a una stringa Unicode con terminazione null che contiene il percorso del file AVI o il nome di una risorsa AVI. In alternativa, questo parametro può essere costituito dall'identificatore di risorsa nella parola di basso livello e da 0 nella parola più significativa. Per creare questo valore, usare la macro [**MAKEINTRESOURCE**](/windows/win32/api/winuser/nf-winuser-makeintresourcea) . Il controllo carica la risorsa dal modulo specificato da hinst. Una risorsa AVI deve avere il tipo "AVI".

</dd> </dl>

## <a name="remarks"></a>Commenti

Per impostazione predefinita, l'oggetto visualizzazione cartella di sistema Visualizza l'animazione "torcia" durante un'enumerazione in background.

*phinst* e *pwszName* verranno passati al [controllo animazione](../controls/animation-control-overview.md) con un messaggio di [**\_ apertura ACM**](../controls/acm-open.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
