---
title: Controllo AUTO3STATE
description: Definisce una casella di controllo automatica a tre stati.
ms.assetid: 8b27367c-30d0-4591-93d0-756c65255b26
keywords:
- Menu e altre risorse del controllo AUTO3STATE
topic_type:
- apiref
api_name:
- AUTO3STATE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 318d43f0b6d8a16d6e76ae3d12f934e41e265197690a955cfe148dd71176f440
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735213"
---
# <a name="auto3state-control"></a>Controllo AUTO3STATE

Definisce una casella di controllo automatica a tre stati. Il controllo è una casella aperta con il testo specificato posizionato a destra della casella. Se selezionata, la casella avanza automaticamente tra tre stati: selezionata, deselezionata e disabilitata (in grigio). Il controllo invia un messaggio al relativo elemento padre ogni volta che l'utente sceglie il controllo.

``` syntax
AUTO3STATE text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Stile*
</dt> <dd>

Stili per il controllo, che può essere una combinazione dello stile **BS \_ AUTO3STATE** e degli stili seguenti: **WS \_ TABSTOP,** **WS \_ DISABLED** e **WS \_ GROUP**.

Se non si specifica uno stile, lo stile predefinito è `BS_AUTO3STATE | WS_TABSTOP` .

</dd> </dl>

Per altre informazioni sulla sintassi generale di un'istruzione di controllo, vedere [Parametri di controllo comuni](common-control-parameters.md).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**AUTOCHECKBOX**](autocheckbox-control.md)
</dt> <dt>

[Caselle](https://www.bing.com/search?q=Check+Boxes)
</dt> <dt>

[**Casella**](checkbox-control.md)
</dt> <dt>

[**Controllo**](control-control.md)
</dt> <dt>

[**STATE3**](state3-control.md)
</dt> <dt>

[Stili finestra](/windows/desktop/winmsg/window-styles)
</dt> </dl>

 

 