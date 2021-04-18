---
description: Per installare più istanze di un prodotto da un pacchetto di Windows Installer, è necessario creare un pacchetto di installazione di base per il prodotto e una trasformazione istanza per ogni istanza da installare oltre all'istanza di di base.
ms.assetid: fef49dda-503f-4b13-8763-70cb2ee0df5d
title: Creazione di più istanze con le trasformazioni dell'istanza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c61424efbf08ea3e726594a3073f4ce7483af57d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311036"
---
# <a name="authoring-multiple-instances-with-instance-transforms"></a>Creazione di più istanze con le trasformazioni dell'istanza

Per installare più istanze di un prodotto da un pacchetto di Windows Installer, è necessario creare un pacchetto di installazione di base per il prodotto e una trasformazione istanza per ogni istanza da installare oltre all'istanza di di base. Usare le linee guida seguenti durante la creazione del pacchetto e delle trasformazioni di base:

-   L'applicazione di installazione può verificare la presenza del programma di installazione in esecuzione in una versione di Windows Vista, Windows Server 2003, Windows XP con Service Pack 1 (SP1) e il Windows Installer 3,0 ridistribuibile. Una di queste versioni del programma di installazione (o versioni successive) è necessaria per installare più istanze da un singolo pacchetto usando un codice prodotto, ovvero cambiando la trasformazione.
-   Ogni istanza deve disporre di un codice prodotto univoco e di un identificatore di istanza. È possibile definire una proprietà nel pacchetto di base, il cui valore può essere impostato sull'identificatore dell'istanza.
-   Per tenere isolati i file di ogni istanza, il pacchetto di base deve installare i file in un percorso di directory che dipende dall'identificatore dell'istanza.
-   Per tenere isolati i dati non del file di ogni istanza, il pacchetto di base deve raccogliere dati non file in set di componenti per ogni istanza. I componenti appropriati devono quindi essere installati in base a istruzioni condizionali che dipendono dall'identificatore dell'istanza.
-   Creare una trasformazione istanza per ogni istanza installata oltre all'istanza di base. Il pacchetto di base può installare una propria istanza.
-   La trasformazione istanza deve modificare il codice e l'identificatore del prodotto per ogni istanza.
-   È consigliabile che la trasformazione prodotto modifichi anche il nome del prodotto, in modo che l'istanza sia facilmente distinguibile in Installazione applicazioni tramite il pannello di controllo.
-   Se la trasformazione istanza installa i file, questi devono essere installati in una directory che dipende dall'identificatore dell'istanza.
-   Tutti i dati non di file, ad esempio le chiavi del registro di sistema, devono includere il nome dell'istanza nel percorso per evitare conflitti. Questa operazione può essere eseguita usando la proprietà il cui valore è l'identificatore dell'istanza nel percorso, come illustrato nell'esempio seguente di una [tabella del registro di sistema](registry-table.md).



| Registro | Radice | Codice                                            | Nome         | Valore           | Componente\_      |
|----------|------|------------------------------------------------|--------------|-----------------|------------------|
| Reg1     | 1    | Software \\ Microsoft \\ prodotto \\ \[ InstanceID\] | : InstanceGuid | \[ProductCode\] | NonFileDataComp1 |



 

Per ulteriori informazioni, vedere [installazione di più istanze di prodotti e patch](installing-multiple-instances-of-products-and-patches.md) e [installazione di più istanze con le trasformazioni dell'istanza](installing-multiple-instances-with-instance-transforms.md).

 

 



