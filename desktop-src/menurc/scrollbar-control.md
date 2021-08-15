---
title: Controllo SCROLLBAR
description: Definisce un controllo barra di scorrimento.
ms.assetid: 9b0b60b1-4b4b-494e-90d0-aaa67e7ea88c
keywords:
- Menu del controllo SCROLLBAR e altre risorse
topic_type:
- apiref
api_name:
- SCROLLBAR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b03865f66a06198cc1b1b78f8bb0b0213d998b7e5407506e4b8ed64ed9efaf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118733439"
---
# <a name="scrollbar-control"></a>Controllo SCROLLBAR

Definisce un controllo barra di scorrimento. Il controllo è un rettangolo che contiene una casella di scorrimento e ha frecce di direzione a entrambe le estremità. Il controllo barra di scorrimento invia un messaggio di notifica all'elemento padre ogni volta che l'utente fa clic con il mouse nel controllo. L'elemento padre è responsabile dell'aggiornamento della posizione della casella di scorrimento. I controlli barra di scorrimento possono essere posizionati in qualsiasi punto di una finestra e usati quando necessario per fornire l'input di scorrimento.

``` syntax
SCROLLBAR id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Stile*
</dt> <dd>

Zero o una combinazione degli stili seguenti: **WS \_ TABSTOP,** **WS \_ GROUP** e **WS \_ DISABLED.**

Oltre a questi stili, il *parametro style* può contenere una combinazione (o nessuno) degli stili della classe SCROLLBAR.

Se non si specifica uno stile, lo stile predefinito è **SBS \_ HORZ.**

</dd> </dl>

Per altre informazioni sulla sintassi generale di un'istruzione di controllo, vedere [Parametri di controllo comuni.](common-control-parameters.md) Si noti che non è possibile specificare testo per questo controllo.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato l'utilizzo **dell'istruzione SCROLLBAR:**

``` syntax
#define IDC_SCROLLBARV                  1010

SCROLLBAR IDC_SCROLLBARV, 7, 55, 187, 44, SBS_VERT
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Barre di scorrimento](../controls/about-scroll-bars.md)
</dt> </dl>

 

 