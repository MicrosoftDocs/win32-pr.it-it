---
title: Uso degli elenchi di visualizzazione
description: Uso degli elenchi di visualizzazione
ms.assetid: f5edff21-0928-4ec9-9718-5189bf8ce2d7
keywords:
- OpenGL, visualizzare elenchi
- elenchi di visualizzazione OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 322721868f3bf994382a7604aa2cb76802f268aec7a1298aaa14e3066d5f6cce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932801"
---
# <a name="using-display-lists"></a>Uso degli elenchi di visualizzazione

Un elenco di visualizzazione è un gruppo di funzioni OpenGL archiviate per l'esecuzione successiva. La [**funzione glNewList**](glnewlist.md) inizia la creazione di un elenco di visualizzazione e [**glEndList lo**](glendlist.md) termina. Con poche eccezioni, le funzioni OpenGL chiamate tra **glNewList** e **glEndList** vengono aggiunte all'elenco di visualizzazione. Vedere **glNewList per** un elenco delle funzioni che non è possibile archiviare ed eseguire dall'interno di un elenco di visualizzazione. Per attivare l'esecuzione di un elenco o di un set di elenchi, usare [**glCallList**](glcalllist.md) o [**glCallLists**](glcalllists.md) e specificare il numero di identificazione di uno o più elenchi specifici. È possibile gestire gli indici usati per identificare gli elenchi visualizzati con [**glGenLists**](glgenlists.md), [**glListBase**](gllistbase.md)e [**glIsList**](glislist.md). Per eliminare un set di elenchi visualizzati, usare [**glDeleteLists.**](gldeletelists.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento per gli elenchi di visualizzazione](display-lists-reference.md)
</dt> </dl>

 

 




