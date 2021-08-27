---
title: Progettazione di interfacce remota
description: Con l'avvento del modello a oggetti dei componenti distribuiti, è importante che l'interfaccia personalizzata sia remota, anche se si prevede di usarla solo in-process.
ms.assetid: 2ee4d950-dfd5-4965-bd77-a600e878be59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52df6deb3f83f253fc46436ba992dc3fc10f74d84e43c6027fd4426b3171a838
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071001"
---
# <a name="designing-remotable-interfaces"></a>Progettazione di interfacce remota

Con l'avvento del modello a oggetti dei componenti distribuiti, è importante che l'interfaccia personalizzata sia remota, anche se si prevede di usarla solo in-process.

MIDL non è solo un modo per generare file di intestazione per le interfacce. È un linguaggio di programmazione per la comunicazione remota che consente di usare le interfacce tra computer, processi e limiti di thread. Ciò significa che è necessario verificare il comportamento delle interfacce definite da MIDL in tali condizioni prima di rilasciare il programma ai clienti. Se si è fatto un errore nel file IDL e l'interfaccia non è remota correttamente, può essere difficile risolvere l'errore. È necessario modificare l'interfaccia con un nuovo IID e lasciare quello precedente per la compatibilità con le versioni precedenti oppure convertire ogni client e ogni computer server contemporaneamente.

Anche se l'interfaccia non verrà mai usata out-of-process, può essere usata tra thread. Il problema peggiore per un file IDL non controllato può verificarsi per i server in-process che non supportano più apartment [a thread singolo](single-threaded-apartments.md). Un server che non specifica un modello di threading è implicitamente a thread singolo. Tutti gli elementi contrassegnati come a thread singolo vengono forzati sul thread che ha chiamato [**prima CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) o [**CoInitializeEx.**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) Se un altro thread è quello che ha attivato l'oggetto, tutte le interfacce nel server a thread singolo devono essere di nuovo remote al thread di attivazione, il che può comportare la restituzione di REGDB \_ E \_ IIDNOTREG in risposta a una chiamata a [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)). A meno che non sia assolutamente possibile asserire che l'interfaccia è sia in-process che verrà sempre chiamata sullo stesso thread, in un certo momento si verrà remoti.

Infine, come finestra di progettazione dell'interfaccia, è necessario considerare il modo in cui le applicazioni client useranno l'interfaccia. Due elementi, insieme, determinano se un'interfaccia sarà efficiente tra i limiti del processo e del computer: la frequenza delle chiamate al metodo attraverso il limite dell'interfaccia e la quantità di dati da trasferire in una determinata chiamata al metodo. Anche se COM rende le chiamate tra processi e tra reti trasparenti per i programmi, non può rendere efficienti le chiamate ad alta frequenza e a larghezza di banda elevata negli spazi di indirizzi. In alcuni casi, è più appropriato progettare interfacce che in genere verranno implementate solo come server in-process, mentre altre interfacce sono più appropriate per l'uso remoto.

 

 




