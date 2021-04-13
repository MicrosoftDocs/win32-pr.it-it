---
title: Porting degli elenchi di visualizzazione
description: L'implementazione OpenGL degli elenchi di visualizzazione è simile all'implementazione di IRIS GL, con due eccezioni in OpenGL non è possibile modificare gli elenchi di visualizzazione una volta creati e non è possibile chiamare funzioni dall'interno degli elenchi di visualizzazione.
ms.assetid: 617e19ff-6a55-4f7c-b229-075cdee8f1cf
keywords:
- Porting di IRIS GL, elenchi di visualizzazione
- porting da IRIS GL, elenchi di visualizzazione
- porting in OpenGL da IRIS GL, elenchi di visualizzazione
- Porting OpenGL da IRIS GL, elenchi di visualizzazione
- visualizzare elenchi, porting da IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461000e6d785f0d03bbbc8f738eba60768bc5d74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328820"
---
# <a name="porting-display-lists"></a>Porting degli elenchi di visualizzazione

L'implementazione OpenGL degli elenchi di visualizzazione è simile all'implementazione di IRIS GL, con due eccezioni: in OpenGL non è possibile modificare gli elenchi di visualizzazione una volta creati e non è possibile chiamare funzioni dall'interno degli elenchi di visualizzazione.

Poiché non è possibile modificare o chiamare funzioni dall'interno degli elenchi di visualizzazione, queste funzioni di IRIS GL non hanno equivalenti in OpenGL:

-   **editobj**
-   **objdelete**, **objinsert** e **objreplace**
-   **maketag**, **Gentag**, **ISTAG** e **DeltaG**
-   **callfunc**

In IRIS GL usare le funzioni **makeobj** e **closeobj** per creare elenchi di visualizzazione. In OpenGL si usano [**glNewList**](glnewlist.md) e [**glEndList**](glendlist.md).

La tabella seguente elenca le funzioni dell'elenco di visualizzazione di IRIS GL con le funzioni OpenGL equivalenti.



| Funzione IRIS GL | OpenGL (funzione)                                                      | Significato                                                       |
|------------------|----------------------------------------------------------------------|---------------------------------------------------------------|
| **makeobj**      | **glNewList**                                                        | Crea un nuovo elenco di visualizzazione.                                   |
| **closeobj**     | **glEndList**                                                        | Segnala la fine dell'elenco di visualizzazione.                                  |
| **callobj**      | [**glCallList**](glcalllist.md), [ **glCallLists**](glcalllists.md) | Esegue l'elenco o gli elenchi di visualizzazione.                               |
| **isobj**        | [**Pagina di**](glislist.md)                                         | Verifica l'esistenza dell'elenco di visualizzazione.                             |
| **DELOBJ**       | [**glDeleteLists**](gldeletelists.md)                               | Elimina il gruppo contiguo di elenchi di visualizzazione.                    |
| **genobj**       | [**glGenLists**](glgenlists.md)                                     | Genera il numero specificato di elenchi di visualizzazione vuoti contigui. |



 

Questo argomento include informazioni sui seguenti elementi.

-   [Porting della funzione bbox2](porting-the-bbox2-function.md)
-   [Porting degli elenchi di visualizzazione modificati](porting-edited-display-lists.md)
-   [Una porta di esempio di un elenco di visualizzazione](a-sample-port-of-a-display-list.md)

 

 




