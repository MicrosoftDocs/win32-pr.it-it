---
description: Compilazione di topologie tramite TopoEdit
ms.assetid: 04173f3d-3722-48ee-a6fb-9cdb2a897a33
title: Compilazione di topologie tramite TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88e678e0c25cbfe56c2633091820468a6c0313663847870a4de5c912a5edae95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959437"
---
# <a name="building-topologies-by-using-topoedit"></a>Compilazione di topologie tramite TopoEdit

Una topologia deve avere i tre nodi seguenti:

-   Nodo di origine: i flussi da un file multimediale, che vengono usati come origine per la topologia.
-   Nodo di trasformazione: Media Foundation trasformazione (MFT). Questi nodi sono in genere codificatori, decodificatori ed effetti per la topologia.
-   Nodo di output: sink di flusso che passa i dati multimediali, i fotogrammi video o i flussi audio alla sessione multimediale per la riproduzione.

Per informazioni sulla struttura della topologia, vedere [Informazioni sulle topologie.](about-topologies.md)

Per creare una topologia, è necessario aggiungere i nodi, connettersi ai nodi e risolvere la topologia in modo che possa essere riprodotta.

I nodi della topologia vengono visualizzati come caselle, con il testo che mostra il nome del nodo. Le caselle verdi rappresentano i nodi aggiunti dall'utente. Quando una topologia viene risolta, TopoEdit può aggiungere automaticamente nodi di trasformazione alla topologia. Queste vengono visualizzate come caselle blu nel **riquadro Topologia**.

Gli input e gli output della topologia sono rappresentati da come quadrati neri lungo il bordo del nodo. *L'input* del nodo viene visualizzato sul lato sinistro del nodo e *l'output* del nodo si trova sul lato destro del nodo.

I nodi della topologia  sono connessi tramite una connessione di nodo che viene visualizzata come una linea nera che connette l'input del nodo di un nodo all'output del nodo di un altro nodo.

La figura seguente mostra una topologia connessa per un'origine audio.

![illustrazione che mostra le connessioni dal nodo di origine a due nodi di trasformazione e quindi al nodo di output](images/e94b4cce-aa8a-497f-94c2-cc9dace17291.gif)

Questa sezione contiene i seguenti argomenti:



| Argomento                                                                                          | Descrizione                                                    |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Aggiunta di nodi di origine con TopoEdit](adding-source-nodes-with-topoedit.md)                     | Viene descritto il processo di aggiunta di nodi di origine a una topologia.    |
| [Aggiunta di nodi di trasformazione con TopoEdit](adding-transform-nodes-with-topoedit.md)               | Viene descritto il processo di aggiunta di nodi di trasformazione a una topologia. |
| [Aggiunta di nodi di output con TopoEdit](adding-output-nodes-with-topoedit.md)                     | Viene descritto il processo di aggiunta di nodi di output a una topologia.    |
| [Connessione e disconnessione di nodi della topologia](connecting-and-disconnecting-topology-nodes.md) | Viene descritto il processo di connessione di due nodi.                 |
| [Risoluzione di una topologia con TopoEdit](resolving-a-topology-with-topoedit.md)                   | Viene descritto il processo di risoluzione della topologia.                  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 



