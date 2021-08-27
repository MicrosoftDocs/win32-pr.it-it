---
description: Consente all'oggetto callback di specificare che deve essere visualizzata un'animazione mentre gli elementi vengono enumerati in un thread in background. Usato da IShellFolderViewCB::MessageSFVCB.
ms.assetid: 6f8b3894-f08f-4ebf-a645-87869e7d1b20
title: SFVM_GETANIMATION messaggio (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 746d8bc9bc4a6d4e15d9cd5190d7cfcb7d1362daba8ec5478b333458f62787da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008991"
---
# <a name="sfvm_getanimation-message"></a>Messaggio \_ SFVM GETANIMATION

Consente all'oggetto callback di specificare che deve essere visualizzata un'animazione mentre gli elementi vengono enumerati in un thread in background. Usato da [**IShellFolderViewCB::MessageSFVCB.**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)


```C++
SFVM_GETANIMATION 

    wParam = (WPARAM)(HINSTANCE*) phinst;

    lParam = (LPARAM)(WCHAR*) pwszName;

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*phinst* \[ Cambio\]
</dt> <dd>

Handle di istanza del modulo da cui deve essere caricata la risorsa.

</dd> <dt>

*pwszName* \[ Cambio\]
</dt> <dd>

Puntatore a una stringa Unicode con terminazione Null contenente il percorso del file .avi o il nome di una risorsa AVI. In alternativa, questo parametro può essere costituito dall'identificatore di risorsa nella parola di ordine più basso e da 0 nella parola di ordine superiore. Per creare questo valore, usare la macro [**MAKEINTRESOURCE.**](/windows/win32/api/winuser/nf-winuser-makeintresourcea) Il controllo carica la risorsa dal modulo specificato da hinst. Una risorsa AVI deve avere il tipo "AVI".

</dd> </dl>

## <a name="remarks"></a>Commenti

Per impostazione predefinita, l'oggetto visualizzazione cartella di sistema visualizza l'animazione "torcia" durante un'enumerazione dello sfondo.

*phinst* e *pwszName* verranno passati al controllo [animazione](../controls/animation-control-overview.md) con un [**messaggio ACM \_ OPEN.**](../controls/acm-open.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
