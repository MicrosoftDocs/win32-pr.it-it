---
description: Per definire un rettangolo, un'applicazione deve usare una struttura RECT.
ms.assetid: 93c63dcb-6c8e-4c8b-aa19-6f8952d75e2e
title: Coordinate rettangolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb8a3fbc3f42c6d69a3d0eac6555b85fbfc1eecb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993901"
---
# <a name="rectangle-coordinates"></a>Coordinate rettangolo

Per definire un rettangolo, un'applicazione deve usare una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) . La struttura specifica le coordinate di due punti: gli angoli superiore sinistro e inferiore destro del rettangolo. I lati del rettangolo si estendono da questi due punti e sono paralleli all'asse x e all'asse y.

I valori delle coordinate per un rettangolo sono espressi come interi con segno. Il valore della coordinata del lato destro di un rettangolo deve essere maggiore di quello del lato sinistro. Analogamente, il valore della coordinata della parte inferiore deve essere maggiore di quello della parte superiore.

Poiché le applicazioni possono utilizzare rettangoli per molti scopi diversi, le funzioni Rectangle non utilizzano un'unità di misura esplicita. Al contrario, tutte le coordinate e le dimensioni del rettangolo vengono specificate nei valori logici firmati. La modalità di mapping e la funzione in cui viene utilizzato il rettangolo determinano le unità di misura. Per ulteriori informazioni sulle coordinate e sulle modalità di mapping, vedere [Coordinate spaces and Transformations](coordinate-spaces-and-transformations.md).

 

 
