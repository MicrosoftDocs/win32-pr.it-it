---
title: Ritaglio (OpenGL)
description: Il ritaglio si verifica in due passaggi
ms.assetid: f6f60135-f43b-4595-bfd3-33e750413e70
keywords:
- Pipeline di elaborazione OpenGL, ritaglio
- ritaglio di OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08aa35458e7e0a137759fe22be95f4b399b4d56b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400131"
---
# <a name="clipping-opengl"></a>Ritaglio (OpenGL)

Il ritaglio si verifica in due passaggi:

1.  **Visualizza il ritaglio specifico del volume clippingApplication.** Subito dopo aver assemblato le primitive, queste vengono ritagliate in coordinate oculari in base alle esigenze per tutti i piani di ritaglio definiti con [**glClipPlane**](glclipplane.md). OpenGL richiede il supporto per almeno sei piani di ritaglio specifici dell'applicazione.
2.  Le primitive vengono trasformate dalla matrice di proiezione in coordinate di ritaglio e ritagliate dal volume di visualizzazione corrispondente. Questa matrice può essere controllata dalle funzioni di trasformazione della matrice (vedere [trasformazioni matrici](matrix-transformations.md)), ma in genere è specificata da [**glFrustum**](glfrustum.md) o [**glOrtho**](glortho.md).

Punti, segmenti di linea e poligoni vengono gestiti in modo diverso durante il ritaglio:

-   I punti vengono conservati nello stato originale (se sono all'interno del volume di ritaglio) o rimossi (se sono all'esterno del volume di ritaglio).
-   Se parti di poligoni o segmenti di linea sono all'esterno del volume di ritaglio, i nuovi vertici vengono generati nei punti di clip.
-   Per i poligoni, può essere necessario costruire un bordo intero tra i nuovi vertici generati nei punti di ritaglio.
-   Per i segmenti di linea e i poligoni che vengono ritagliati, le informazioni relative al flag, al colore e alla trama del bordo vengono assegnate a tutti i nuovi vertici.

 

 




