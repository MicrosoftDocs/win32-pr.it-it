---
title: Controllo STATE3
description: Definisce un controllo casella di controllo a tre stati. Il controllo è identico a un controllo CHECKBOX, ad eccezione del fatto che ha tre stati selezionati, deselezionati e disabilitati (in grigio).
ms.assetid: 74659827-ce46-4d36-a5e2-3a97e8fd1c04
keywords:
- Menu di controllo STATE3 e altre risorse
topic_type:
- apiref
api_name:
- STATE3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53a2c6b6078b13d9aa7b69506f51dc58335f414884b53447b5f7a16c37497a91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117686868"
---
# <a name="state3-control"></a>Controllo STATE3

Definisce un controllo casella di controllo a tre stati. Il controllo è identico a un [**controllo CHECKBOX**](checkbox-control.md), ad eccezione del fatto che ha tre stati: checked, unchecked e disabled (in grigio).

``` syntax
STATE3 text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*Testo*
</dt> <dd>

Testo da visualizzare a destra del controllo.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*Stile*
</dt> <dd>

Stili dei controlli. Questo valore può essere una combinazione dello stile della classe del pulsante **BS \_ 3STATE** e degli stili **WS \_ TABSTOP** **e WS \_ GROUP.**

Se non si specifica uno stile, lo stile predefinito è `BS_3STATE | WS_TABSTOP` .

</dd> </dl>

Per altre informazioni sulla sintassi generale di un'istruzione di controllo, vedere [Parametri di controllo comuni](common-control-parameters.md).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**AUTOCHECKBOX**](autocheckbox-control.md)
</dt> <dt>

[Caselle](https://www.bing.com/search?q=Check+Boxes)
</dt> <dt>

[**Casella**](checkbox-control.md)
</dt> <dt>

[**Controllo**](control-control.md)
</dt> </dl>

 

 




