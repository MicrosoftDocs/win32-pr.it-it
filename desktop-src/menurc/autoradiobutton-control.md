---
title: Controllo AUTORADIOBUTTON
description: Definisce un controllo pulsante di opzione automatico. Questo controllo esegue automaticamente l'esclusione reciproca con gli altri controlli AUTORADIOBUTTON nello stesso gruppo. Quando si sceglie il pulsante, l'applicazione viene notificata con BN \_ CLICKED.
ms.assetid: af843084-5213-4934-b291-0787b88ef62d
keywords:
- Menu e altre risorse del controllo AUTORADIOBUTTON
topic_type:
- apiref
api_name:
- AUTORADIOBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29c8a966a21b07744ce05063ae8c68f09156c47717fcff825875f82b4535f945
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118235650"
---
# <a name="autoradiobutton-control"></a>Controllo AUTORADIOBUTTON

Definisce un controllo pulsante di opzione automatico. Questo controllo esegue automaticamente l'esclusione reciproca con gli altri **controlli AUTORADIOBUTTON** nello stesso gruppo. Quando si sceglie il pulsante, l'applicazione viene notificata con **BN \_ CLICKED.**

``` syntax
AUTORADIOBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*Testo*
</dt> <dd>

Testo che verrà visualizzato accanto al pulsante di opzione.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*Stile*
</dt> <dd>

Stili per il pulsante di opzione automatico, che può essere una combinazione di stili di classe BUTTON e gli stili seguenti: **WS \_ TABSTOP,** **WS \_ DISABLED** e **WS \_ GROUP**.

Se non si specifica uno stile, lo stile predefinito è `BS_AUTORADIOBUTTON | WS_TABSTOP` .

</dd> </dl>

Per altre informazioni sulla sintassi generale di un'istruzione di controllo, vedere [Parametri di controllo comuni](common-control-parameters.md).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Controllo**](control-control.md)
</dt> <dt>

[Pulsanti](https://www.bing.com/search?q=Radio+Buttons)
</dt> <dt>

[**Radiobutton**](radiobutton-control.md)
</dt> </dl>

 

 




