---
title: Controllo LTEXT
description: Definisce un controllo testo allineato a sinistra.
ms.assetid: ef6d7d06-3614-4b54-8a23-684d7ef65115
keywords:
- Menu di controllo di LTEXT e altre risorse
topic_type:
- apiref
api_name:
- LTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f253c55238a36f7f6dd43f578c5ea5862a516869
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299741"
---
# <a name="ltext-control"></a>Controllo LTEXT

Definisce un controllo testo allineato a sinistra. Il controllo è un rettangolo semplice che Visualizza il testo specificato allineato a sinistra nel rettangolo. Il testo viene formattato prima di essere visualizzato. Le parole che si estendono oltre la fine di una riga vengono automaticamente racchiuse all'inizio della riga successiva. Le parole più lunghe della larghezza del controllo vengono troncate.

L'istruzione **LTEXT** , che può essere utilizzata solo in un'istruzione [**DIALOGEX**](dialogex-resource.md) , definisce il testo, l'identificatore, le dimensioni e gli attributi del controllo.

``` syntax
LTEXT text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*stile*
</dt> <dd>

Stili del controllo. Questo valore può essere costituito da qualsiasi combinazione dello stile del **\_ RadioButton BS** e dagli stili seguenti: **SS \_ Left**, **WS \_ TABSTOP** e **WS \_ Group**.

Se non si specifica uno stile, lo stile predefinito è `SS_LEFT | WS_GROUP` .

</dd> </dl>

Per ulteriori informazioni sulla sintassi generale di un'istruzione di controllo, vedere [parametri di controllo comuni](common-control-parameters.md).

## <a name="examples"></a>Esempio

Questo esempio definisce un controllo testo allineato a sinistra con etichetta filename:

``` syntax
LTEXT "Filename", 101, 10, 10, 100, 100
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CONTROLLO**](control-control.md)
</dt> <dt>

[**CTEXT**](ctext-control.md)
</dt> <dt>

[Controlli di modifica](../controls/about-edit-controls.md)
</dt> <dt>

[**RTEXT**](rtext-control.md)
</dt> </dl>

 

 