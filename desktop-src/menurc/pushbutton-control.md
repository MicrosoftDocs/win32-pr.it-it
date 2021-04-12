---
title: Controllo pulsante (menu e altre risorse)
description: Definisce un controllo pulsante di comando. Il controllo è un rettangolo con angoli arrotondati che contiene il testo specificato. Il testo viene centrato nel controllo. Il controllo Invia un messaggio al relativo elemento padre ogni volta che l'utente sceglie il controllo.
ms.assetid: c5fbcfb7-1b7d-4199-acac-d11bfd899298
keywords:
- Menu di controllo pulsante e altre risorse
topic_type:
- apiref
api_name:
- PUSHBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9a303121b7c0eee7ac57fc369164547bd3ae6b9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337470"
---
# <a name="pushbutton-control"></a>Controllo pulsante

Definisce un controllo pulsante di comando. Il controllo è un rettangolo con angoli arrotondati che contiene il testo specificato. Il testo viene centrato nel controllo. Il controllo Invia un messaggio al relativo elemento padre ogni volta che l'utente sceglie il controllo.

``` syntax
PUSHBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*stile*
</dt> <dd>

Stili per il pulsante, che può essere una combinazione dello stile **del \_ pulsante BS** e degli stili seguenti: **WS \_ TABSTOP**, **WS \_ disabled** e **WS \_ Group**.

Se non si specifica uno stile, lo stile predefinito è `BS_PUSHBUTTON | WS_TABSTOP` .

</dd> </dl>

Per ulteriori informazioni sulla sintassi generale di un'istruzione di controllo, vedere [parametri di controllo comuni](common-control-parameters.md).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato l'utilizzo dell'istruzione **pulsante** :

``` syntax
PUSHBUTTON "ON", 7, 10, 10, 20, 10
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[Pulsanti di push](https://www.bing.com/search?q=Push+Buttons)
</dt> </dl>

 

 