---
title: Controllo EDITTEXT
description: Definisce un controllo di modifica appartenente alla classe di modifica.
ms.assetid: 9dc4be90-9503-4c97-813d-db246869ba3c
keywords:
- Menu di controllo di EDITTEXT e altre risorse
topic_type:
- apiref
api_name:
- EDITTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 511cff6791703b30ec975625e0cd5cb044f4f492
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725879"
---
# <a name="edittext-control"></a>Controllo EDITTEXT

Definisce un controllo di modifica appartenente alla classe di modifica. Viene creata un'area rettangolare in cui l'utente può digitare e modificare il testo. Il controllo Visualizza un cursore quando l'utente fa clic sul mouse. L'utente può quindi utilizzare la tastiera per immettere testo o modificare il testo esistente. La modifica delle chiavi include le chiavi backspace ed DELETE. L'utente può inoltre utilizzare il mouse per selezionare i caratteri da eliminare o per selezionare la posizione in cui inserire nuovi caratteri.

``` syntax
EDITTEXT id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*stile*
</dt> <dd>

Stili del controllo. Questo valore può essere una combinazione degli stili della classe Edit e degli stili seguenti: **WS \_ TABSTOP**, **WS \_ Group**, **WS \_ VSCROLL**, **WS \_ HSCROLL** e **WS \_ disabled**.

Se non si specifica uno stile, lo stile predefinito è `ES_LEFT | WS_BORDER | WS_TABSTOP` .

</dd> </dl>

Per ulteriori informazioni sulla sintassi generale di un'istruzione di controllo, vedere [parametri di controllo comuni](common-control-parameters.md).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato l'utilizzo dell'istruzione **EDITTEXT** :

``` syntax
EDITTEXT  3, 10, 10, 100, 10
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Controlli di modifica](../controls/about-edit-controls.md)
</dt> </dl>

 

 