---
title: Uso di rettangoli (Windows Media Player SDK)
description: Uso di rettangoli
ms.assetid: b3fc16b4-dc93-43c0-a97d-5234e36437c8
keywords:
- Visualizzazioni, rettangoli
- Visualizzazioni personalizzate, rettangoli
- Visualizzazioni, funzione render
- Visualizzazioni personalizzate, funzione render
- Funzione render, rettangoli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b48f16888d8e71c052d216a838683f2b7127e75
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300870"
---
# <a name="using-rectangles-windows-media-player-sdk"></a>Uso di rettangoli (Windows Media Player SDK)

I rettangoli vengono utilizzati per specificare le aree rettangolari in Microsoft Windows. È possibile creare molti rettangoli nella finestra, ma Windows Media Player fornisce i valori di un rettangolo tramite la funzione [IWMPEffects:: Render](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-render) . Se il plug-in viene eseguito tramite una finestra, il rettangolo è l'area client della finestra. Questa operazione viene definita rettangolo PRC e definisce il rettangolo in cui verrà visualizzata la visualizzazione di Windows Media Player. Utilizzare questa frequenza per assicurarsi che non venga disegnato oltre gli extent del rettangolo fornito da Windows Media Player.

Un rettangolo ha quattro valori che lo definiscono. Sono a sinistra, in alto, a destra e in basso. L'angolo superiore sinistro del rettangolo viene definito da Left e top, mentre l'angolo inferiore destro del rettangolo viene definito in basso e a destra.

Usare il codice seguente per ottenere gli extent del rettangolo di disegno. È necessario eseguire questa operazione perché l'utente può ridimensionare la finestra e si vuole essere certi che il disegno venga sempre visualizzato in un'area che può essere visualizzata dall'utente.


```C++
int leftside = prc->left;
int rightside = prc->right;
int topside = prc->top;
int bottomside = prc->bottom;

```



Per creare, ad esempio, da sinistra a destra, nella parte superiore della finestra, usare codice simile al seguente:


```C++
::MoveToEx( hdc, prc->left, prc->top, NULL );  
::LineTo(hdc, prc->right, prc->top);

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Implementazione di rendering**](implementing-render.md)
</dt> </dl>

 

 




