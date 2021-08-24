---
title: Controllo GROUPBOX (menu e altre risorse)
description: Definisce un controllo casella di gruppo. Il controllo è un rettangolo che raggruppa altri controlli. I controlli vengono raggruppati disegnando un bordo intorno a essi e visualizzando il testo specificato nell'angolo superiore sinistro.
ms.assetid: ffca7b68-0326-4fbe-8330-7d1151abb14a
keywords:
- Menu e altre risorse del controllo GROUPBOX
topic_type:
- apiref
api_name:
- GROUPBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05fb8e795cfe483d16406f07fffd2a26df14cebc3c38a07fbef7f2cb78cc245a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602081"
---
# <a name="groupbox-control"></a>Controllo GROUPBOX

Definisce un controllo casella di gruppo. Il controllo è un rettangolo che raggruppa altri controlli. I controlli vengono raggruppati disegnando un bordo intorno a essi e visualizzando il testo specificato nell'angolo superiore sinistro.

**L'istruzione GROUPBOX,** che è possibile usare solo in un'istruzione [**DIALOGEX,**](dialogex-resource.md) definisce il testo, l'identificatore, le dimensioni e gli attributi di una finestra di controllo.

``` syntax
GROUPBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Stile*
</dt> <dd>

Stili dei controlli. Questo valore può essere una combinazione dello stile della classe del pulsante **BS \_ GROUPBOX** e degli stili **WS \_ TABSTOP** **e WS \_ DISABLED.**

Se non si specifica uno stile, lo stile predefinito è **BS \_ GROUPBOX**.

</dd> </dl>

Per altre informazioni sulla sintassi generale di un'istruzione di controllo, vedere [Parametri di controllo comuni](common-control-parameters.md).

## <a name="remarks"></a>Commenti

Quando lo stile contiene **WS \_ TABSTOP** o il testo specifica un tasto di scelta rapida, la tabulazione o la pressione del tasto di scelta rapida sposta lo stato attivo sul primo controllo all'interno del gruppo.

## <a name="examples"></a>Esempio

In questo esempio viene definito un controllo casella di gruppo con l'etichetta Opzioni:

``` syntax
GROUPBOX "Options", 101, 10, 10, 100, 100
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Caselle di gruppo](https://www.bing.com/search?q=Group+Boxes)
</dt> </dl>

 

 




