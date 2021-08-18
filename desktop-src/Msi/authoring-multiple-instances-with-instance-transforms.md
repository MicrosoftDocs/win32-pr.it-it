---
description: Per installare più istanze di un prodotto da un pacchetto del programma di installazione di Windows, è necessario creare un pacchetto di installazione di base per il prodotto e una trasformazione di istanza per ogni istanza da installare oltre all'istanza di base.
ms.assetid: fef49dda-503f-4b13-8763-70cb2ee0df5d
title: Creazione di più istanze con trasformazioni di istanza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0efac957d5e0e82665cb1ba20aeb42fe9b60293699c5c3fd97f5e6a6f1abf58a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745911"
---
# <a name="authoring-multiple-instances-with-instance-transforms"></a>Creazione di più istanze con trasformazioni di istanza

Per installare più istanze di un prodotto da un pacchetto del programma di installazione di Windows, è necessario creare un pacchetto di installazione di base per il prodotto e una trasformazione di istanza per ogni istanza da installare oltre all'istanza di base. Quando si crea il pacchetto di base e le trasformazioni, usare le linee guida seguenti:

-   L'applicazione di installazione può verificare la presenza del programma di installazione in esecuzione in una versione di Windows Vista, Windows Server 2003, Windows XP con Service Pack 1 (SP1) e Windows Installer 3.0 redistributable. Una qualsiasi di queste versioni del programma di installazione (o versioni successive) è necessaria per installare più istanze da un singolo pacchetto usando una trasformazione che modifica il codice del prodotto.
-   Ogni istanza deve avere un codice prodotto e un identificatore di istanza univoci. È possibile definire una proprietà nel pacchetto di base, il cui valore può essere impostato sull'identificatore di istanza.
-   Per mantenere isolati i file di ogni istanza, il pacchetto di base deve installare i file in un percorso di directory che dipende dall'identificatore dell'istanza.
-   Per mantenere isolati i dati non file di ogni istanza, il pacchetto di base deve raccogliere dati non file in set di componenti per ogni istanza. I componenti appropriati devono quindi essere installati in base alle istruzioni condizionali che dipendono dall'identificatore di istanza.
-   Creare una trasformazione di istanza per ogni istanza installata in aggiunta all'istanza di base. Il pacchetto di base può installare la propria istanza.
-   La trasformazione dell'istanza deve modificare il codice prodotto e l'identificatore per ogni istanza.
-   È consigliabile che la trasformazione del prodotto cambi anche il nome del prodotto in modo che l'istanza sia immediatamente distinta in Installazione applicazioni tramite Pannello di controllo.
-   Se la trasformazione dell'istanza installa i file, questi devono essere installati in una directory che dipende dall'identificatore dell'istanza.
-   Tutti i dati non file, ad esempio le chiavi del Registro di sistema, devono includere il nome dell'istanza nel percorso per evitare conflitti. Questa operazione può essere eseguita usando la proprietà il cui valore è l'identificatore di istanza nel percorso, come illustrato nell'esempio seguente di una tabella [del Registro di sistema](registry-table.md).



| Registro | Radice | Codice                                            | Nome         | Valore           | Componente\_      |
|----------|------|------------------------------------------------|--------------|-----------------|------------------|
| Reg1     | 1    | Software \\ Microsoft \\ MyProduct \\ \[ InstanceId\] | InstanceGuid | \[ProductCode\] | NonFileDataComp1 |



 

Per altre informazioni, vedere [Installazione di più istanze](installing-multiple-instances-of-products-and-patches.md) di prodotti e patch e Installazione di più istanze con trasformazioni di [istanza](installing-multiple-instances-with-instance-transforms.md).

 

 



