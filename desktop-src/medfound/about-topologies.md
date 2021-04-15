---
description: Informazioni sulle topologie
ms.assetid: 4f69b099-0ca7-4ea6-8412-0f1ea02e1600
title: Informazioni sulle topologie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35008d839e8054554370039dd13297ae7a1f0b0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104569517"
---
# <a name="about-topologies"></a>Informazioni sulle topologie

Una topologia è un oggetto che rappresenta la modalità di flusso dei dati nella pipeline. Un'applicazione crea una topologia per descrivere il percorso che ogni flusso prende dall'origine multimediale a un sink multimediale. L'applicazione passa la topologia alla sessione multimediale e la sessione multimediale utilizza la topologia per controllare il flusso di dati.

I componenti di elaborazione dati nella pipeline (origini multimediali, trasformazioni e sink multimediali) sono rappresentati nella topologia come *nodi*. Il flusso di dati da un componente a un altro è rappresentato da una connessione tra i nodi. Sono definiti i seguenti tipi di nodo:

-   Nodo di origine: rappresenta un flusso multimediale su un'origine multimediale.
-   Nodo Transform: rappresenta una trasformazione Media Foundation (MFT).
-   Nodo di output: rappresenta un sink del flusso in un sink multimediale.
-   Tee node: rappresenta un fork nel flusso. I nodi Tee rappresentano un'eccezione alla regola che un nodo rappresenta un oggetto pipeline. A differenza di altri tipi di nodo, il nodo Tee indirizza semplicemente il flusso di dati.

Una topologia funzionante deve contenere almeno un nodo di origine connesso a un nodo di output, possibilmente attraverso uno o più nodi di trasformazione. Nel diagramma seguente, ad esempio, viene illustrata una topologia semplice con un flusso.

![diagramma che mostra una topologia con un flusso.](images/topology01.png)

Per la riproduzione di file, il nodo Transform potrebbe rappresentare un decodificatore e il nodo di output rappresenterebbe il renderer audio o video. Per la codifica dei file, il nodo di trasformazione rappresenterebbe un codificatore e il nodo di output rappresenterebbe un sink di archivio, ad esempio il sink di file ASF.

Se due nodi sono connessi, il nodo che produce dati viene chiamato nodo *upstream* e il nodo che riceve i dati viene chiamato nodo *downstream* . Nel diagramma precedente, ad esempio, il nodo di origine è upstream dal nodo Transform.

In una coppia di nodi connessi, il punto di connessione nel nodo upstream è denominato *output*. Il punto di connessione nel nodo downstream è denominato *input*. Il diagramma seguente mostra una coppia di nodi con i relativi punti di connessione e il flusso di dati tra di essi. I punti di connessione non sono rappresentati come oggetti separati nella topologia. Sono specificati dal valore di indice nell'oggetto node.

![diagramma che mostra due nodi connessi.](images/topology04.png)

Un nodo di origine non può contenere input. Pertanto, non possono essere presenti nodi upstream da un nodo di origine. Analogamente, un nodo di output non può contenere output e non possono essere presenti nodi downstream da un nodo di output. Una catena di nodi da un nodo di origine a un nodo di output viene chiamata *ramo* della topologia. Il primo diagramma di questo argomento illustra una topologia con un solo ramo. In genere è presente un ramo per ogni flusso. Per riprodurre un file con un flusso audio e un flusso video, ad esempio, richiede una topologia con due rami.

## <a name="partial-topologies"></a>Topologie parziali

Una topologia completa o *completa* contiene un nodo per ogni oggetto pipeline necessario. Tuttavia, l'applicazione non deve necessariamente creare una topologia completa. Viene invece creata una topologia *parziale* che omette uno o più nodi di trasformazione.

La sessione multimediale completa la topologia usando un oggetto denominato caricatore della *topologia*. Il caricatore della topologia converte le topologie parziali in topologie complete inserendo le trasformazioni necessarie. Il processo di conversione viene chiamato *risoluzione* della topologia.

Per riprodurre un flusso audio codificato, ad esempio, è necessario che la topologia includa un decodificatore tra i nodi di origine e di output. L'applicazione crea una topologia parziale che connette il nodo di origine direttamente al nodo di output, senza il decodificatore. Il caricatore della topologia esamina i formati dei flussi, trova il decodificatore corretto e inserisce un nodo di trasformazione nella topologia.

Il diagramma seguente illustra la topologia parziale creata dall'applicazione.

![diagramma che mostra una parte parziale con un nodo di origine e un nodo di output.](images/topology02.png)

Il diagramma seguente mostra la topologia completa dopo che il caricatore della topologia lo risolve. In questo esempio, il caricatore della topologia ha inserito un nodo Transform per il decodificatore.

![diagramma che mostra una topologia completa.](images/topology03.png)

Nella versione corrente di Media Foundation, il caricatore della topologia supporta le topologie per la riproduzione. Per la codifica dei file e altri scenari, è necessario che l'applicazione costruisca una topologia completa.

Le applicazioni possono anche creare il caricatore della topologia e usarlo direttamente. Ad esempio, è possibile usare il caricatore della topologia per risolvere una topologia parziale e quindi modificare la topologia completa prima di assegnarla alla sessione multimediale. Per creare il caricatore della topologia, chiamare [**MFCreateTopoLoader**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopoloader).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Topologie](topologies.md)
</dt> </dl>

 

 



