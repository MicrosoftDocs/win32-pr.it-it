---
title: Controllo DEFPUSHBUTTON
description: Definisce un controllo pulsante di comando predefinito.
ms.assetid: 17b2ffcb-0611-4d92-9108-bf27b1c07049
keywords:
- Menu e altre risorse del controllo DEFPUSHBUTTON
topic_type:
- apiref
api_name:
- DEFPUSHBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abde79167128be133d865dcd5c73cd1d6d125172ea83f7b47930ed5aafbacbb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117687865"
---
# <a name="defpushbutton-control"></a>Controllo DEFPUSHBUTTON

Definisce un controllo pulsante di comando predefinito. Il controllo è un piccolo rettangolo con un contorno in grassetto che rappresenta la risposta predefinita per l'utente. Il testo specificato viene visualizzato all'interno del pulsante. Il controllo evidenzia il pulsante nel modo consueto quando l'utente fa clic con il mouse su di esso e invia un messaggio alla finestra padre.

``` syntax
DEFPUSHBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*Testo*
</dt> <dd>

Testo da centrare nell'area rettangolare del controllo.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*Stile*
</dt> <dd>

Stili dei controlli. Questo valore può essere una combinazione degli stili seguenti: **BS \_ DEFPUSHBUTTON,** **WS \_ TABSTOP,** **WS \_ GROUP** e **WS \_ DISABLED.**

Se non si specifica uno stile, lo stile predefinito è `BS_DEFPUSHBUTTON | WS_TABSTOP` .

</dd> </dl>

Per altre informazioni sulla sintassi generale di un'istruzione di controllo, vedere [Parametri di controllo comuni.](common-control-parameters.md)

## <a name="examples"></a>Esempio

Questo esempio definisce un controllo pulsante di comando predefinito con etichetta Annulla:

``` syntax
DEFPUSHBUTTON "Cancel", 101, 10, 10, 24, 50
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Pulsanti](https://www.bing.com/search?q=Push+Buttons)
</dt> <dt>

[**Pulsante**](pushbutton-control.md)
</dt> <dt>

[**Radiobutton**](radiobutton-control.md)
</dt> </dl>

 

 




