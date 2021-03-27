---
description: L'ombreggiatura uniforme è un metodo di ombreggiatura di un'area con una sfumatura di colore.
ms.assetid: 94f26d15-fb76-47ec-b805-f04975d41b43
title: Ombreggiatura uniforme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5b73738c03147083099a5070e61fe21ca5cac76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232550"
---
# <a name="smooth-shading"></a>Ombreggiatura uniforme

L' *ombreggiatura uniforme* è un metodo di ombreggiatura di un'area con una sfumatura di colore. L'inclusione di informazioni sui colori, insieme ai limiti della primitiva di disegno, specifica la sfumatura di colore. GDI esegue l'interpolazione lineare del colore dell'interno della primitiva passata sugli endpoint dei colori. Le informazioni sui vertici e sui colori sono incluse con le informazioni sulla posizione nella struttura [**trivertice**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex) .

Utilizzare la funzione [**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill) per riempire un triangolo o una struttura Rectangle. Per riempire un triangolo con ombreggiatura uniforme, chiamare **GradientFill** con i tre endpoint triangolari. Per riempire un rettangolo con ombreggiatura uniforme, chiamare **GradientFill** con le coordinate del rettangolo superiore sinistro e inferiore destro. **GradientFill** fa riferimento alle strutture [**trivertice**](/windows/desktop/api/Wingdi/ns-wingdi-trivertex), rettangolo [**\_ sfumato**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_rect)e [**\_ triangolo sfumatura**](/windows/desktop/api/Wingdi/ns-wingdi-gradient_triangle) .

Per un esempio, vedere [disegno di un triangolo ombreggiato](drawing-a-shaded-triangle.md).

 

 



