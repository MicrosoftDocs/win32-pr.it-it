---
title: Controllo STATE3
description: Definisce un controllo casella di controllo a tre stati. Il controllo è identico a una casella di controllo, ad eccezione del fatto che ha tre stati controllati, deselezionati e disabilitati (in grigio).
ms.assetid: 74659827-ce46-4d36-a5e2-3a97e8fd1c04
keywords:
- Menu di controllo di STATE3 e altre risorse
topic_type:
- apiref
api_name:
- STATE3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24333fa9567db5613896f26429b72ff68e029335
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718130"
---
# <a name="state3-control"></a>Controllo STATE3

Definisce un controllo casella di controllo a tre stati. Il controllo è identico a una [**casella**](checkbox-control.md)di controllo, ad eccezione del fatto che ha tre stati: checked, dechecked e Disabled (grigio).

``` syntax
STATE3 text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*testo*
</dt> <dd>

Testo da visualizzare a destra del controllo.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*stile*
</dt> <dd>

Stili del controllo. Questo valore può essere una combinazione dello stile della classe Button **BS \_ 3STATE** e degli stili di **\_ gruppo** **WS \_ TABSTOP** e WS.

Se non si specifica uno stile, lo stile predefinito è `BS_3STATE | WS_TABSTOP` .

</dd> </dl>

Per ulteriori informazioni sulla sintassi generale di un'istruzione di controllo, vedere [parametri di controllo comuni](common-control-parameters.md).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CASELLA di controllo AUTOCHECKBOX**](autocheckbox-control.md)
</dt> <dt>

[Caselle di controllo](https://www.bing.com/search?q=Check+Boxes)
</dt> <dt>

[**CASELLA**](checkbox-control.md)
</dt> <dt>

[**CONTROLLO**](control-control.md)
</dt> </dl>

 

 




