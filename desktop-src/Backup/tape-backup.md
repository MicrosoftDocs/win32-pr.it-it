---
title: Backup su nastro
description: Un volume nastro è costituito da un supporto di registrazione e dal relativo supporto fisico. Ogni volume nastro ha una o più partizioni. Le partizioni sono in genere suddivise in sezioni per contrassegni file o setmark. Esistono tre tipi di contrassegni file.
ms.assetid: 2057e6e4-b674-4151-b3b6-bde5d87d10c1
keywords:
- backup Backup , nastro
- Backup su nastro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 217c1a536b8a1a345218d3748c6207e9b336b84eca4cea0f4e48b4e84c521733
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588831"
---
# <a name="tape-backup"></a>Backup su nastro

Un *volume nastro è* costituito da un supporto di registrazione e dal relativo supporto fisico. L'intera lunghezza del nastro in un volume non è disponibile per la registrazione dei dati. Le brevi sezioni all'inizio e alla fine del nastro sono riservate per il collegamento del nastro agli hub del supporto. La prima posizione sul nastro in cui è possibile registrare i dati è denominata marcatore di inizio medio e l'ultima posizione è denominata marcatore di fine *media.*

Ogni volume nastro ha una o più partizioni. Una partizione è una parte del volume, contenente i propri punti di inizio e di fine, che non si sovrappone ad altre parti del volume. Ogni partizione ha tre posizioni predefinite. La prima posizione in una partizione in cui è possibile registrare i dati è denominata marcatore di inizio partizione e l'ultima è denominata marcatore *di fine partizione*. Il *marcatore di avviso* anticipato si trova immediatamente prima del marcatore di fine partizione. La posizione di avviso anticipata notifica alle applicazioni nastro di trasferire i dati memorizzati nel buffer sul nastro prima di raggiungere il marcatore di fine partizione.

L'area tra i punti di inizio e di fine di una partizione è in genere suddivisa in sezioni per *contrassegni file* *o contrassegni set*. I contrassegni file e setmark sono elementi registrati speciali che non contengono dati utente. si limitano a dividere la partizione in aree più piccole per fornire uno schema di indirizzi. I contrassegni file e setmark hanno scopi simili, ma offrono un posizionamento più rapido su unità nastro ad alta capacità.

In genere, i dispositivi nastro supportano i contrassegni file e i contrassegni di set. Il supporto di entrambi consente la formattazione dei dati su nastro in modo che i contrassegni di impostazione separino i dati da volumi del disco diversi e i contrassegni file separano i dati dai singoli file in un volume su disco.

Un altro elemento registrato che indica le posizioni sul nastro è un gap di *cancellazione,* un'area di nastro cancellato o un modello che il dispositivo non riconosce come contrassegno o come dati utente.

Esistono tre tipi di contrassegni file. Un *breve contrassegno di file* contiene un breve intervallo di cancellazione che non può essere sovrascritto a meno che l'operazione di scrittura non venga eseguita dall'inizio della partizione o da un contrassegno file lungo precedente. Un *lungo contrassegno* di file contiene un lungo gap di cancellazione che consente a un'applicazione di posizionare il nastro all'inizio del contrassegno file e di sovrascrivere il contrassegno file e lo spazio vuoto. Un *contrassegno di file* normale non contiene un gap di cancellazione. I dispositivi nastro che usano contrassegni file supportano contrassegni di file brevi e lunghi o contrassegni di file normali, ma non tutti e tre.

L'area in una partizione tra setmarks o filemarks è disponibile per la registrazione dei dati. Un'unità di dati scritta o letta da un nastro viene definita blocco.

Per altre informazioni, vedere i seguenti argomenti:

-   [Inizializzazione nastro](tape-initialization.md)
-   [Input e output su nastro](tape-input-and-output.md)
-   [Creazione di un'applicazione di backup](creating-a-backup-application.md)
-   [Backup e ripristino di collegamenti rigidi](backing-up-and-restoring-hard-links.md)

 

 




