---
description: Non esistono essenzialmente vincoli per la scrittura di un'applicazione di avvio automatico.
ms.assetid: 6D95E5F0-8D93-47A8-9D8C-49CBDCA150A7
title: Come implementare le applicazioni di avvio AutoRun
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b553e102f574835103898b17558541000633412
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967445"
---
# <a name="how-to-implement-autorun-startup-applications"></a>Come implementare le applicazioni di avvio AutoRun

Non esistono essenzialmente vincoli per la scrittura di un'applicazione di avvio automatico. È possibile implementare l'applicazione di avvio per eseguire tutte le operazioni necessarie per installare, disinstallare, configurare o eseguire l'applicazione. Tuttavia, i suggerimenti seguenti forniscono alcune linee guida per l'implementazione di un'applicazione di avvio AutoRun efficace.

## <a name="instructions"></a>Istruzioni

### <a name="step-1"></a>Passaggio 1:

Assicurarsi che gli utenti ricevano il feedback appena possibile dopo aver inserito un disco di AutoRun nell'unità. Le applicazioni di avvio devono essere piccoli programmi che si caricano rapidamente. Devono identificare chiaramente l'applicazione e fornire un modo semplice per annullare l'operazione.

### <a name="step-2"></a>Passaggio 2:

Verificare se il programma è già installato. In caso contrario, il passaggio successivo sarà probabilmente la procedura di installazione. L'applicazione di avvio può trarre vantaggio dal tempo impiegato dall'utente per leggere la finestra di dialogo avviando un altro thread per iniziare a caricare il codice di installazione. Quando l'utente fa clic su **OK**, il programma di installazione sarà già in parte se non è completamente caricato. Questo approccio riduce significativamente la percezione dell'utente della quantità di tempo necessaria per caricare l'applicazione.

> [!Note]  
> In genere, la parte iniziale dell'applicazione di avvio presenta agli utenti un'interfaccia utente, ad esempio una finestra di dialogo, in cui viene chiesto come procedere.

 

### <a name="step-3"></a>Passaggio 3:

Avviare un altro thread per iniziare a caricare il codice dell'applicazione per ridurre il tempo di attesa per l'utente. Se l'applicazione è già stata installata, è probabile che l'utente abbia inserito il disco per l'esecuzione dell'applicazione.

### <a name="step-4"></a>Passaggio 4:

Utilizzare gli hint seguenti per ridurre al minimo l'utilizzo del disco rigido:

-   Tenere al minimo il numero di file che devono essere presenti sul disco rigido. Devono essere limitate a file essenziali per l'esecuzione del programma o che richiederebbe una quantità di tempo inaccettabile per la lettura da parte dei supporti.
-   In molti casi, l'installazione di file non essenziali sul disco rigido non è necessaria, ma potrebbe offrire vantaggi come un miglioramento delle prestazioni. Fornire all'utente la possibilità di decidere come fare il compromesso tra i costi e i vantaggi dell'archiviazione su disco rigido.
-   Fornire un modo per disinstallare tutti i componenti che sono stati posizionati sul disco rigido.
-   Se l'applicazione memorizza nella cache i dati, fornire all'utente un controllo su di essa. Includere le opzioni nell'applicazione di avvio, ad esempio l'impostazione di un limite per la quantità massima di dati memorizzati nella cache che verranno archiviati nel disco rigido o l'eliminazione di tutti i dati memorizzati nella cache al termine dell'applicazione.

### <a name="step-5"></a>Passaggio 5:

Se necessario, disabilitare autorun. L'esecuzione automatica può essere evitata a livello di codice o disabilitata interamente con il registro di sistema, anche quando un supporto include un file Autorun. inf. Per ulteriori informazioni, vedere [Abilitazione e disabilitazione dell'esecuzione automatica](autoplay-reg.md) .

 

 



