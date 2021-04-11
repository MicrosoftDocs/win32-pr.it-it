---
title: Controllo LISTBOX (menu e altre risorse)
description: Definisce i controlli di uso comune per una finestra di dialogo o una finestra. Il controllo è un rettangolo contenente un elenco di stringhe, ad esempio i nomi file, da cui l'utente può selezionare.
ms.assetid: 78f6d36e-5079-4f04-87e4-ca55a1161a51
keywords:
- Menu di controllo LISTBOX e altre risorse
topic_type:
- apiref
api_name:
- LISTBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9f062387463917438a988c3b023ca656beef722
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117718"
---
# <a name="listbox-control"></a>LISTBOX (controllo)

Definisce i controlli di uso comune per una finestra di dialogo o una finestra. Il controllo è un rettangolo contenente un elenco di stringhe, ad esempio i nomi file, da cui l'utente può selezionare.

L'istruzione **ListBox** , che può essere utilizzata solo in un'istruzione [**DIALOGEX**](dialogex-resource.md) o **Window** , definisce l'identificatore, le dimensioni e gli attributi di una finestra del controllo.

``` syntax
LISTBOX id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*stile*
</dt> <dd>

Stili del controllo. Questo valore può essere costituito da una combinazione degli stili delle classi della casella di riepilogo e da uno qualsiasi degli stili seguenti: **WS \_ Border** e **WS \_ VSCROLL**.

Se non si specifica uno stile, lo stile predefinito è `LBS_NOTIFY | WS_BORDER` .

</dd> </dl>

Per ulteriori informazioni sulla sintassi generale di un'istruzione di controllo, vedere [parametri di controllo comuni](common-control-parameters.md).

## <a name="examples"></a>Esempio

Questo esempio definisce un controllo casella di riepilogo il cui identificatore è 101:

``` syntax
LISTBOX 101, 10, 10, 100, 100
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**COMBOBOX**](combobox-control.md)
</dt> <dt>

[Caselle di riepilogo](../controls/about-list-boxes.md)
</dt> </dl>

 

 