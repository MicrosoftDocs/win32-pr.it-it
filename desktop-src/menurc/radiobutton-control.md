---
title: Controllo RADIOBUTTON
description: Definisce un controllo pulsante di opzione.
ms.assetid: c427080f-0408-42b4-8888-7333f3eb985d
keywords:
- Menu e altre risorse del controllo RADIOBUTTON
topic_type:
- apiref
api_name:
- RADIOBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18b01d6b2313ec4b881f182fd4a4ca34cf5bbf713dca9f329173d1817132606d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952251"
---
# <a name="radiobutton-control"></a>Controllo RADIOBUTTON

Definisce un controllo pulsante di opzione. Il controllo è un piccolo cerchio con il testo specificato visualizzato accanto, in genere a destra. Il controllo evidenzia il cerchio e invia un messaggio alla relativa finestra padre quando l'utente seleziona il pulsante. Il controllo rimuove l'evidenziazione e invia un messaggio alla successiva selezione del pulsante.

``` syntax
RADIOBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Stile*
</dt> <dd>

Stili per il pulsante di opzione, che può essere una combinazione di stili di classe BUTTON e gli stili seguenti: **WS \_ TABSTOP,** **WS \_ DISABLED** e **WS \_ GROUP**.

Se non si specifica uno stile, lo stile predefinito è `BS_RADIOBUTTON | WS_TABSTOP` .

</dd> </dl>

Per altre informazioni sulla sintassi generale di un'istruzione di controllo, vedere [Parametri di controllo comuni](common-control-parameters.md).

## <a name="examples"></a>Esempio

L'esempio seguente illustra l'uso **dell'istruzione RADIOBUTTON:**

``` syntax
RADIOBUTTON "Italic", 100, 10, 10, 40, 10
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[Pulsanti](https://www.bing.com/search?q=Radio+Buttons)
</dt> </dl>

 

 