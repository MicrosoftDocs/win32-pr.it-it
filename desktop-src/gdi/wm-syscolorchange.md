---
description: Il \_ messaggio WM SYSCOLORCHANGE viene inviato a tutte le finestre di primo livello quando viene apportata una modifica a un'impostazione dei colori di sistema.
ms.assetid: ffe61768-86d6-4ea8-ae2d-1095a9afa925
title: Messaggio WM_SYSCOLORCHANGE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac3883f0534d91a6d852b0e70fbb4edabdcab56b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980791"
---
# <a name="wm_syscolorchange-message"></a>\_Messaggio SYSCOLORCHANGE WM

Il messaggio **WM \_ SYSCOLORCHANGE** viene inviato a tutte le finestre di primo livello quando viene apportata una modifica a un'impostazione dei colori di sistema.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


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

Il sistema invia un messaggio di [**\_ disegno WM**](wm-paint.md) a qualsiasi finestra interessata da una modifica del colore di sistema.

Le applicazioni che hanno pennelli che usano i colori di sistema esistenti devono eliminare tali pennelli e ricrearli usando i nuovi colori di sistema.

Le finestre di primo livello che usano controlli comuni devono trasmettere il messaggio **WM \_ SYSCOLORCHANGE** ai controlli; in caso contrario, i controlli non riceveranno una notifica della modifica del colore. In questo modo si garantisce che i colori utilizzati dai controlli comuni siano coerenti con quelli utilizzati da altri oggetti dell'interfaccia utente. Ad esempio, un controllo Toolbar usa il colore "oggetti 3D" per creare i pulsanti. Se l'utente modifica il colore degli oggetti 3D ma il messaggio **WM \_ SYSCOLORCHANGE** non viene trasmesso alla barra degli strumenti, i pulsanti della barra degli strumenti rimarranno nel colore originale mentre viene modificato il colore di altri pulsanti del sistema.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica sui colori](colors.md)
</dt> <dt>

[Messaggi colori](color-messages.md)
</dt> <dt>

[**\_disegno WM**](wm-paint.md)
</dt> </dl>

 

 
