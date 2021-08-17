---
description: Le versioni a 64 bit di Windows 7 e Windows Server 2008 R2 e versioni successive di Windows supportano più di 64 processori logici in un singolo computer. Questa funzionalità non è disponibile nelle versioni a 32 bit Windows.
ms.assetid: c627ac0f-96e8-48b5-9103-4316f487e173
title: Gruppi di processori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc5916faf3cf90bce7f8549834fe130f299f782d6b2534969c89d74df454ae9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119418671"
---
# <a name="processor-groups"></a>Gruppi di processori

Le versioni a 64 bit di Windows 7 e Windows Server 2008 R2 e versioni successive di Windows supportano più di 64 processori logici in un singolo computer. Questa funzionalità non è disponibile nelle versioni a 32 bit Windows.

I sistemi con più processori fisici o con processori fisici con più core forniscono al sistema operativo più processori logici. Un *processore logico* è un motore di calcolo logico dal punto di vista del sistema operativo, dell'applicazione o del driver. Un *core* è un'unità processore, che può essere costituita da uno o più processori logici. Un *processore* fisico può essere costituito da uno o più core. Un processore fisico è uguale a un pacchetto del processore, un socket o una CPU.

Il supporto per i sistemi con più di 64 processori logici si basa sul concetto di gruppo di processori *,* ovvero un set statico di fino a 64 processori logici considerati come una singola entità di pianificazione. I gruppi di processori sono numerati a partire da 0. I sistemi con meno di 64 processori logici hanno sempre un singolo gruppo, Il gruppo 0.

**Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP:** I gruppi di processori non sono supportati.

All'avvio del sistema, il sistema operativo crea gruppi di processori e assegna processori logici ai gruppi. Se il sistema è in grado di aggiungere processori a caldo, il sistema operativo consente lo spazio in gruppi per i processori che potrebbero arrivare mentre il sistema è in esecuzione. Il sistema operativo riduce al minimo il numero di gruppi in un sistema. Ad esempio, un sistema con 128 processori logici avrebbe due gruppi di processori con 64 processori in ogni gruppo, non quattro gruppi con 32 processori logici in ogni gruppo.

Per prestazioni migliori, il sistema operativo tiene conto della posizione fisica quando si assegnano processori logici ai gruppi. Tutti i processori logici in un core e tutti i core in un processore fisico vengono assegnati allo stesso gruppo, se possibile. I processori fisici fisicamente vicini tra loro vengono assegnati allo stesso gruppo. Un nodo NUMA viene assegnato a un singolo gruppo a meno che la capacità del nodo non superi le dimensioni massime del gruppo. Per altre informazioni, vedere [Supporto NUMA.](numa-support.md)

Nei sistemi con 64 o meno processori, le applicazioni esistenti funzioneranno correttamente senza modifiche. Le applicazioni che non chiamano funzioni che usano maschere di affinità del processore o numeri di processore funzioneranno correttamente in tutti i sistemi, indipendentemente dal numero di processori. Per funzionare correttamente nei sistemi con più di 64 processori logici, i tipi di applicazioni seguenti potrebbero richiedere modifiche:

-   Le applicazioni che gestiscono, gestiscono o visualizzano informazioni per processore per l'intero sistema devono essere modificate per supportare più di 64 processori logici. Un esempio di tale applicazione è Windows Gestione attività, che visualizza il carico di lavoro di ogni processore nel sistema.
-   Le applicazioni per cui le prestazioni sono critiche e che possono essere ridimensionate in modo efficiente oltre i 64 processori logici devono essere modificate per l'esecuzione in tali sistemi. Ad esempio, le applicazioni di database potrebbero trarre vantaggio dalle modifiche.
-   Se un'applicazione usa una DLL con strutture di dati per processore e la DLL non è stata modificata per supportare più di 64 processori logici, tutti i thread nell'applicazione che chiamano funzioni esportate dalla DLL devono essere assegnati allo stesso gruppo.

Per impostazione predefinita, un'applicazione è vincolata a un singolo gruppo, che deve offrire un'ampio livello di funzionalità di elaborazione per l'applicazione tipica. Il sistema operativo assegna inizialmente ogni processo a un singolo gruppo in modo round robin tra i gruppi nel sistema. Un processo inizia l'esecuzione assegnata a un gruppo. Il primo thread di un processo viene eseguito inizialmente nel gruppo a cui è assegnato il processo. Ogni thread appena creato viene assegnato allo stesso gruppo del thread che lo ha creato.

Un'applicazione che richiede l'uso di più gruppi in modo che possa essere eseguita su più di 64 processori deve determinare in modo esplicito dove eseguire i thread ed è responsabile dell'impostazione delle affinità del processore dei thread sui gruppi desiderati. Il flag [INHERIT \_ PARENT \_ AFFINITY](process-creation-flags.md) può essere usato per specificare un processo padre (che può essere diverso dal processo corrente) da cui generare l'affinità per un nuovo processo. Se il processo è in esecuzione in un singolo gruppo, può leggerne e modificarne l'affinità usando [**GetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-getprocessaffinitymask) e [**SetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask) rimanendo nello stesso gruppo; se l'affinità di processo viene modificata, la nuova affinità viene applicata ai relativi thread.

L'affinità di un thread può essere specificata durante la creazione usando l'attributo esteso [**PROC THREAD ATTRIBUTE GROUP \_ \_ \_ \_ AFFINITY**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-updateprocthreadattribute) con [**la funzione CreateRemoteThreadEx.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethreadex) Dopo aver creato il thread, è possibile modificarne l'affinità chiamando [**SetThreadAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setthreadaffinitymask) o [**SetThreadGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-setthreadgroupaffinity). Se un thread viene assegnato a un gruppo diverso dal processo, l'affinità del processo viene aggiornata in modo da includere l'affinità del thread e il processo diventa un processo a più gruppi. È necessario apportare altre modifiche all'affinità per i singoli thread. Non è possibile modificare l'affinità di un processo multi-gruppo usando [**SetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask). La [**funzione GetProcessGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-getprocessgroupaffinity) recupera il set di gruppi a cui sono assegnati un processo e i relativi thread.

Per specificare l'affinità per tutti i processi associati a un oggetto processo, usare la [**funzione SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) con la classe di informazioni **JobObjectGroupInformation** o **JobObjectGroupInformationEx.**

Un processore logico è identificato dal numero di gruppo e dal relativo numero di processore relativo al gruppo. È rappresentato da una struttura [**PROCESSOR \_ NUMBER.**](/windows/desktop/api/WinNT/ns-winnt-processor_number) I numeri numerici del processore usati dalle funzioni legacy sono relativi al gruppo.

Per una descrizione delle modifiche all'architettura del sistema operativo per supportare più di 64 processori, vedere white paper Sistemi di supporto con più di [64 processori](https://www.microsoft.com/whdc/system/Sysinternals/MoreThan64proc.mspx).

Per un elenco di nuove funzioni e strutture che supportano i gruppi di processori, vedere [Novità di processi e thread](what-s-new-in-processes-and-threads.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Processori multipli](multiple-processors.md)
</dt> <dt>

[Supporto NUMA](numa-support.md)
</dt> </dl>

 

 
