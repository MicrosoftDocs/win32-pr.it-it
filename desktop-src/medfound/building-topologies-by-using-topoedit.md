---
description: Compilazione di topologie tramite TopoEdit
ms.assetid: 04173f3d-3722-48ee-a6fb-9cdb2a897a33
title: Compilazione di topologie tramite TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92758911113c7500cb13fa814d07321435fafeb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127999"
---
# <a name="building-topologies-by-using-topoedit"></a>Compilazione di topologie tramite TopoEdit

Una topologia deve disporre dei tre nodi seguenti:

-   Nodo di origine: flussi da un file multimediale, usati come origine per la topologia.
-   Nodo Transform: una trasformazione Media Foundation (MFT). Questi nodi sono in genere codificatori, decodificatori ed effetti per la topologia.
-   Nodo di output: sink del flusso che passa i dati multimediali, i fotogrammi video o i flussi audio alla sessione multimediale per la riproduzione.

Per informazioni sulla struttura della topologia, vedere [informazioni sulle topologie](about-topologies.md).

Per compilare una topologia, è necessario aggiungere i nodi, connettere i nodi e risolvere la topologia in modo che sia possibile riprodurli.

I nodi della topologia vengono visualizzati come caselle, con testo che mostra il nome del nodo. Le caselle verdi rappresentano i nodi aggiunti dall'utente. Quando viene risolta una topologia, TopoEdit può aggiungere nodi Transform alla topologia automaticamente. Questi vengono visualizzati come caselle blu nel **riquadro topologia**.

Gli input e gli output della topologia sono rappresentati da quadratini neri lungo il bordo del nodo. L' *input del nodo* viene visualizzato sul lato sinistro del nodo e l'output del *nodo* si trova sul lato destro del nodo.

I nodi della topologia sono connessi tramite una *connessione al nodo* visualizzata come una linea nera che connette l'input del nodo di un nodo all'output del nodo di un altro nodo.

Nella figura seguente viene illustrata una topologia connessa per un'origine audio.

![illustrazione che mostra le connessioni dal nodo di origine a due nodi di trasformazione, quindi al nodo di output](images/e94b4cce-aa8a-497f-94c2-cc9dace17291.gif)

Questa sezione contiene i seguenti argomenti:



| Argomento                                                                                          | Descrizione                                                    |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Aggiunta di nodi di origine con TopoEdit](adding-source-nodes-with-topoedit.md)                     | Viene descritto il processo di aggiunta di nodi di origine a una topologia.    |
| [Aggiunta di nodi Transform con TopoEdit](adding-transform-nodes-with-topoedit.md)               | Viene descritto il processo di aggiunta di nodi Transform a una topologia. |
| [Aggiunta di nodi di output con TopoEdit](adding-output-nodes-with-topoedit.md)                     | Viene descritto il processo di aggiunta di nodi di output a una topologia.    |
| [Connessione e disconnessione di nodi della topologia](connecting-and-disconnecting-topology-nodes.md) | Descrive il processo di connessione di due nodi.                 |
| [Risoluzione di una topologia con TopoEdit](resolving-a-topology-with-topoedit.md)                   | Descrive il processo di risoluzione della topologia.                  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 



