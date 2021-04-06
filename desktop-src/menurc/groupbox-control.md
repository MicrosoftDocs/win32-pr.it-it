---
title: Controllo GROUPBOX (menu e altre risorse)
description: Definisce un controllo casella di gruppo. Il controllo è un rettangolo che raggruppa altri controlli. I controlli sono raggruppati disegnando un bordo intorno a essi e visualizzando il testo specificato nell'angolo superiore sinistro.
ms.assetid: ffca7b68-0326-4fbe-8330-7d1151abb14a
keywords:
- Menu di controllo GROUPBOX e altre risorse
topic_type:
- apiref
api_name:
- GROUPBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4f77461099362e4f100924f82d95dffa09a94fa
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/12/2019
ms.locfileid: "104046053"
---
# <a name="groupbox-control"></a>Controllo GROUPBOX

Definisce un controllo casella di gruppo. Il controllo è un rettangolo che raggruppa altri controlli. I controlli sono raggruppati disegnando un bordo intorno a essi e visualizzando il testo specificato nell'angolo superiore sinistro.

L'istruzione **GroupBox** , che può essere utilizzata solo in un'istruzione [**DIALOGEX**](dialogex-resource.md) , definisce il testo, l'identificatore, le dimensioni e gli attributi di una finestra del controllo.

``` syntax
GROUPBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*stile*
</dt> <dd>

Stili del controllo. Questo valore può essere una combinazione dello stile della classe Button **BS \_ GroupBox** e degli stili **WS \_ TABSTOP** e **WS \_ disabled** .

Se non si specifica uno stile, lo stile predefinito è **BS \_ GroupBox**.

</dd> </dl>

Per ulteriori informazioni sulla sintassi generale di un'istruzione di controllo, vedere [parametri di controllo comuni](common-control-parameters.md).

## <a name="remarks"></a>Commenti

Quando lo stile contiene **WS \_ TABSTOP** o il testo specifica un tasto di scelta rapida, la tabulazione o la pressione del tasto di scelta rapida Sposta lo stato attivo sul primo controllo all'interno del gruppo.

## <a name="examples"></a>Esempio

Questo esempio definisce un controllo casella di gruppo con etichetta opzioni:

``` syntax
GROUPBOX "Options", 101, 10, 10, 100, 100
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Caselle di gruppo](https://www.bing.com/search?q=Group+Boxes)
</dt> </dl>

 

 




