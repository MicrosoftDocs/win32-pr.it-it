---
description: L'ombreggiatura smussata è un metodo di ombreggiatura di un'area con una sfumatura di colore.
ms.assetid: 94f26d15-fb76-47ec-b805-f04975d41b43
title: Ombreggiatura smussata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd5bfa54fef8d0a6810a3230e88e4e3144f7ecf4b62f7313f5daf4213e948c00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965201"
---
# <a name="smooth-shading"></a>Ombreggiatura smussata

*L'ombreggiatura smussata* è un metodo di ombreggiatura di un'area con una sfumatura di colore. L'inclusione delle informazioni sul colore, insieme ai limiti della primitiva di disegno, specifica la sfumatura di colore. GDI interpola in modo lineare il colore dell'oggetto all'interno della primitiva passata sugli endpoint del colore. Le informazioni sul colore e sui vertici sono incluse nelle informazioni sulla posizione nella [**struttura TRIVERTEX.**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex)

Usare la [**funzione GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill) per riempire una struttura triangolare o rettangolare. Per riempire un triangolo con ombreggiatura uniforme, chiama **GradientFill** con i tre endpoint del triangolo. Per riempire un rettangolo con ombreggiatura smussata, chiama **GradientFill** con le coordinate del rettangolo in alto a sinistra e in basso a destra. **GradientFill** fa riferimento [**alle strutture TRIVERTEX,**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex) [**GRADIENT \_ RECT**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect)e [**GRADIENT \_ TRIANGLE.**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_triangle)

Per un esempio, vedere [Disegno di un triangolo ombreggiato.](drawing-a-shaded-triangle.md)

 

 



