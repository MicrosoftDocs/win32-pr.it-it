---
description: Alcune applicazioni sono progettate in modo da impedire l'installazione di più istanze dell'applicazione in un computer.
ms.assetid: 951d20c8-7908-40d8-a9d5-d321340c97f3
title: Restrizioni di progettazione delle applicazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16b98e7b7d8dddf1cd74224573d355e1f42d75c8ae6122d20977bbc1b38ffb99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117917545"
---
# <a name="application-design-restrictions"></a>Restrizioni di progettazione delle applicazioni

Alcune applicazioni sono progettate in modo da impedire l'installazione di più istanze dell'applicazione in un computer. Con questa limitazione, un'applicazione non può usare la funzionalità partizioni. Per poter usare le partizioni per tale applicazione, potrebbe essere necessario modificare le funzionalità di progettazione dell'applicazione seguenti.

## <a name="tables-and-arrays"></a>Tabelle e matrici

Alcune applicazioni creano tabelle di database, tabelle in memoria o matrici che usano un CLSID come chiave univoca del Registro di sistema. In un computer senza partizioni, questa chiave del Registro di sistema è in genere computer/CLSID (un CLSID per computer).

Al contrario, in un computer con partizioni questa chiave del Registro di sistema è computer/ID partizione/ID applicazione/CLSID (più istanze di un CLSID per computer). Poiché la funzionalità partizioni consente l'esistenza di più istanze di un CLSID in un computer, le applicazioni che contengono elementi di progettazione che richiedono un CLSID univoco per ogni computer potrebbero essere influenzate negativamente.

## <a name="global-resources"></a>Risorse globali

Alcune applicazioni usano risorse globali, ad esempio memoria condivisa, file di dati e voci del Registro di sistema. Ciò potrebbe causare problemi se più istanze di un'applicazione di questo tipo vengono eseguite contemporaneamente.

Ad esempio, se un componente usa la memoria condivisa per interagire con altri componenti, sarà necessario modificare il componente in modo che ogni istanza del componente alloca la propria memoria condivisa.

## <a name="type-libraries"></a>Librerie dei tipi

Le librerie dei tipi forniscono informazioni sulle interfacce e sui metodi di un componente. Queste informazioni vengono usate per diversi scopi, tra cui:

-   Marshalling dei dati tra componenti quando vengono effettuate chiamate di funzione
-   Supporto dei componenti in coda COM+ e dei servizi eventi COM+
-   Fornire le informazioni corrette all'interno di un editor Visual Basic Microsoft

I riferimenti a una libreria dei tipi vengono installati nel Registro di sistema di un computer. Quando si sviluppano applicazioni che verranno richiamate dall'interno di partizioni, è importante che nel Registro di sistema sia installata la versione più recente di una libreria dei tipi. Ciò garantisce che l Visual Basic editor usato otterrà informazioni accurate sui metodi disponibili per tale componente.

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

 

 



