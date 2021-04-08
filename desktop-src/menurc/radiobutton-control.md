---
title: RADIOBUTTON (controllo)
description: Definisce un controllo pulsante di opzione.
ms.assetid: c427080f-0408-42b4-8888-7333f3eb985d
keywords:
- Menu di controllo RADIOBUTTON e altre risorse
topic_type:
- apiref
api_name:
- RADIOBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67dd559c2d61ca8b2735d393170c177a65735b4b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046743"
---
# <a name="radiobutton-control"></a>RADIOBUTTON (controllo)

Definisce un controllo pulsante di opzione. Il controllo è un piccolo cerchio a cui è visualizzato il testo specificato, in genere a destra. Il controllo evidenzia il cerchio e invia un messaggio alla relativa finestra padre quando l'utente seleziona il pulsante. Il controllo rimuove l'evidenziazione e invia un messaggio quando viene selezionato il pulsante Avanti.

``` syntax
RADIOBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*stile*
</dt> <dd>

Stili per il pulsante di opzione, che può essere una combinazione di stili di classi di pulsanti e gli stili seguenti: **WS \_ TABSTOP**, **WS \_ disabled** e **WS \_ Group**.

Se non si specifica uno stile, lo stile predefinito è `BS_RADIOBUTTON | WS_TABSTOP` .

</dd> </dl>

Per ulteriori informazioni sulla sintassi generale di un'istruzione di controllo, vedere [parametri di controllo comuni](common-control-parameters.md).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato l'utilizzo dell'istruzione **RadioButton** :

``` syntax
RADIOBUTTON "Italic", 100, 10, 10, 40, 10
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[Pulsanti di opzione](https://www.bing.com/search?q=Radio+Buttons)
</dt> </dl>

 

 