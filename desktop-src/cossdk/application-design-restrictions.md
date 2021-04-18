---
description: Alcune applicazioni sono progettate in modo da impedire l'installazione di più istanze dell'applicazione in un computer.
ms.assetid: 951d20c8-7908-40d8-a9d5-d321340c97f3
title: Limitazioni relative alla progettazione di applicazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1c4307a979866e3df9f019e69b858e8347c295b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304739"
---
# <a name="application-design-restrictions"></a>Limitazioni relative alla progettazione di applicazioni

Alcune applicazioni sono progettate in modo da impedire l'installazione di più istanze dell'applicazione in un computer. Con tale limitazione, un'applicazione non può utilizzare la funzionalità partizioni. Potrebbe essere necessario modificare le seguenti funzionalità di progettazione dell'applicazione prima di poter utilizzare le partizioni per l'applicazione.

## <a name="tables-and-arrays"></a>Tabelle e matrici

Alcune applicazioni creano tabelle di database, tabelle in memoria o matrici che utilizzano un CLSID come chiave univoca del registro di sistema. In un computer senza partizioni, questa chiave del registro di sistema è in genere computer/CLSID (un CLSID per computer).

Viceversa, in un computer con partizioni, questa chiave del registro di sistema è ID computer/partizione/ID applicazione/CLSID (più istanze di un CLSID per computer). Poiché la funzionalità partizioni consente l'esistenza di più istanze di un CLSID in un computer, le applicazioni che contengono elementi di progettazione che richiedono un CLSID univoco per computer potrebbero essere compromesse.

## <a name="global-resources"></a>Risorse globali

Alcune applicazioni utilizzano risorse globali quali la memoria condivisa, i file di dati e le voci del registro di sistema. Questo può causare problemi se più istanze di tale applicazione sono in esecuzione simultaneamente.

Se, ad esempio, un componente utilizza memoria condivisa per interagire con altri componenti, sarà necessario modificare il componente in modo che ogni istanza del componente allochi la propria memoria condivisa.

## <a name="type-libraries"></a>Librerie dei tipi

Le librerie dei tipi forniscono informazioni sulle interfacce e i metodi di un componente. Queste informazioni vengono utilizzate per diversi scopi, incluse le seguenti:

-   Marshalling dei dati tra i componenti quando vengono effettuate chiamate di funzione
-   Supporto dei componenti in coda COM+ e dei servizi eventi COM+
-   Fornire le informazioni corrette in un editor di Microsoft Visual Basic

I riferimenti a una libreria dei tipi vengono installati nel registro di sistema di un computer. Quando si sviluppano applicazioni che verranno richiamate dall'interno di partizioni, è importante che nel registro di sistema sia installata la versione più recente di una libreria dei tipi. In questo modo si garantisce che l'editor Visual Basic in uso ottenga informazioni accurate sui metodi disponibili per tale componente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Componenti e partizioni in coda COM+](com--queued-components-and-partitions.md)
</dt> <dt>

[Implementazione della partizione](partition-implementation.md)
</dt> <dt>

[Registrazione e attivazione di componenti nelle partizioni](registering-and-activating-components-in-partitions.md)
</dt> <dt>

[Che cosa sono le partizioni COM+?](what-are-com--partitions-.md)
</dt> </dl>

 

 



