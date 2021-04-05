---
title: Progettazione di interfacce utilizzabili in remoto
description: Con l'avvento del modello a oggetti del componente distribuito, è importante che l'interfaccia personalizzata sia utilizzabile in modalità remota, anche se si prevede di usarla solo in-process.
ms.assetid: 2ee4d950-dfd5-4965-bd77-a600e878be59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3502604d62e6a5129ca3e3538761722909c0198f
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "103857953"
---
# <a name="designing-remotable-interfaces"></a>Progettazione di interfacce utilizzabili in remoto

Con l'avvento del modello a oggetti del componente distribuito, è importante che l'interfaccia personalizzata sia utilizzabile in modalità remota, anche se si prevede di usarla solo in-process.

MIDL non è solo un modo per generare file di intestazione per le interfacce. Si tratta di un linguaggio di programmazione per la comunicazione remota che consente di usare le interfacce tra computer, processi e limiti di thread. Ciò significa che è necessario verificare il comportamento delle interfacce definite da MIDL in tali condizioni prima di rilasciare il programma ai clienti. Se è stato commesso un errore in IDL e l'interfaccia non è stata eseguita correttamente, potrebbe essere difficile risolvere l'errore. È necessario modificare l'interfaccia con un nuovo IID e lasciare il vecchio in per la compatibilità con le versioni precedenti oppure convertire tutti i client e tutti i computer server contemporaneamente.

Anche se l'interfaccia non viene mai usata out-of-process, può essere usata tra thread. Il problema peggiore per un file IDL non verificato può verificarsi per i server in-process che non supportano più [Apartment a thread singolo](single-threaded-apartments.md). Un server che non specifica un modello di threading è implicitamente a thread singolo. Tutte le operazioni contrassegnate come a thread singolo vengono forzate al thread chiamato prima [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) o [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex). Se un altro thread era quello che ha attivato l'oggetto, tutte le interfacce sul server a thread singolo devono essere restituite al thread di attivazione, il che può comportare la restituzione di REGDB \_ E \_ IIDNOTREG in risposta a una chiamata a [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)). A meno che non sia possibile affermare che l'interfaccia è sia in-process che sempre chiamata sullo stesso thread, si otterrà una modalità remota in un determinato momento.

Infine, come Interface Designer, è necessario considerare come le applicazioni client utilizzeranno l'interfaccia. Due elementi, insieme, determinano se un'interfaccia sarà efficiente tra i limiti del processo e del computer: la frequenza delle chiamate al metodo oltre il limite dell'interfaccia e la quantità di dati da trasferire in una determinata chiamata al metodo. Sebbene COM renda le chiamate tra processi e tra reti trasparenti ai programmi, non è in grado di effettuare chiamate a frequenza elevata e larghezza di banda elevata in spazi di indirizzi. In alcuni casi, è più appropriato progettare interfacce che in genere verranno implementate solo come server in-process, mentre altre interfacce sono più appropriate per l'uso remoto.

 

 




