---
description: Questo argomento elenca i metodi SetClip della classe Graphics. Per un elenco completo dei metodi per la classe Graphics, vedere Graphics.
ms.assetid: e8348373-da79-4d33-8bea-d594985493d4
title: Metodi Graphics.SetClip
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 616a78aa7dd251e888bba1186a3583c5d7f62d188dcc6313560f651ec6558827
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037189"
---
# <a name="graphicssetclip-methods"></a>Metodi Graphics.SetClip

Questo argomento elenca i metodi SetClip della [**classe Graphics.**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Per un elenco completo dei metodi per la **classe Graphics,** vedere [**Graphics.**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                                     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|:-----------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetClip(HRGN,CombineMode)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inhrgn_incombinemode))                     | Il [**metodo Graphics::SetClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inhrgn_incombinemode)) aggiorna l'area di ritaglio di questo oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) in un'area che rappresenta la combinazione di se stesso e di un'area GDI.<br/>                                                                                                                                                                                                          |
| [**SetClip(Rect&,CombineMode)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstrect__incombinemode))   | Il [**metodo Graphics::SetClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstrect__incombinemode)) aggiorna l'area di ritaglio di questo oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) in un'area che rappresenta la combinazione di se stesso e di un rettangolo.<br/>                                                                                                                                                                                          |
| [**SetClip(RectF&,CombineMode)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstrectf__incombinemode)) | Il [**metodo Graphics::SetClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstrectf__incombinemode)) aggiorna l'area di ritaglio di questo oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) in un'area che rappresenta la combinazione di se stesso e di un rettangolo.<br/>                                                                                                                                                                                         |
| [**\*SetClip(Region,CombineMode)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode))               | Il [**metodo Graphics::SetClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) aggiorna l'area di ritaglio di questo oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) in un'area che rappresenta la combinazione di se stesso e dell'area specificata da un [**oggetto Region.**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region)<br/>                                                                                                                                      |
| [**SetClip(Graphics \* ,CombineMode)**](/previous-versions//ms535823(v=vs.85))                  | Il [**metodo Graphics::SetClip**](/previous-versions//ms535823(v=vs.85)) aggiorna l'area di ritaglio di questo oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) in un'area che è la combinazione di se stesso e l'area di ritaglio di un altro **oggetto Graphics.**<br/>                                                                                                                                                                       |
| [**\*SetClip(GraphicsPath,CombineMode)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstgraphicspath_incombinemode))           | Il [**metodo Graphics::SetClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstgraphicspath_incombinemode)) aggiorna l'area di ritaglio di questo oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) in un'area che rappresenta la combinazione di se stesso e dell'area specificata da un tracciato grafico. Se una figura nel percorso non è chiusa, questo metodo considera la figura non chiusa come se fosse chiusa da una linea retta che connette i punti iniziale e finale della figura.<br/> |



 

 
