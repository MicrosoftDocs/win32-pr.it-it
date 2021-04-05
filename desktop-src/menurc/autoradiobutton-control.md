---
title: Controllo AUTORADIOBUTTON
description: Definisce un controllo pulsante di opzione automatico. Questo controllo esegue automaticamente l'esclusione reciproca con gli altri controlli di AUTORADIOBUTTON nello stesso gruppo. Quando si sceglie il pulsante, l'applicazione riceve una notifica con un \_ clic su BN.
ms.assetid: af843084-5213-4934-b291-0787b88ef62d
keywords:
- Menu di controllo AUTORADIOBUTTON e altre risorse
topic_type:
- apiref
api_name:
- AUTORADIOBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67395437303de0adc8c1af226210f8ca2f45958d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718352"
---
# <a name="autoradiobutton-control"></a>Controllo AUTORADIOBUTTON

Definisce un controllo pulsante di opzione automatico. Questo controllo esegue automaticamente l'esclusione reciproca con gli altri controlli di **AUTORADIOBUTTON** nello stesso gruppo. Quando si sceglie il pulsante, l'applicazione riceve una notifica con un **\_ clic su BN**.

``` syntax
AUTORADIOBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*testo*
</dt> <dd>

Testo che verrà visualizzato accanto al pulsante di opzione.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*stile*
</dt> <dd>

Stili per il pulsante di opzione automatico, che può essere una combinazione di stili di classi di pulsanti e gli stili seguenti: **WS \_ TABSTOP**, **WS \_ disabled** e **WS \_ Group**.

Se non si specifica uno stile, lo stile predefinito è `BS_AUTORADIOBUTTON | WS_TABSTOP` .

</dd> </dl>

Per ulteriori informazioni sulla sintassi generale di un'istruzione di controllo, vedere [parametri di controllo comuni](common-control-parameters.md).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CONTROLLO**](control-control.md)
</dt> <dt>

[Pulsanti di opzione](https://www.bing.com/search?q=Radio+Buttons)
</dt> <dt>

[**RADIOBUTTON**](radiobutton-control.md)
</dt> </dl>

 

 




