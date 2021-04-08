---
title: Backup su nastro
description: Un volume di nastri è costituito da un supporto di registrazione e dal relativo operatore fisico. Ogni volume del nastro dispone di una o più partizioni. Le partizioni vengono in genere divise in sezioni in base ai filemark o ai contrassegni. Sono disponibili tre tipi di filemark.
ms.assetid: 2057e6e4-b674-4151-b3b6-bde5d87d10c1
keywords:
- backup backup, nastro
- Backup su nastro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2820e512646642046059cb151061e3f605d56cd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044256"
---
# <a name="tape-backup"></a>Backup su nastro

Un *volume di nastri* è costituito da un supporto di registrazione e dal relativo operatore fisico. L'intera lunghezza del nastro in un volume non è disponibile per la registrazione dei dati. Le sezioni brevi all'inizio e alla fine del nastro sono riservate per il fissaggio del nastro agli hub del vettore. La prima posizione sul nastro in cui è possibile registrare i dati è chiamata *indicatore di inizio di media* e l'ultima posizione viene chiamata *indicatore di fine del supporto*.

Ogni volume del nastro dispone di una o più partizioni. Una partizione è una parte del volume, che contiene i punti iniziali e finali, che non si sovrappongono a qualsiasi altra parte del volume. Ogni partizione ha tre posizioni predefinite. La prima posizione in una partizione in cui è possibile registrare i dati è denominata *marcatore di inizio della partizione* e l'ultimo è denominato *marcatore di fine partizione*. Il *marcatore di avviso anticipato* si trova immediatamente prima del marcatore di fine partizione. La posizione di avviso anticipato informa le applicazioni nastro di trasferire i dati memorizzati nel buffer sul nastro prima di raggiungere il marcatore di fine partizione.

L'area tra i punti di inizio e fine di una partizione viene in genere divisa in sezioni in base ai *filemark* o *ai contrassegni.* I contrassegni e i contrassegni sono elementi speciali registrati che non contengono dati utente; dividono semplicemente la partizione in aree più piccole per fornire uno schema di indirizzi. I contrassegni e i segni di spunta hanno scopi simili, ma i segni di spunta forniscono un posizionamento più veloce sulle unità nastro ad alta capacità.

In genere, i dispositivi nastro supportano i filemark e i contrassegni. Il supporto di entrambi i tipi consente di formattare i dati del nastro in modo da contrassegnare i dati separati da volumi di dischi diversi e i file di contrassegno separati dai singoli file in un volume del disco.

Un altro elemento registrato che indica le posizioni sul nastro è uno *spazio di cancellazione*, un'area del nastro cancellato o un modello che il dispositivo non riconosce come contrassegno o come dati utente.

Sono disponibili tre tipi di filemark. Un *breve filemark* contiene un breve gap di cancellazione che non può essere sovrascritto, a meno che l'operazione di scrittura non venga eseguita dall'inizio della partizione o da un filemark lungo precedente. Un *filemark lungo* contiene uno spazio di cancellazione lungo che consente a un'applicazione di posizionare il nastro all'inizio del filemark e di sovrascrivere il filemark e il gap di cancellazione. Un *filemark normale* non contiene un gap di cancellazione. I dispositivi nastro che usano i filemark supportano i filemark brevi e lunghi o i filemark normali, ma non tutti e tre.

L'area di una partizione tra i contrassegni o i filemark è disponibile per la registrazione dei dati. Un'unità di dati scritti o letti da un nastro viene definita blocco.

Per altre informazioni, vedere i seguenti argomenti:

-   [Inizializzazione del nastro](tape-initialization.md)
-   [Input e output su nastro](tape-input-and-output.md)
-   [Creazione di un'applicazione di backup](creating-a-backup-application.md)
-   [Backup e ripristino di collegamenti reali](backing-up-and-restoring-hard-links.md)

 

 




