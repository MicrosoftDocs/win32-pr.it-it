---
description: Il messaggio WM SYSCOLORCHANGE viene inviato a tutte le finestre di primo livello quando viene apportata una modifica \_ a un'impostazione del colore di sistema.
ms.assetid: ffe61768-86d6-4ea8-ae2d-1095a9afa925
title: WM_SYSCOLORCHANGE messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e39ff8b5189da1a4cf48b7f6923c1cf12e8f30aa20fb26457d54a3f01d1b5c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118483100"
---
# <a name="wm_syscolorchange-message"></a>Messaggio \_ SYSCOLORCHANGE WM

Il **messaggio \_ WM SYSCOLORCHANGE** viene inviato a tutte le finestre di primo livello quando viene apportata una modifica a un'impostazione del colore di sistema.

Una finestra riceve questo messaggio tramite la [**relativa funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il sistema invia un [**messaggio WM \_ PAINT**](wm-paint.md) a qualsiasi finestra interessata da una modifica del colore di sistema.

Le applicazioni con pennelli che usano i colori di sistema esistenti devono eliminare tali pennelli e crearli di nuovo usando i nuovi colori di sistema.

Le finestre di primo livello che usano controlli comuni devono inoltrare il messaggio **\_ SYSCOLORCHANGE DI WM** ai controlli. In caso contrario, i controlli non riceveranno notifica della modifica del colore. Ciò garantisce che i colori usati dai controlli comuni siano coerenti con quelli usati da altri oggetti dell'interfaccia utente. Ad esempio, un controllo barra degli strumenti usa il colore "Oggetti 3D" per disegnare i pulsanti. Se l'utente modifica il colore degli oggetti 3D ma il messaggio **WM \_ SYSCOLORCHANGE** non viene inoltrato alla barra degli strumenti, i pulsanti della barra degli strumenti rimarranno nel colore originale mentre il colore degli altri pulsanti nel sistema cambia.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica dei colori](colors.md)
</dt> <dt>

[Messaggi di colore](color-messages.md)
</dt> <dt>

[**WM \_ PAINT**](wm-paint.md)
</dt> </dl>

 

 
