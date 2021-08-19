---
description: Informazioni sulle topologie
ms.assetid: 4f69b099-0ca7-4ea6-8412-0f1ea02e1600
title: Informazioni sulle topologie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9410207ed5f235f61e167564f7a5dee8a1367044032be0a15cef9ac3b95fb9e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975125"
---
# <a name="about-topologies"></a>Informazioni sulle topologie

Una topologia è un oggetto che rappresenta il flusso dei dati nella pipeline. Un'applicazione crea una topologia per descrivere il percorso che ogni flusso accetta dall'origine multimediale a un sink multimediale. L'applicazione passa la topologia alla sessione multimediale e la sessione multimediale usa la topologia per controllare il flusso di dati.

I componenti di elaborazione dati nella pipeline (origini multimediali, trasformazioni e sink multimediali) sono rappresentati nella topologia come *nodi*. Il flusso di dati da un componente a un altro è rappresentato da una connessione tra i nodi. Vengono definiti i tipi di nodo seguenti:

-   Nodo di origine: rappresenta un flusso multimediale in un'origine multimediale.
-   Nodo Di trasformazione: rappresenta una Media Foundation di trasformazione (MFT).
-   Nodo di output: rappresenta un sink di flusso in un sink multimediale.
-   Nodo Tee: rappresenta un fork nel flusso. I nodi tee sono un'eccezione alla regola che indica che un nodo rappresenta un oggetto pipeline. A differenza di altri tipi di nodo, il nodo tee indirizza semplicemente il flusso di dati.

Una topologia funzionante deve contenere almeno un nodo di origine connesso a un nodo di output, possibilmente tramite uno o più nodi di trasformazione. Ad esempio, il diagramma seguente mostra una topologia semplice con un flusso.

![diagramma che mostra una topologia con un flusso.](images/topology01.png)

Per la riproduzione di file, il nodo di trasformazione potrebbe rappresentare un decodificatore e il nodo di output rappresenta il renderer audio o video. Per la codifica dei file, il nodo di trasformazione rappresenterebbe un codificatore e il nodo di output rappresenterebbe un sink di archivio, ad esempio il sink del file ASF.

Se due nodi sono connessi, il nodo che produce dati viene chiamato nodo *upstream* e il nodo che riceve i dati viene chiamato *nodo downstream.* Nel diagramma precedente, ad esempio, il nodo di origine è upstream dal nodo di trasformazione.

In una coppia di nodi connessi, il punto di connessione nel nodo upstream è denominato *output*. Il punto di connessione nel nodo downstream viene chiamato *input*. Il diagramma seguente mostra una coppia di nodi con i relativi punti di connessione e il flusso di dati tra di essi. I punti di connessione non sono rappresentati come oggetti separati nella topologia. Vengono specificati dal valore di indice nell'oggetto nodo.

![diagramma che mostra due nodi connessi.](images/topology04.png)

Un nodo di origine non può avere input. Pertanto, non possono essere presenti nodi upstream da un nodo di origine. Analogamente, un nodo di output non può avere output e non possono essere presenti nodi a valle da un nodo di output. Una catena di nodi da un nodo di origine a un nodo di output è detta *ramo* della topologia. Nel primo diagramma di questo argomento viene illustrata una topologia con un singolo ramo. In genere è presente un ramo per flusso. Per riprodurre un file con un flusso audio e un flusso video, ad esempio, è necessaria una topologia con due rami.

## <a name="partial-topologies"></a>Topologie parziali

Una topologia completa *o* completa contiene un nodo per ogni oggetto pipeline necessario. Tuttavia, l'applicazione non deve sempre creare una topologia completa. Crea invece una topologia *parziale* che omette uno o più nodi di trasformazione.

La sessione multimediale completa la topologia usando un oggetto denominato *caricatore della topologia*. Il caricatore della topologia converte le topologie parziali in topologie complete inserendo le trasformazioni necessarie. Il processo di conversione *è detto risoluzione* della topologia.

Ad esempio, per riprodurre un flusso audio codificato, la topologia deve avere un decodificatore tra i nodi di origine e di output. L'applicazione crea una topologia parziale che connette il nodo di origine direttamente al nodo di output, senza il decodificatore. Il caricatore della topologia esamina i formati di flusso, trova il decodificatore giusto e inserisce un nodo di trasformazione nella topologia.

Il diagramma seguente illustra la topologia parziale creata dall'applicazione.

![Diagramma che mostra un elemento parziale con un nodo di origine e un nodo di output.](images/topology02.png)

Il diagramma seguente mostra la topologia completa dopo che il caricatore della topologia la risolve. In questo esempio il caricatore della topologia ha inserito un nodo di trasformazione per il decodificatore.

![diagramma che mostra una topologia completa.](images/topology03.png)

Nella versione corrente di Media Foundation, il caricatore della topologia supporta topologie per la riproduzione. Per la codifica dei file e altri scenari, l'applicazione deve costruire una topologia completa.

Le applicazioni possono anche creare il caricatore della topologia e usarlo direttamente. Ad esempio, è possibile usare il caricatore della topologia per risolvere una topologia parziale e quindi modificare la topologia completa prima di darla alla sessione multimediale. Per creare il caricatore della topologia, chiamare [**MFCreateTopoLoader**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopoloader).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Topologie](topologies.md)
</dt> </dl>

 

 



