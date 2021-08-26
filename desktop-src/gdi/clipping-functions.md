---
description: Le funzioni seguenti vengono usate con il ritaglio.
ms.assetid: de9e5786-63d8-47be-8522-e96d7c0f8634
title: Funzioni di ritaglio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c7e3ec1c57713a87e5367ed28427caaab663e0bcd1abfe83c4040e04a7e6d75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120115331"
---
# <a name="clipping-functions"></a>Funzioni di ritaglio

Le funzioni seguenti vengono usate con il ritaglio.



| Funzione                                       | Descrizione                                                                                                                                                                               |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ExcludeClipRect**](/windows/desktop/api/Wingdi/nf-wingdi-excludecliprect)     | Crea una nuova area di ritaglio costituita dall'area di ritaglio esistente meno il rettangolo specificato.                                                                                |
| [**ExtSelectClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-extselectcliprgn)   | Combina l'area specificata con l'area di ritaglio corrente usando la modalità specificata.                                                                                                  |
| [**GetClipBox**](/windows/desktop/api/Wingdi/nf-wingdi-getclipbox)               | Recupera le dimensioni del rettangolo di delimitazione più stretto che può essere disegnato intorno all'area visibile corrente del dispositivo.                                                              |
| [**GetClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-getcliprgn)               | Recupera un handle che identifica l'area di ritaglio definita dall'applicazione corrente per il contesto di dispositivo specificato.                                                                          |
| [**GetMetaRgn**](/windows/desktop/api/Wingdi/nf-wingdi-getmetargn)               | Recupera la metaarea corrente per il contesto di dispositivo specificato.                                                                                                                        |
| [**GetRandomRgn**](/windows/desktop/api/Wingdi/nf-wingdi-getrandomrgn)           | Copia l'area di ritaglio di sistema di un contesto di dispositivo specificato in un'area specifica.                                                                                                     |
| [**IntersectClipRect**](/windows/desktop/api/Wingdi/nf-wingdi-intersectcliprect) | Crea una nuova area di ritaglio dall'intersezione tra l'area di ritaglio corrente e il rettangolo specificato.                                                                           |
| [**OffsetClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-offsetcliprgn)         | Sposta l'area di ritaglio di un contesto di dispositivo in base a offset specificati.                                                                                                                   |
| [**PtVisible**](/windows/desktop/api/Wingdi/nf-wingdi-ptvisible)                 | Determina se il punto specificato si trova all'interno dell'area di ritaglio di un contesto di dispositivo.                                                                                                 |
| [**RectVisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible)             | Determina se una parte del rettangolo specificato si trova all'interno dell'area di ritaglio di un contesto di dispositivo.                                                                               |
| [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath)       | Seleziona il tracciato corrente come area di ritaglio per un contesto di dispositivo, combinando la nuova area con qualsiasi area di ritaglio esistente usando la modalità specificata.                               |
| [**SelectClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-selectcliprgn)         | Seleziona un'area come area di ritaglio corrente per il contesto di dispositivo specificato.                                                                                                         |
| [**SetMetaRgn**](/windows/desktop/api/Wingdi/nf-wingdi-setmetargn)               | Interseca l'area di ritaglio corrente per il contesto di dispositivo specificato con la metaarea corrente e salva l'area combinata come nuova metaarea per il contesto di dispositivo specificato. |



 

 

 



