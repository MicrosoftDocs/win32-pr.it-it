---
title: Controllo AUTO3STATE
description: Definisce una casella di controllo automatica a tre stati.
ms.assetid: 8b27367c-30d0-4591-93d0-756c65255b26
keywords:
- Menu di controllo di AUTO3STATE e altre risorse
topic_type:
- apiref
api_name:
- AUTO3STATE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de184a639de7beee7ac05bdf63609ae29a0f034b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117667"
---
# <a name="auto3state-control"></a>Controllo AUTO3STATE

Definisce una casella di controllo automatica a tre stati. Il controllo è una casella aperta con il testo specificato posizionato a destra della casella. Quando viene scelto, la casella viene spostata automaticamente tra tre stati: selezionata, deselezionata e disabilitata (in grigio). Il controllo Invia un messaggio al relativo elemento padre ogni volta che l'utente sceglie il controllo.

``` syntax
AUTO3STATE text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*stile*
</dt> <dd>

Stili per il controllo, che può essere una combinazione dello stile **BS \_ AUTO3STATE** e degli stili seguenti: **WS \_ TABSTOP**, **WS \_ disabled** e **WS \_ Group**.

Se non si specifica uno stile, lo stile predefinito è `BS_AUTO3STATE | WS_TABSTOP` .

</dd> </dl>

Per ulteriori informazioni sulla sintassi generale di un'istruzione di controllo, vedere [parametri di controllo comuni](common-control-parameters.md).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CASELLA di controllo AUTOCHECKBOX**](autocheckbox-control.md)
</dt> <dt>

[Caselle di controllo](https://www.bing.com/search?q=Check+Boxes)
</dt> <dt>

[**CASELLA**](checkbox-control.md)
</dt> <dt>

[**CONTROLLO**](control-control.md)
</dt> <dt>

[**STATE3**](state3-control.md)
</dt> <dt>

[Stili finestra](/windows/desktop/winmsg/window-styles)
</dt> </dl>

 

 