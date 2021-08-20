---
title: Controllo RTEXT
description: Definisce un controllo testo allineato a destra.
ms.assetid: 66b890db-598e-4255-9d65-a21647005f8e
keywords:
- Menu del controllo RTEXT e altre risorse
topic_type:
- apiref
api_name:
- RTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d0fa44cb1584195518ad39f27fbe7cd802cccc193086ebaf225ce18019b093d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117687064"
---
# <a name="rtext-control"></a>Controllo RTEXT

Definisce un controllo testo allineato a destra. Il controllo è un rettangolo semplice che visualizza il testo specificato allineato a destra nel rettangolo. Il testo viene formattato prima di essere visualizzato. Le parole che si estendono oltre la fine di una riga vengono automaticamente racchiuse all'inizio della riga successiva. Le parole più lunghe della larghezza del controllo vengono troncate.

**L'istruzione RTEXT,** che può essere usata solo in un'istruzione [**DIALOGEX,**](dialogex-resource.md) definisce il testo, l'identificatore, le dimensioni e gli attributi del controllo.

``` syntax
RTEXT text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Stile*
</dt> <dd>

Stili per il controllo di testo, che possono essere qualsiasi combinazione dei seguenti elementi: **WS \_ TABSTOP** e **WS \_ GROUP**.

Se non si specifica uno stile, lo stile predefinito è `SS_RIGHT | WS_GROUP` .

</dd> </dl>

Per altre informazioni sulla sintassi generale di un'istruzione di controllo, vedere [Parametri di controllo comuni.](common-control-parameters.md)

## <a name="examples"></a>Esempio

L'esempio seguente illustra l'uso **dell'istruzione RTEXT:**

``` syntax
RTEXT "Number of Messages", 4, 30, 50, 100, 10
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Controllo**](control-control.md)
</dt> <dt>

[**CTEXT**](ctext-control.md)
</dt> <dt>

[Controlli di modifica](../controls/about-edit-controls.md)
</dt> <dt>

[**LTEXT**](ltext-control.md)
</dt> </dl>

 

 