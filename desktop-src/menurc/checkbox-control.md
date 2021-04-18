---
title: Controllo CHECKBOX (compilatore di risorse)
description: Definisce un controllo casella di controllo.
ms.assetid: 24ee25e5-9de2-4843-a55e-96b897f6ae8e
keywords:
- Menu di controllo CHECKBOX e altre risorse
topic_type:
- apiref
api_name:
- CHECKBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57b4a86a2f08baf7d6e3af9960bd68db1eba86f1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299684"
---
# <a name="checkbox-control"></a>CHECKBOX (controllo)

Definisce un controllo casella di controllo. Il controllo è un rettangolo di piccole dimensioni (casella di controllo) a cui viene visualizzato il testo specificato (in genere, a destra). Quando l'utente seleziona il controllo, il controllo evidenzia il rettangolo e invia un messaggio alla relativa finestra padre.

L'istruzione **CheckBox** , che può essere utilizzata solo in un'istruzione [**DIALOGEX**](dialogex-resource.md) , definisce il testo, l'identificatore, le dimensioni e gli attributi del controllo.

``` syntax
CHECKBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*testo*
</dt> <dd>

Testo da visualizzare a destra del controllo.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*stile*
</dt> <dd>

Stili del controllo. Questo valore può essere una combinazione della **\_ casella** di controllo di stile della classe Button e degli stili **di \_ gruppo** **WS \_ TABSTOP** e WS.

Se non si specifica uno stile, lo stile predefinito è `BS_CHECKBOX | WS_TABSTOP` .

</dd> </dl>

Per ulteriori informazioni sulla sintassi generale di un'istruzione di controllo, vedere [parametri di controllo comuni](common-control-parameters.md).

## <a name="examples"></a>Esempio

Questo esempio definisce un controllo casella di controllo con etichetta corsivo:

``` syntax
CHECKBOX "Italic", 3, 10, 10, 40, 10
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CASELLA di controllo AUTOCHECKBOX**](autocheckbox-control.md)
</dt> <dt>

[**AUTO3STATE**](auto3state-control.md)
</dt> <dt>

[Caselle di controllo](https://www.bing.com/search?q=Check+Boxes)
</dt> <dt>

[**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[**STATE3**](state3-control.md)
</dt> </dl>

 

 