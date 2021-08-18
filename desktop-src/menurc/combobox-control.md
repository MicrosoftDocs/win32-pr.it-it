---
title: Controllo COMBOBOX (menu e altre risorse)
description: Definisce un controllo casella di combinazione (casella combinata).
ms.assetid: 0a0fcfa8-b65c-44c1-89d8-f5020af10f0f
keywords:
- Menu e altre risorse del controllo COMBOBOX
topic_type:
- apiref
api_name:
- COMBOBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd2ffaa64266d9b370cca5215725eb45d0f620054c66562e3f60492441e38890
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972120"
---
# <a name="combobox-control"></a>Controllo COMBOBOX

Definisce un controllo casella di combinazione (casella combinata). Una casella combinata è costituita da una casella di testo statica o da una casella di modifica combinata con una casella di riepilogo. La casella di riepilogo può essere sempre visualizzata o trascinata dall'utente. Se la casella combinata contiene una casella di testo statica, la casella di testo visualizza sempre la selezione (se presente) nella parte casella di riepilogo della casella combinata. Se usa una casella di modifica, l'utente può digitare la selezione desiderata. la casella di riepilogo evidenzia il primo elemento (se presente) corrispondente a quello immesso dall'utente nella casella di modifica. L'utente può quindi selezionare l'elemento evidenziato nella casella di riepilogo per completare la scelta. Inoltre, la casella combinata può essere disegnata dal proprietario e di altezza fissa o variabile.

``` syntax
COMBOBOX id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Stile*
</dt> <dd>

Stili dei controlli. Questo valore può essere una combinazione degli stili della classe COMBOBOX e di uno degli stili seguenti: **WS \_ TABSTOP,** **WS \_ GROUP,** **WS \_ VSCROLL** e **WS \_ DISABLED.**

Se non si specifica uno stile, lo stile predefinito è `CBS_SIMPLE | WS_TABSTOP` .

</dd> </dl>

Il *parametro height* si applica all'altezza di una casella combinata con un elenco a discesa completamente espanso.

Per altre informazioni sulla sintassi generale di un'istruzione di controllo, vedere [Parametri di controllo comuni](common-control-parameters.md).

## <a name="examples"></a>Esempio

Questo esempio definisce un controllo casella combinata con una barra di scorrimento verticale:

``` syntax
COMBOBOX 777, 10, 10, 50, 54, CBS_SIMPLE | WS_VSCROLL | WS_TABSTOP 
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Caselle combinate](../controls/about-combo-boxes.md)
</dt> </dl>

 

 