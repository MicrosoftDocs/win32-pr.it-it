---
description: Heap a tolleranza di errore
ms.assetid: f1ac375a-3f08-49cd-8752-6f55db24a60c
title: Heap a tolleranza di errore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b17ab2630e6dc28cb84604e48be1aa60bf208a97
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088399"
---
# <a name="fault-tolerant-heap"></a>Heap a tolleranza di errore

## <a name="affected-platforms"></a>Piattaforme interessate

**Client -** Windows 7  

## <a name="feature-impact"></a>Impatto sulle funzionalità

 **Gravità :** Medio  
**Frequenza -** Basso  


## <a name="description"></a>Descrizione

L'heap a tolleranza di errore (FTH) è un sottosistema di Windows 7 responsabile del monitoraggio degli arresti anomali delle applicazioni e dell'applicazione autonoma di mitigazioni per evitare arresti anomali futuri per ogni applicazione. Per la maggior parte degli utenti, FTH funzionerà senza necessità di intervento o modifica da parte dell'utente. Tuttavia, in alcuni casi, gli sviluppatori di applicazioni e i tester software potrebbero dover eseguire l'override del comportamento predefinito di questo sistema.

## <a name="solution"></a>Soluzione

**Visualizzazione dell'attività heap a tolleranza di errore**

Heap a tolleranza di errore registra le informazioni all'avvio, all'arresto o all'avvio del servizio per attenuare i problemi relativi a una nuova applicazione. Per vedere le informazioni, seguire questa procedura:

1.  Fare clic sul menu Start.
2.  Fare clic con il pulsante **destro del mouse** su Computer e scegliere **Gestisci**.
3.  Fare **clic Visualizzatore eventi** registri applicazioni e  >  **servizi** di  >  **Microsoft** Windows > heap a tolleranza di  >  **errore**
4.  Visualizzare gli eventi FTH.

Gli eventi di arresto e avvio del servizio non contengono dati aggiuntivi. L'evento FTH Enabled contiene l'ID processo (PID), il nome dell'immagine del processo e l'ora di inizio dell'istanza del processo.

**Disabilitazione dell'heap a tolleranza di errore**

**Attenzione** Possono verificarsi problemi gravi se si modifica il Registro di sistema in modo non corretto usando l'editor del Registro di sistema o un altro metodo. Questi problemi possono richiedere la reinstallazione del sistema operativo. Microsoft non garantisce la possibilità di risolvere questi problemi. La modifica del Registro di sistema è a rischio e pericolo dell'utente.  
 Per disabilitare l'heap a tolleranza di errore interamente in un sistema, impostare il valore \_ DWORD **REG HKLM \\ Software Microsoft \\ \\ FTH \\ Enabled** su **0.**

Dopo aver modificato questo valore, riavviare il sistema. FTH non verrà più attivato per le nuove applicazioni.

**Reimpostazione dell'elenco di applicazioni rilevate da FTH**

L'heap a tolleranza di errore è a gestione autonoma e interromperà autonomamente l'applicazione nel caso in cui le mitigazioni non siano effettive per una determinata applicazione. Tuttavia, se è necessario reimpostare l'elenco di applicazioni per cui FTH sta attenuando i problemi (ad esempio, se si sta testando un'applicazione ed è necessario riprodurre un arresto anomalo che FTH sta mitigando), è possibile eseguire il comando seguente da un prompt dei comandi con privilegi elevati:  **Rundll32.exe fthsvc.dll,FthSysprepSpecialize**  
**Attenzione** L'esecuzione di questo comando cancella tutte le applicazioni FTH, pertanto le applicazioni che funzionano correttamente potrebbero iniziare di nuovo a bloccarsi dopo l'esecuzione di questo comando.  

 

 



