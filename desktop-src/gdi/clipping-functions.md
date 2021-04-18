---
description: Le funzioni seguenti vengono utilizzate con il ritaglio.
ms.assetid: de9e5786-63d8-47be-8522-e96d7c0f8634
title: Funzioni di ritaglio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bf202d5ba102095c6bfddb3c3928cab1e55a230
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978767"
---
# <a name="clipping-functions"></a>Funzioni di ritaglio

Le funzioni seguenti vengono utilizzate con il ritaglio.



| Funzione                                       | Descrizione                                                                                                                                                                               |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ExcludeClipRect**](/windows/desktop/api/Wingdi/nf-wingdi-excludecliprect)     | Crea una nuova area di visualizzazione costituita dall'area di ridimensionamento esistente meno il rettangolo specificato.                                                                                |
| [**ExtSelectClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-extselectcliprgn)   | Combina l'area specificata con l'area di visualizzazione corrente usando la modalità specificata.                                                                                                  |
| [**GetClipBox**](/windows/desktop/api/Wingdi/nf-wingdi-getclipbox)               | Recupera le dimensioni del rettangolo di delimitazione più stretto che può essere tracciato intorno all'area visibile corrente nel dispositivo.                                                              |
| [**GetClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-getcliprgn)               | Recupera un handle che identifica l'area di ritaglio definita dall'applicazione corrente per il contesto di dispositivo specificato.                                                                          |
| [**GetMetaRgn**](/windows/desktop/api/Wingdi/nf-wingdi-getmetargn)               | Recupera la metaarea corrente per il contesto di dispositivo specificato.                                                                                                                        |
| [**GetRandomRgn**](/windows/desktop/api/Wingdi/nf-wingdi-getrandomrgn)           | Copia l'area di ritaglio del sistema di un contesto di dispositivo specificato in un'area specifica.                                                                                                     |
| [**IntersectClipRect**](/windows/desktop/api/Wingdi/nf-wingdi-intersectcliprect) | Crea una nuova area di ridimensionamento dall'intersezione tra l'area di ritaglio corrente e il rettangolo specificato.                                                                           |
| [**OffsetClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-offsetcliprgn)         | Sposta l'area di visualizzazione di un contesto di dispositivo in base agli offset specificati.                                                                                                                   |
| [**PtVisible**](/windows/desktop/api/Wingdi/nf-wingdi-ptvisible)                 | Determina se il punto specificato si trova all'interno dell'area di visualizzazione di un contesto di dispositivo.                                                                                                 |
| [**RectVisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible)             | Determina se una parte del rettangolo specificato si trova all'interno dell'area di visualizzazione di un contesto di dispositivo.                                                                               |
| [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath)       | Seleziona il percorso corrente come area di ridimensionamento per un contesto di dispositivo, combinando la nuova regione con qualsiasi area di ritaglio esistente usando la modalità specificata.                               |
| [**SelectClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-selectcliprgn)         | Seleziona un'area come area di ritaglio corrente per il contesto di dispositivo specificato.                                                                                                         |
| [**SetMetaRgn**](/windows/desktop/api/Wingdi/nf-wingdi-setmetargn)               | Interseca l'area di ritaglio corrente per il contesto di dispositivo specificato con la metaarea corrente e salva l'area combinata come nuova metaarea per il contesto di dispositivo specificato. |



 

 

 



