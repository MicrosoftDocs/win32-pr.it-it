---
title: Controllo RTEXT
description: Definisce un controllo di testo allineato a destra.
ms.assetid: 66b890db-598e-4255-9d65-a21647005f8e
keywords:
- Menu di controllo di RTEXT e altre risorse
topic_type:
- apiref
api_name:
- RTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bc56a870df7ebf5d2696e70573ae320220e803c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104473094"
---
# <a name="rtext-control"></a>Controllo RTEXT

Definisce un controllo di testo allineato a destra. Il controllo è un rettangolo semplice che Visualizza il testo specificato allineato a destra nel rettangolo. Il testo viene formattato prima di essere visualizzato. Le parole che si estendono oltre la fine di una riga vengono automaticamente racchiuse all'inizio della riga successiva. Le parole più lunghe della larghezza del controllo vengono troncate.

L'istruzione **RTEXT** , che può essere utilizzata solo in un'istruzione [**DIALOGEX**](dialogex-resource.md) , definisce il testo, l'identificatore, le dimensioni e gli attributi del controllo.

``` syntax
RTEXT text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*stile*
</dt> <dd>

Stili per il controllo testo, che può essere una qualsiasi combinazione delle seguenti: **WS \_ TABSTOP** e **WS \_ Group**.

Se non si specifica uno stile, lo stile predefinito è `SS_RIGHT | WS_GROUP` .

</dd> </dl>

Per ulteriori informazioni sulla sintassi generale di un'istruzione di controllo, vedere [parametri di controllo comuni](common-control-parameters.md).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato l'utilizzo dell'istruzione **RTEXT** :

``` syntax
RTEXT "Number of Messages", 4, 30, 50, 100, 10
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CONTROLLO**](control-control.md)
</dt> <dt>

[**CTEXT**](ctext-control.md)
</dt> <dt>

[Controlli di modifica](../controls/about-edit-controls.md)
</dt> <dt>

[**LTEXT**](ltext-control.md)
</dt> </dl>

 

 