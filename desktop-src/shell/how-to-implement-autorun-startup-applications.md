---
description: Non esistono essenzialmente vincoli su come scrivere un'applicazione di avvio esecuzione automatica.
ms.assetid: 6D95E5F0-8D93-47A8-9D8C-49CBDCA150A7
title: Come implementare applicazioni di avvio automatico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb5c31f57c8a972ee6b138b55c09c432d9cf8fc1a9f33644c92c95229c344893
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119350771"
---
# <a name="how-to-implement-autorun-startup-applications"></a>Come implementare applicazioni di avvio automatico

Non esistono essenzialmente vincoli su come scrivere un'applicazione di avvio esecuzione automatica. È possibile implementare l'applicazione di avvio per eseguire tutte le operazioni necessarie per installare, disinstallare, configurare o eseguire l'applicazione. I suggerimenti seguenti forniscono tuttavia alcune linee guida per l'implementazione di un'applicazione di avvio con esecuzione automatica efficace.

## <a name="instructions"></a>Istruzioni

### <a name="step-1"></a>Passaggio 1:

Assicurarsi che gli utenti ricevano commenti e suggerimenti non appena possibile dopo l'inserimento di un disco di esecuzione automatica nell'unità. Le applicazioni di avvio devono essere programmi di piccole dimensioni che vengono caricati rapidamente. Devono identificare chiaramente l'applicazione e fornire un modo semplice per annullare l'operazione.

### <a name="step-2"></a>Passaggio 2:

Verificare se il programma è già installato. In caso contrario, il passaggio successivo sarà probabilmente la procedura di installazione. L'applicazione di avvio può sfruttare il tempo che l'utente dedica alla lettura della finestra di dialogo avviando un altro thread per iniziare a caricare il codice di installazione. Quando l'utente fa clic su **OK,** il programma di installazione sarà già parzialmente se non completamente caricato. Questo approccio riduce significativamente la percezione dell'utente della quantità di tempo necessario per caricare l'applicazione.

> [!Note]  
> In genere, la parte iniziale dell'applicazione di avvio presenta agli utenti un'interfaccia utente, ad esempio una finestra di dialogo, in cui viene chiesto come procedere.

 

### <a name="step-3"></a>Passaggio 3:

Avviare un altro thread per iniziare a caricare il codice dell'applicazione per abbreviare il tempo di attesa per l'utente. Se l'applicazione è già stata installata, l'utente probabilmente ha inserito il disco per eseguire l'applicazione.

### <a name="step-4"></a>Passaggio 4:

Usare i suggerimenti seguenti per ridurre al minimo l'utilizzo del disco rigido:

-   Mantenere il numero minimo di file che devono essere sul disco rigido. Devono essere limitati ai file essenziali per l'esecuzione del programma o che potrebbero richiedere una quantità inaccettabile di tempo per la lettura dai supporti.
-   In molti casi, l'installazione di file non necessari sul disco rigido non è necessaria, ma può offrire vantaggi quali un aumento delle prestazioni. Offrire all'utente la possibilità di decidere come effettuare il compromesso tra i costi e i vantaggi dell'archiviazione su disco rigido.
-   Consente di disinstallare tutti i componenti che sono stati inseriti nel disco rigido.
-   Se l'applicazione memorizza nella cache i dati, concedere all'utente un certo controllo su di esso. Includere opzioni nell'applicazione di avvio, ad esempio l'impostazione di un limite per la quantità massima di dati memorizzati nella cache che verranno archiviati sul disco rigido o la necessità che l'applicazione scarti tutti i dati memorizzati nella cache al termine.

### <a name="step-5"></a>Passaggio 5:

Disabilitare l'esecuzione automatica, se necessario. L'esecuzione automatica può essere eliminata a livello di codice o disabilitata interamente con il Registro di sistema, anche quando un supporto include un file Autorun.inf. Per [altre informazioni, vedere Abilitazione e disabilitazione dell'esecuzione](autoplay-reg.md) automatica.

 

 



