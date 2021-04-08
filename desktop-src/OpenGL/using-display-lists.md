---
title: Uso degli elenchi di visualizzazione
description: Uso degli elenchi di visualizzazione
ms.assetid: f5edff21-0928-4ec9-9718-5189bf8ce2d7
keywords:
- OpenGL, elenchi di visualizzazione
- visualizzazione degli elenchi OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 793ec78af0b19ac437e44f16e13b93db6eab32a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855817"
---
# <a name="using-display-lists"></a>Uso degli elenchi di visualizzazione

Un elenco di visualizzazione è un gruppo di funzioni OpenGL che è stato archiviato per l'esecuzione successiva. La funzione [**glNewList**](glnewlist.md) inizia la creazione di un elenco di visualizzazione e [**glEndList**](glendlist.md) lo termina. Con poche eccezioni, le funzioni OpenGL chiamate tra **glNewList** e **glEndList** vengono aggiunte all'elenco di visualizzazione. Per un elenco delle funzioni che non è possibile archiviare ed eseguire dall'interno di un elenco di visualizzazione, vedere **glNewList** . Per attivare l'esecuzione di un elenco o di un set di elenchi, utilizzare [**glCallList**](glcalllist.md) o [**glCallLists**](glcalllists.md) e specificare il numero di identificazione di un elenco o di elenchi specifici. È possibile gestire gli indici usati per identificare gli elenchi di visualizzazione con [**glGenLists**](glgenlists.md), [**glListBase**](gllistbase.md)e l' [**elenco a pagina.**](glislist.md) Per eliminare un set di elenchi di visualizzazione, usare [**glDeleteLists**](gldeletelists.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimenti a elenchi di visualizzazione](display-lists-reference.md)
</dt> </dl>

 

 




