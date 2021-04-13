---
title: Controllo COMBOBOX (menu e altre risorse)
description: Definisce un controllo casella combinata (casella combinata).
ms.assetid: 0a0fcfa8-b65c-44c1-89d8-f5020af10f0f
keywords:
- Menu di controllo COMBOBOX e altre risorse
topic_type:
- apiref
api_name:
- COMBOBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 311cb45282b949a166add8d3aececc0698803fe5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398917"
---
# <a name="combobox-control"></a>Controllo COMBOBOX

Definisce un controllo casella combinata (casella combinata). Una casella combinata è costituita da una casella di testo statica o da una casella di modifica combinata con una casella di riepilogo. La casella di riepilogo può essere visualizzata sempre o spostata dall'utente. Se la casella combinata contiene una casella di testo statica, nella casella di testo viene sempre visualizzata la selezione, se presente, nella casella combinata della casella combinata. Se usa una casella di modifica, l'utente può digitare la selezione desiderata; nella casella di riepilogo viene evidenziato il primo elemento, se presente, che corrisponde a quello immesso dall'utente nella casella di modifica. L'utente può quindi selezionare l'elemento evidenziato nella casella di riepilogo per completare la scelta. Inoltre, la casella combinata può essere disegnata dal proprietario e di altezza fissa o variabile.

``` syntax
COMBOBOX id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*stile*
</dt> <dd>

Stili del controllo. Questo valore può essere una combinazione degli stili della classe COMBOBOX e di uno degli stili seguenti: **WS \_ TABSTOP**, **WS \_ Group**, **WS \_ VSCROLL** e **WS \_ disabled**.

Se non si specifica uno stile, lo stile predefinito è `CBS_SIMPLE | WS_TABSTOP` .

</dd> </dl>

Il parametro *Height* si applica all'altezza di una casella combinata con un elenco a discesa completamente espanso.

Per ulteriori informazioni sulla sintassi generale di un'istruzione di controllo, vedere [parametri di controllo comuni](common-control-parameters.md).

## <a name="examples"></a>Esempio

Questo esempio definisce un controllo casella combinata con una barra di scorrimento verticale:

``` syntax
COMBOBOX 777, 10, 10, 50, 54, CBS_SIMPLE | WS_VSCROLL | WS_TABSTOP 
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Caselle combinate](../controls/about-combo-boxes.md)
</dt> </dl>

 

 