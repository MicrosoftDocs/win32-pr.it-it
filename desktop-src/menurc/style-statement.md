---
title: Istruzione STYLE
description: Definisce lo stile della finestra della finestra di dialogo. Lo stile della finestra specifica se la casella è un popup o una finestra figlio.
ms.assetid: 5ede57ad-5fa5-414c-9823-e66994826027
keywords:
- Menu di istruzioni di stile e altre risorse
topic_type:
- apiref
api_name:
- STYLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67cd8f6af4a6baa2f36b66855cbe9faa2b0e5120
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398964"
---
# <a name="style-statement"></a>Istruzione STYLE

Definisce lo stile della finestra della finestra di dialogo. Lo stile della finestra specifica se la casella è un popup o una finestra figlio.

``` syntax
STYLE style
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*stile*
</dt> <dd>

Stile della finestra. Questo parametro può essere un valore intero o una combinazione di valori di stile della finestra, ad esempio **WS \_ Caption** e **WS \_ SYSMENU**, e i valori di stile della finestra di dialogo (ad esempio **DS \_ Center**).

</dd> </dl>

Per un elenco degli stili della finestra, vedere [stili di finestra](/windows/desktop/winmsg/window-styles). Per un elenco degli stili della finestra di dialogo, vedere [stili di modelli](../dlgbox/about-dialog-boxes.md)di finestra di dialogo. Se si utilizzano i valori di stile della finestra o della finestra di dialogo, è necessario includere Windows. h.

 

 