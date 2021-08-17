---
title: Porting degli elenchi di visualizzazione
description: L'implementazione OpenGL degli elenchi di visualizzazione è simile all'implementazione di IRIS GL, con due eccezioni in OpenGL che non è possibile modificare gli elenchi di visualizzazione dopo averli creati e non è possibile chiamare funzioni dall'interno degli elenchi di visualizzazione.
ms.assetid: 617e19ff-6a55-4f7c-b229-075cdee8f1cf
keywords:
- Portabilità IRIS GL, visualizzazione elenchi
- porting from IRIS GL,display lists
- porting to OpenGL from IRIS GL,display lists
- Portabilità OpenGL da IRIS GL, visualizzazione di elenchi
- visualizzare elenchi, porting da IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 858f1f3be180b3ef09c81bb8d61b18705fc9485742d7384562eecff142f4bfb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117980803"
---
# <a name="porting-display-lists"></a>Porting degli elenchi di visualizzazione

L'implementazione OpenGL degli elenchi di visualizzazione è simile all'implementazione di IRIS GL, con due eccezioni: in OpenGL non è possibile modificare gli elenchi di visualizzazione dopo averli creati e non è possibile chiamare funzioni dall'interno degli elenchi di visualizzazione.

Poiché non è possibile modificare o chiamare funzioni dall'interno degli elenchi di visualizzazione, queste funzioni IRIS GL non hanno equivalenti in OpenGL:

-   **editobj**
-   **objdelete**, **objinsert** e **objreplace**
-   **maketag**, **gentag**, **istag** e **deltag**
-   **callfunc**

In IRIS GL si usano le funzioni **makeobj** e **closeobj** per creare elenchi di visualizzazione. In OpenGL si usano [**glNewList**](glnewlist.md) e [**glEndList**](glendlist.md).

La tabella seguente elenca le funzioni dell'elenco di visualizzazione IRIS GL con le funzioni OpenGL equivalenti.



| Funzione GL IRIS | Funzione OpenGL                                                      | Significato                                                       |
|------------------|----------------------------------------------------------------------|---------------------------------------------------------------|
| **makeobj**      | **glNewList**                                                        | Crea un nuovo elenco di visualizzazione.                                   |
| **closeobj**     | **glEndList**                                                        | Segnala la fine dell'elenco di visualizzazione.                                  |
| **callobj**      | [**glCallList**](glcalllist.md), [ **glCallLists**](glcalllists.md) | Esegue l'elenco o gli elenchi visualizzati.                               |
| **isobj**        | [**glIsList**](glislist.md)                                         | Verifica l'esistenza dell'elenco di visualizzazione.                             |
| **Delobj**       | [**glDeleteLists**](gldeletelists.md)                               | Elimina un gruppo contiguo di elenchi di visualizzazione.                    |
| **genobj**       | [**glGenLists**](glgenlists.md)                                     | Genera il numero specificato di elenchi di visualizzazione vuoti contigui. |



 

Questo argomento include informazioni sugli argomenti seguenti.

-   [Porting della funzione bbox2](porting-the-bbox2-function.md)
-   [Porting degli elenchi visualizzati modificati](porting-edited-display-lists.md)
-   [Porta di esempio di un elenco di visualizzazione](a-sample-port-of-a-display-list.md)

 

 




