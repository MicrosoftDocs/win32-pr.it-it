---
title: Controllo CTEXT
description: Definisce un controllo di testo centrato.
ms.assetid: 11f42d25-8fe1-4a8b-a5c5-c8cb47cc8c73
keywords:
- Menu di controllo di CTEXT e altre risorse
topic_type:
- apiref
api_name:
- CTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41c12b6c1da5d5bd5c8ce59a01e21b05baf77503
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117663"
---
# <a name="ctext-control"></a>Controllo CTEXT

Definisce un controllo di testo centrato. Il controllo è un rettangolo semplice che Visualizza il testo specificato centrato nel rettangolo. Il testo viene formattato prima di essere visualizzato. Le parole che si estendono oltre la fine di una riga vengono automaticamente racchiuse all'inizio della riga successiva. Le parole più lunghe della larghezza del controllo vengono troncate.

L'istruzione [**LTEXT**](ltext-control.md) , che può essere utilizzata solo in un'istruzione REP, definisce il testo, l'identificatore, le dimensioni e gli attributi del controllo.

``` syntax
CTEXT text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*testo*
</dt> <dd>

Testo che deve essere centrato nell'area rettangolare del controllo.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*stile*
</dt> <dd>

Stili del controllo. Questo valore può essere costituito da qualsiasi combinazione degli stili seguenti: **SS \_ Center**, **WS \_ TABSTOP** e **WS \_ Group**.

Se non si specifica uno stile, lo stile predefinito è `SS_CENTER | WS_GROUP` .

</dd> </dl>

Per ulteriori informazioni sulla sintassi generale di un'istruzione di controllo, vedere [parametri di controllo comuni](common-control-parameters.md).

## <a name="examples"></a>Esempio

Questo esempio definisce un controllo di testo centrato con etichetta filename:

``` syntax
CTEXT "Filename", 101, 10, 10, 100, 100 
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CONTROLLO**](control-control.md)
</dt> <dt>

[Controlli di modifica](../controls/about-edit-controls.md)
</dt> <dt>

[**LTEXT**](ltext-control.md)
</dt> <dt>

[**RTEXT**](rtext-control.md)
</dt> </dl>

 

 