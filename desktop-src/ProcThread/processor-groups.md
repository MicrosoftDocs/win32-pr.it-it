---
description: Le versioni a 64 bit di Windows 7 e Windows Server 2008 R2 e versioni successive di Windows supportano più di 64 processori logici in un singolo computer. Questa funzionalità non è disponibile nelle versioni di Windows a 32 bit.
ms.assetid: c627ac0f-96e8-48b5-9103-4316f487e173
title: Gruppi di processori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cebc5b9ab1b386847b6561a9f6322c2fca0e2ae5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104050014"
---
# <a name="processor-groups"></a>Gruppi di processori

Le versioni a 64 bit di Windows 7 e Windows Server 2008 R2 e versioni successive di Windows supportano più di 64 processori logici in un singolo computer. Questa funzionalità non è disponibile nelle versioni di Windows a 32 bit.

I sistemi con più processori fisici o sistemi con processori fisici che dispongono di più core forniscono il sistema operativo con più processori logici. Un *processore logico* è un motore di calcolo logico dal punto di vista del sistema operativo, dell'applicazione o del driver. Un *Core* è un'unità del processore, che può essere costituita da uno o più processori logici. Un *processore fisico* può essere costituito da uno o più core. Un processore fisico corrisponde a un pacchetto del processore, un socket o una CPU.

Il supporto per i sistemi con più di 64 processori logici è basato sul concetto di un *gruppo* di processori, ovvero un set statico di un massimo di 64 processori logici considerati come una singola entità di pianificazione. I gruppi di processori sono numerati a partire da 0. I sistemi con meno di 64 processori logici hanno sempre un solo gruppo, gruppo 0.

**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** I gruppi di processori non sono supportati.

All'avvio del sistema, il sistema operativo crea gruppi di processori e assegna processori logici ai gruppi. Se il sistema è in grado di aggiungere processori a caldo, il sistema operativo consente lo spazio in gruppi per i processori che potrebbero arrivare mentre il sistema è in esecuzione. Il sistema operativo riduce al minimo il numero di gruppi in un sistema. Ad esempio, un sistema con processori logici 128 avrà due gruppi di processori con processori 64 in ogni gruppo, non quattro gruppi con processori logici 32 in ogni gruppo.

Per ottenere prestazioni migliori, il sistema operativo prende in considerazione la località fisica quando si assegnano processori logici ai gruppi. Tutti i processori logici in un core e tutti i core in un processore fisico vengono assegnati allo stesso gruppo, se possibile. I processori fisici che sono fisicamente vicini l'uno all'altro vengono assegnati allo stesso gruppo. Un nodo NUMA viene assegnato a un singolo gruppo, a meno che la capacità del nodo non superi le dimensioni massime del gruppo. Per ulteriori informazioni, vedere [supporto NUMA](numa-support.md).

Nei sistemi con 64 o un minor numero di processori, le applicazioni esistenti funzioneranno correttamente senza modifiche. Le applicazioni che non chiamano funzioni che utilizzano maschere di affinità processori o numeri di processore funzioneranno correttamente su tutti i sistemi, indipendentemente dal numero di processori. Per funzionare correttamente nei sistemi con più di 64 processori logici, potrebbe essere necessario modificare i tipi di applicazioni seguenti:

-   Le applicazioni che gestiscono, gestiscono o visualizzano le informazioni per processore per l'intero sistema devono essere modificate per supportare più di 64 processori logici. Un esempio di tale applicazione è gestione attività di Windows, che consente di visualizzare il carico di lavoro di ogni processore nel sistema.
-   Le applicazioni per le quali le prestazioni sono critiche e che possono essere ridimensionate in modo efficiente oltre 64 processori logici devono essere modificate per l'esecuzione su tali sistemi. Ad esempio, le applicazioni di database possono trarre vantaggio dalle modifiche.
-   Se un'applicazione utilizza una DLL con strutture di dati per processore e la DLL non è stata modificata per supportare più di 64 processori logici, tutti i thread nell'applicazione che chiamano le funzioni esportate dalla DLL devono essere assegnati allo stesso gruppo.

Per impostazione predefinita, un'applicazione è vincolata a un singolo gruppo, che dovrebbe offrire un'ampia funzionalità di elaborazione per l'applicazione tipica. Il sistema operativo assegna inizialmente ogni processo a un singolo gruppo in modo round robin tra i gruppi nel sistema. Un processo inizia l'esecuzione assegnata a un gruppo. Il primo thread di un processo viene inizialmente eseguito nel gruppo a cui è assegnato il processo. Ogni thread appena creato viene assegnato allo stesso gruppo del thread che lo ha creato.

Un'applicazione che richiede l'uso di più gruppi, in modo che possa essere eseguita su più di 64 processori, deve determinare in modo esplicito dove eseguire i thread ed è responsabile dell'impostazione delle affinità del processore dei thread per i gruppi desiderati. Il flag di [ \_ \_ affinità padre ereditato](process-creation-flags.md) può essere usato per specificare un processo padre, che può essere diverso dal processo corrente, da cui generare l'affinità per un nuovo processo. Se il processo è in esecuzione in un singolo gruppo, può leggere e modificare l'affinità usando [**GetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-getprocessaffinitymask) e [**SetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask) rimanendo nello stesso gruppo. Se l'affinità del processo viene modificata, la nuova affinità viene applicata ai relativi thread.

È possibile specificare l'affinità di un thread in fase di creazione usando l'attributo esteso [**\_ \_ \_ \_ affinity Attribute del gruppo di thread proc**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-updateprocthreadattribute) con la funzione [**CreateRemoteThreadEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethreadex) . Dopo la creazione del thread, è possibile modificare l'affinità chiamando [**SetThreadAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setthreadaffinitymask) o [**SetThreadGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-setthreadgroupaffinity). Se un thread viene assegnato a un gruppo diverso da quello del processo, l'affinità del processo viene aggiornata in modo da includere l'affinità del thread e il processo diventa un processo multigruppo. È necessario apportare ulteriori modifiche di affinità per i singoli thread; non è possibile modificare l'affinità del processo multigruppo con [**SetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask). La funzione [**GetProcessGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-getprocessgroupaffinity) Recupera il set di gruppi a cui sono assegnati un processo e i relativi thread.

Per specificare l'affinità per tutti i processi associati a un oggetto processo, usare la funzione [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) con la classe di informazioni **JobObjectGroupInformation** o **JobObjectGroupInformationEx** .

Un processore logico viene identificato in base al numero di gruppo e al numero di processore relativo al gruppo. Questa operazione è rappresentata da una struttura di [**\_ numeri di processore**](/windows/desktop/api/WinNT/ns-winnt-processor_number) . I numeri di processore numerici utilizzati dalle funzioni legacy sono relativi al gruppo.

Per informazioni sulle modifiche apportate all'architettura del sistema operativo per supportare più di 64 processori, vedere i sistemi di supporto white paper con [più di 64 processori](https://www.microsoft.com/whdc/system/Sysinternals/MoreThan64proc.mspx).

Per un elenco delle nuove funzioni e strutture che supportano i gruppi di processori, vedere Novità di [processi e thread](what-s-new-in-processes-and-threads.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Processori multipli](multiple-processors.md)
</dt> <dt>

[Supporto NUMA](numa-support.md)
</dt> </dl>

 

 
