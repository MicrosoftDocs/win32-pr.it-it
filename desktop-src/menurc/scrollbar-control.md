---
title: SCROLLBAR (controllo)
description: Definisce un controllo barra di scorrimento.
ms.assetid: 9b0b60b1-4b4b-494e-90d0-aaa67e7ea88c
keywords:
- Menu di controllo SCROLLBAR e altre risorse
topic_type:
- apiref
api_name:
- SCROLLBAR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44ef4069988603c7c89ec2ed8a363d3515a0b8bb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117746"
---
# <a name="scrollbar-control"></a>SCROLLBAR (controllo)

Definisce un controllo barra di scorrimento. Il controllo è un rettangolo che contiene una casella di scorrimento e con frecce di direzione a entrambe le estremità. Il controllo barra di scorrimento invia un messaggio di notifica all'elemento padre ogni volta che l'utente fa clic sul mouse nel controllo. L'elemento padre è responsabile dell'aggiornamento della posizione della casella di scorrimento. I controlli barra di scorrimento possono essere posizionati in qualsiasi punto di una finestra e usati quando necessario per fornire input di scorrimento.

``` syntax
SCROLLBAR id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*stile*
</dt> <dd>

Zero o una combinazione degli stili seguenti: **WS \_ TABSTOP**, **WS \_ Group** e **WS \_ disabled**.

Oltre a questi stili, il parametro di *stile* può contenere una combinazione (o nessuno) degli stili della classe ScrollBar.

Se non si specifica uno stile, lo stile predefinito è **SBS \_ orizzontalmente**.

</dd> </dl>

Per ulteriori informazioni sulla sintassi generale di un'istruzione di controllo, vedere [parametri di controllo comuni](common-control-parameters.md). Si noti che non è possibile specificare il testo per questo controllo.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato l'utilizzo dell'istruzione **ScrollBar** :

``` syntax
#define IDC_SCROLLBARV                  1010

SCROLLBAR IDC_SCROLLBARV, 7, 55, 187, 44, SBS_VERT
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Barre di scorrimento](../controls/about-scroll-bars.md)
</dt> </dl>

 

 