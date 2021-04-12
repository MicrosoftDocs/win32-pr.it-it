---
description: Risoluzione di una topologia con TopoEdit
ms.assetid: da3e2bbc-7c9f-4a15-8842-c1bb00662cd2
title: Risoluzione di una topologia con TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8397e380b19a6f45736c06e859d2a80456aad079
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226507"
---
# <a name="resolving-a-topology-with-topoedit"></a>Risoluzione di una topologia con TopoEdit

Esistono due tipi di topologie:

-   Topologia parziale. Il nodo di origine è connesso direttamente al nodo di output. In alcuni casi, una topologia parziale può avere alcuni nodi di trasformazione intermedi, ad esempio effetti, ma non tutti. I nodi di trasformazione omessi sono in genere decodificatori o conversione di formato MFTs, ad esempio convertitori di colori e ricampionatori audio.

-   Topologia completa. Il nodo di origine è connesso al nodo di output tramite un nodo di trasformazione. Questo tipo di topologia deve avere ogni nodo per elaborare i dati.

TopoEdit può riprodurre solo topologie complete. TopoEdit utilizza l'oggetto caricatore della topologia, fornito da Media Foundation, per convertire una topologia parziale in una topologia completa inserendo le trasformazioni necessarie. Il processo di creazione di una topologia completa è denominato risoluzione di una topologia.

Per informazioni sui tipi di topologia, vedere la sezione topologie parziali in [informazioni sulle](about-topologies.md)topologie.

Prima di risolvere una topologia, verificare quanto segue:

-   La topologia contiene un nodo di origine e un nodo di output.

-   I nodi di origine e di output sono connessi tramite una connessione di nodo valida. Durante la risoluzione della topologia, il caricatore della topologia controlla il tipo di supporto dei nodi per la compatibilità. Se esiste una connessione nodo non valida, il processo ha esito negativo e viene visualizzato un messaggio di errore.

Per risolvere una topologia, scegliere **Risolvi topologia** dal menu **topologia** .

La barra degli strumenti indica lo stato della topologia: **\[ solved \]** o **\[ not resolved \]**.

Se TopoEdit risolve correttamente una topologia, **lo stato della topologia** è impostato su **\[ risolto \]** e i controlli di riproduzione sono abilitati.

Ogni volta che si apportano modifiche alla topologia, **lo stato della topologia** è impostato su **\[ non risolto \]** , a indicare che è necessario risolverlo di nuovo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Compilazione di topologie tramite TopoEdit](building-topologies-by-using-topoedit.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 



