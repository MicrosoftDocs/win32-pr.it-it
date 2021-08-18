---
title: Controllo EDITTEXT
description: Definisce un controllo di modifica appartenente alla classe EDIT.
ms.assetid: 9dc4be90-9503-4c97-813d-db246869ba3c
keywords:
- Menu e altre risorse del controllo EDITTEXT
topic_type:
- apiref
api_name:
- EDITTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b287f01b89aaa3e378309e8f98f777acc475bcca962557305021aaf471926ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847391"
---
# <a name="edittext-control"></a>Controllo EDITTEXT

Definisce un controllo di modifica appartenente alla classe EDIT. Crea un'area rettangolare in cui l'utente può digitare e modificare il testo. Il controllo visualizza un cursore quando l'utente fa clic sul mouse. L'utente può quindi usare la tastiera per immettere testo o modificare il testo esistente. Le chiavi di modifica includono le chiavi BACKSPACE e DELETE. L'utente può anche usare il mouse per selezionare i caratteri da eliminare o per selezionare la posizione in cui inserire i nuovi caratteri.

``` syntax
EDITTEXT id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Stile*
</dt> <dd>

Stili dei controlli. Questo valore può essere una combinazione degli stili della classe di modifica e degli stili seguenti: **WS \_ TABSTOP,** **WS \_ GROUP,** **WS \_ VSCROLL, WS** **\_ HSCROLL** e **WS \_ DISABLED.**

Se non si specifica uno stile, lo stile predefinito è `ES_LEFT | WS_BORDER | WS_TABSTOP` .

</dd> </dl>

Per altre informazioni sulla sintassi generale di un'istruzione di controllo, vedere [Parametri di controllo comuni](common-control-parameters.md).

## <a name="examples"></a>Esempio

L'esempio seguente illustra l'uso **dell'istruzione EDITTEXT:**

``` syntax
EDITTEXT  3, 10, 10, 100, 10
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modificare i controlli](../controls/about-edit-controls.md)
</dt> </dl>

 

 