---
title: Controllo CHECKBOX (Compilatore di risorse)
description: Definisce un controllo casella di controllo.
ms.assetid: 24ee25e5-9de2-4843-a55e-96b897f6ae8e
keywords:
- Menu e altre risorse del controllo CHECKBOX
topic_type:
- apiref
api_name:
- CHECKBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab103291a919a166d63656718629a7781bdd5f3a4b3023283f2dd114decd966e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461331"
---
# <a name="checkbox-control"></a>Controllo CHECKBOX

Definisce un controllo casella di controllo. Il controllo è un piccolo rettangolo (casella di controllo) a cui è visualizzato il testo specificato (in genere, a destra). Quando l'utente seleziona il controllo, il controllo evidenzia il rettangolo e invia un messaggio alla finestra padre.

**L'istruzione CHECKBOX,** che può essere usata solo in un'istruzione [**DIALOGEX,**](dialogex-resource.md) definisce il testo, l'identificatore, le dimensioni e gli attributi del controllo.

``` syntax
CHECKBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*Testo*
</dt> <dd>

Testo da visualizzare a destra del controllo.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*Stile*
</dt> <dd>

Stili dei controlli. Questo valore può essere una combinazione dello stile della classe del pulsante **BS \_ CHECKBOX** e degli stili **WS \_ TABSTOP** **e WS \_ GROUP.**

Se non si specifica uno stile, lo stile predefinito è `BS_CHECKBOX | WS_TABSTOP` .

</dd> </dl>

Per altre informazioni sulla sintassi generale di un'istruzione di controllo, vedere [Parametri di controllo comuni.](common-control-parameters.md)

## <a name="examples"></a>Esempio

Questo esempio definisce un controllo casella di controllo con etichetta Corsivo:

``` syntax
CHECKBOX "Italic", 3, 10, 10, 40, 10
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CASELLA DI CONTROLLO AUTOMATICA**](autocheckbox-control.md)
</dt> <dt>

[**AUTO3STATE**](auto3state-control.md)
</dt> <dt>

[Caselle](https://www.bing.com/search?q=Check+Boxes)
</dt> <dt>

[**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[**STATE3**](state3-control.md)
</dt> </dl>

 

 