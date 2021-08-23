---
title: Ritaglio (OpenGL)
description: Il ritaglio avviene in due passaggi
ms.assetid: f6f60135-f43b-4595-bfd3-33e750413e70
keywords:
- pipeline di elaborazione OpenGL, ritaglio
- ritaglio di OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb518b9208b73dad2071531f6a30cdff6cab2ec5dcbe937fa3e66fea8bb0a8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119289041"
---
# <a name="clipping-opengl"></a>Ritaglio (OpenGL)

Il ritaglio avviene in due passaggi:

1.  **Visualizzare il ritaglio del volume Ritaglio specifico dell'applicazione.** Subito dopo l'assemblaggio, le primitive vengono ritagliate in coordinate oculare in base alle esigenze per i piani di ritaglio definiti con [**glClipPlane.**](glclipplane.md) OpenGL richiede il supporto per almeno sei piani di ritaglio specifici dell'applicazione.
2.  Le primitive vengono trasformate dalla matrice di proiezione in coordinate di ritaglio e ritagliate in base al volume di visualizzazione corrispondente. Questa matrice può essere controllata dalle funzioni di trasformazione della matrice (vedere [Matrix Transformations](matrix-transformations.md)) ma viene in genere specificata da [**glFrustum**](glfrustum.md) o [**glOrtho.**](glortho.md)

I punti, i segmenti di linea e i poligoni vengono gestiti in modo diverso durante il ritaglio:

-   I punti vengono mantenuti nello stato originale (se si trova all'interno del volume di clip) o eliminati (se si trova all'esterno del volume di clip).
-   Se parti di segmenti di linea o poligoni si trova all'esterno del volume della clip, vengono generati nuovi vertici in corrispondenza dei punti di ritaglio.
-   Per i poligoni, potrebbe essere necessario costruire un intero bordo tra i nuovi vertici generati in corrispondenza dei punti di ritaglio.
-   Per i segmenti di linea e i poligoni ritagliati, le informazioni relative a flag, colore e trama vengono assegnate a tutti i nuovi vertici.

 

 




