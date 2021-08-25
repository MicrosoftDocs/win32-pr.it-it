---
title: Controllo CTEXT
description: Definisce un controllo di testo centrato.
ms.assetid: 11f42d25-8fe1-4a8b-a5c5-c8cb47cc8c73
keywords:
- Menu e altre risorse del controllo CTEXT
topic_type:
- apiref
api_name:
- CTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6b220448fcaa6cbbbb6b01c605a9b5fd6e03f8dc6a60a0e409f6f275d9b74b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826001"
---
# <a name="ctext-control"></a>Controllo CTEXT

Definisce un controllo di testo centrato. Il controllo è un semplice rettangolo che visualizza il testo specificato centrato nel rettangolo. Il testo viene formattato prima della visualizzazione. Le parole che si estendono oltre la fine di una riga vengono automaticamente racchiuse all'inizio della riga successiva. Le parole più lunghe della larghezza del controllo vengono troncate.

[**L'istruzione LTEXT,**](ltext-control.md) che può essere usata solo in un'istruzione rep, definisce il testo, l'identificatore, le dimensioni e gli attributi del controllo.

``` syntax
CTEXT text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*Testo*
</dt> <dd>

Testo da centrare nell'area rettangolare del controllo.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*Stile*
</dt> <dd>

Stili dei controlli. Questo valore può essere qualsiasi combinazione degli stili **seguenti: SS \_ CENTER,** **WS \_ TABSTOP** e **WS \_ GROUP**.

Se non si specifica uno stile, lo stile predefinito è `SS_CENTER | WS_GROUP` .

</dd> </dl>

Per altre informazioni sulla sintassi generale di un'istruzione di controllo, vedere [Parametri di controllo comuni](common-control-parameters.md).

## <a name="examples"></a>Esempio

In questo esempio viene definito un controllo di testo centrato con l'etichetta Nome file:

``` syntax
CTEXT "Filename", 101, 10, 10, 100, 100 
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Controllo**](control-control.md)
</dt> <dt>

[Modificare i controlli](../controls/about-edit-controls.md)
</dt> <dt>

[**LTEXT**](ltext-control.md)
</dt> <dt>

[**Rtext**](rtext-control.md)
</dt> </dl>

 

 