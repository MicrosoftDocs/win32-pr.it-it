---
title: Controllo DEFPUSHBUTTON
description: Definisce un controllo pulsante di comando predefinito.
ms.assetid: 17b2ffcb-0611-4d92-9108-bf27b1c07049
keywords:
- Menu di controllo di DEFPUSHBUTTON e altre risorse
topic_type:
- apiref
api_name:
- DEFPUSHBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49b958e60d812c3372ad6a6e6ed2a8d02d56c0f6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299267"
---
# <a name="defpushbutton-control"></a>Controllo DEFPUSHBUTTON

Definisce un controllo pulsante di comando predefinito. Il controllo è un rettangolo di piccole dimensioni con un contorno in grassetto che rappresenta la risposta predefinita per l'utente. Il testo specificato viene visualizzato all'interno del pulsante. Il controllo evidenzia il pulsante nel modo consueto quando l'utente fa clic sul mouse e invia un messaggio alla finestra padre.

``` syntax
DEFPUSHBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*testo*
</dt> <dd>

Testo che deve essere centrato nell'area rettangolare del controllo.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*stile*
</dt> <dd>

Stili del controllo. Questo valore può essere una combinazione degli stili seguenti: **BS \_ DEFPUSHBUTTON**, **WS \_ TABSTOP**, **WS \_ Group** e **WS \_ disabled**.

Se non si specifica uno stile, lo stile predefinito è `BS_DEFPUSHBUTTON | WS_TABSTOP` .

</dd> </dl>

Per ulteriori informazioni sulla sintassi generale di un'istruzione di controllo, vedere [parametri di controllo comuni](common-control-parameters.md).

## <a name="examples"></a>Esempio

Questo esempio definisce un controllo pulsante di comando predefinito con etichetta Annulla:

``` syntax
DEFPUSHBUTTON "Cancel", 101, 10, 10, 24, 50
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Pulsanti di push](https://www.bing.com/search?q=Push+Buttons)
</dt> <dt>

[**PULSANTE**](pushbutton-control.md)
</dt> <dt>

[**RADIOBUTTON**](radiobutton-control.md)
</dt> </dl>

 

 




