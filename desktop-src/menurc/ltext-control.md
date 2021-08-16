---
title: Controllo LTEXT
description: Definisce un controllo testo allineato a sinistra.
ms.assetid: ef6d7d06-3614-4b54-8a23-684d7ef65115
keywords:
- Menu e altre risorse del controllo LTEXT
topic_type:
- apiref
api_name:
- LTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdaafe752d547466267e8494743e8f0c99ccef0d0fb05b77db5dab2fa358f158
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117870275"
---
# <a name="ltext-control"></a>Controllo LTEXT

Definisce un controllo testo allineato a sinistra. Il controllo è un semplice rettangolo che visualizza il testo specificato allineato a sinistra nel rettangolo. Il testo viene formattato prima della visualizzazione. Le parole che si estendono oltre la fine di una riga vengono automaticamente racchiuse all'inizio della riga successiva. Le parole più lunghe della larghezza del controllo vengono troncate.

**L'istruzione LTEXT,** che può essere usata solo in un'istruzione [**DIALOGEX,**](dialogex-resource.md) definisce il testo, l'identificatore, le dimensioni e gli attributi del controllo.

``` syntax
LTEXT text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Stile*
</dt> <dd>

Stili dei controlli. Questo valore può essere qualsiasi combinazione dello stile **\_ BS RADIOBUTTON** e degli stili seguenti: **SS \_ LEFT,** **WS \_ TABSTOP** e **WS \_ GROUP**.

Se non si specifica uno stile, lo stile predefinito è `SS_LEFT | WS_GROUP` .

</dd> </dl>

Per altre informazioni sulla sintassi generale di un'istruzione di controllo, vedere [Parametri di controllo comuni](common-control-parameters.md).

## <a name="examples"></a>Esempio

In questo esempio viene definito un controllo testo allineato a sinistra con l'etichetta Nome file:

``` syntax
LTEXT "Filename", 101, 10, 10, 100, 100
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Controllo**](control-control.md)
</dt> <dt>

[**CTEXT**](ctext-control.md)
</dt> <dt>

[Modificare i controlli](../controls/about-edit-controls.md)
</dt> <dt>

[**Rtext**](rtext-control.md)
</dt> </dl>

 

 