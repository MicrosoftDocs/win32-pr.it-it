---
description: .
ms.assetid: f1ac375a-3f08-49cd-8752-6f55db24a60c
title: Heap a tolleranza di errore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 349c8c3d6d066de3d563880c169c8dde2e062370
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318884"
---
# <a name="fault-tolerant-heap"></a>Heap a tolleranza di errore

## <a name="affected-platforms"></a>Piattaforme interessate

**Client-** Windows 7  

## <a name="feature-impact"></a>Effetto sulle funzionalità

 **Gravità-** Media  
**Frequenza-** Basso  


## <a name="description"></a>Descrizione

L'heap a tolleranza di errore (FTH) è un sottosistema di Windows 7 responsabile del monitoraggio degli arresti anomali dell'applicazione e dell'applicazione autonoma delle mitigazioni per impedire arresti anomali futuri in base alle singole applicazioni. Per la maggior parte degli utenti, FTH funzionerà senza alcuna necessità di intervento o modifica. Tuttavia, in alcuni casi, gli sviluppatori di applicazioni e i tester software potrebbero dover eseguire l'override del comportamento predefinito di questo sistema.

## <a name="solution"></a>Soluzione

**Visualizzazione dell'attività heap a tolleranza di errore**

L'heap a tolleranza di errore registra le informazioni quando il servizio viene avviato, arrestato o inizia a mitigare i problemi per una nuova applicazione. Per vedere le informazioni, seguire questa procedura:

1.  Fare clic sul menu Start.
2.  Fare clic con il pulsante destro del mouse su **computer** e scegliere **gestione**.
3.  Fare clic su **Visualizzatore eventi**  >  **registri applicazioni e servizi**  >  **Microsoft**  >  **Windows > a tolleranza di errore-heap**
4.  Visualizzare gli eventi FTH.

Gli eventi di arresto e avvio del servizio non contengono dati aggiuntivi. L'evento FTH Enabled contiene l'ID del processo (PID), il nome dell'immagine del processo e l'ora di inizio dell'istanza del processo.

**Disabilitazione dell'heap a tolleranza di errore**

**Attenzione** Se si modifica il registro di sistema in modo errato utilizzando l'editor del registro di sistema o un altro metodo, possono verificarsi problemi gravi. Questi problemi potrebbero richiedere la reinstallazione del sistema operativo. Microsoft non garantisce la possibilità di risolvere questi problemi. La modifica del Registro di sistema è a rischio e pericolo dell'utente.  
 Per disabilitare completamente l'heap a tolleranza di errore in un sistema, impostare il \_ valore reg DWORD **HKLM \\ software \\ Microsoft \\ FTH \\ abilitato** su **0**.

Dopo avere modificato questo valore, riavviare il sistema. FTH non si attiverà più per le nuove applicazioni.

**Reimpostazione dell'elenco di applicazioni registrate da FTH**

L'heap a tolleranza di errore è gestito autonomamente e si arresterà in modo autonomo nel caso in cui le mitigazioni non siano valide per una determinata applicazione. Tuttavia, se è necessario reimpostare l'elenco delle applicazioni per cui FTH è in grado di attenuare i problemi (ad esempio, se si sta testando un'applicazione ed è necessario riprodurre un arresto anomalo di FTH), è possibile eseguire il comando seguente da un prompt dei comandi con privilegi elevati:  **Rundll32.exe fthsvc.dll, FthSysprepSpecialize**  
**Attenzione** L'esecuzione di questo comando eliminerà tutte le applicazioni FTH, in modo che le applicazioni che funzionano attualmente correttamente potrebbero iniziare a arrestarsi nuovamente dopo l'esecuzione di questo comando.  

 

 



