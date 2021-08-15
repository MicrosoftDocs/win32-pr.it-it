---
title: Controllo LISTBOX (menu e altre risorse)
description: Definisce i controlli di uso comune per una finestra di dialogo o una finestra. Il controllo è un rettangolo contenente un elenco di stringhe(ad esempio nomi file) da cui l'utente può selezionare.
ms.assetid: 78f6d36e-5079-4f04-87e4-ca55a1161a51
keywords:
- Menu e altre risorse del controllo LISTBOX
topic_type:
- apiref
api_name:
- LISTBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 676ea07f7d66a0d84997f0b2b22b9973c326db0fb603caedcc631caeffffaf98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119226349"
---
# <a name="listbox-control"></a>Controllo LISTBOX

Definisce i controlli di uso comune per una finestra di dialogo o una finestra. Il controllo è un rettangolo contenente un elenco di stringhe(ad esempio nomi file) da cui l'utente può selezionare.

**L'istruzione LISTBOX,** che può essere usata solo in un'istruzione [**DIALOGEX**](dialogex-resource.md) o **WINDOW,** definisce l'identificatore, le dimensioni e gli attributi di una finestra di controllo.

``` syntax
LISTBOX id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Stile*
</dt> <dd>

Stili dei controlli. Questo valore può essere una combinazione degli stili della classe casella di riepilogo e di uno degli stili seguenti: **WS \_ BORDER** e **WS \_ VSCROLL**.

Se non si specifica uno stile, lo stile predefinito è `LBS_NOTIFY | WS_BORDER` .

</dd> </dl>

Per altre informazioni sulla sintassi generale di un'istruzione di controllo, vedere [Parametri di controllo comuni](common-control-parameters.md).

## <a name="examples"></a>Esempio

Questo esempio definisce un controllo casella di riepilogo il cui identificatore è 101:

``` syntax
LISTBOX 101, 10, 10, 100, 100
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Combobox**](combobox-control.md)
</dt> <dt>

[Caselle di riepilogo](../controls/about-list-boxes.md)
</dt> </dl>

 

 