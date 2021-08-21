---
title: Uso di rettangoli (Windows Media Player SDK)
description: Uso di rettangoli
ms.assetid: b3fc16b4-dc93-43c0-a97d-5234e36437c8
keywords:
- visualizzazioni, rettangoli
- visualizzazioni personalizzate, rettangoli
- visualizzazioni, funzione Render
- visualizzazioni personalizzate, funzione Render
- Funzione di rendering, rettangoli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79dd46928ccf8f8a0a465fa71fbb6b1bc1b4f48cbdb5c37b4b93ffd21c78c6b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118117296"
---
# <a name="using-rectangles-windows-media-player-sdk"></a>Uso di rettangoli (Windows Media Player SDK)

I rettangoli vengono usati per specificare aree rettangolari in Microsoft Windows. È possibile creare molti rettangoli nella finestra, ma Windows Media Player i valori di un rettangolo tramite la [funzione IWMPEffects::Render.](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-render) Se il rendering del plug-in viene eseguito usando una finestra, il rettangolo è l'area client della finestra. Questo viene chiamato rettangolo prc e definisce il rettangolo in cui Windows Media Player la visualizzazione. Usare spesso questa opzione per assicurarsi di non disegnare oltre gli extent del rettangolo fornito da Windows Media Player.

Un rettangolo ha quattro valori che lo definiscono. Sono a sinistra, in alto, a destra e in basso. L'angolo superiore sinistro del rettangolo è definito da sinistra e dall'angolo superiore e l'angolo inferiore destro del rettangolo è definito dal lato inferiore e destro.

Usare il codice seguente per ottenere gli extent del rettangolo di disegno. È necessario eseguire questa operazione perché l'utente può ridimensionare la finestra e si vuole essere certi di disegnare sempre in un'area che l'utente può visualizzare.


```C++
int leftside = prc->left;
int rightside = prc->right;
int topside = prc->top;
int bottomside = prc->bottom;

```



Ad esempio, per disegnare da sinistra a destra, nella parte superiore della finestra, usare codice simile al seguente:


```C++
::MoveToEx( hdc, prc->left, prc->top, NULL );  
::LineTo(hdc, prc->right, prc->top);

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Implementazione del rendering**](implementing-render.md)
</dt> </dl>

 

 




