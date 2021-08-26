---
description: Un'applicazione può usare processi annidati per gestire subset di processi. I processi annidati consentono anche a un'applicazione che usa processi per ospitare altre applicazioni che usano anche processi.
ms.assetid: FA22493B-CD29-49A7-BDAC-349FA96B8C9E
title: Processi annidati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fba0a517b71cdc01ec701a4a8f6a4f272f039797c140333e64ecad5532aca23f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032212"
---
# <a name="nested-jobs"></a>Processi annidati

Un'applicazione può usare processi annidati per gestire subset di processi. I processi annidati consentono anche a un'applicazione che usa processi per ospitare altre applicazioni che usano anche processi.

**Windows 7, Windows Server 2008 R2, Windows XP con SP3, Windows Server 2008, Windows Vista e Windows Server 2003:** Un processo può essere associato a un solo processo. I processi annidati sono stati introdotti Windows 8 e Windows Server 2012.

Questo argomento offre una panoramica dell'annidamento dei processi e del comportamento dei processi annidati:

-   [Gerarchie di processi annidati](#nested-job-hierarchies)
-   [Creazione di una gerarchia di processi annidati](#creating-a-nested-job-hierarchy)
-   [Limiti e notifiche dei processi annidati](#job-limits-and-notifications-for-nested-jobs)
-   [Contabilità delle risorse per i processi annidati](#resource-accounting-for-nested-jobs)
-   [Terminazione di processi annidati](#termination-of-nested-jobs)

Per informazioni generali sui processi e sugli oggetti processo, vedere [Oggetti processo](job-objects.md).

## <a name="nested-job-hierarchies"></a>Gerarchie di processi annidati

I processi annidati hanno una relazione padre-figlio in cui ogni processo figlio contiene un subset dei processi nel processo padre. Se un processo già presente in un processo viene aggiunto a un altro processo, i processi vengono annidati per impostazione predefinita se il sistema può formare una gerarchia di processi valida e nessuno dei due processi imposta limiti dell'interfaccia utente ([**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) con **JobObjectBasicUIRestrictions**).

La figura 1 mostra una gerarchia di processi che contiene un albero di processi etichettati da P0 a P7. Il processo 1 è *il processo padre* del processo 2 e del processo 4 ed è un *predecessore* del processo 3. Il processo 2 è *l'elemento padre* immediato del processo 3. Il processo 3 è *l'elemento figlio immediato* del processo 2. I processi 1, 2 e 3 formano una *catena* di processi in cui i processi 1 e 2 sono la catena di processi *padre* del processo 3. Il processo finale in una catena di processi è *il* processo immediato dei processi in tale processo. Nella figura 1 il processo 3 è il processo immediato dei processi P2, P3 e P4.

![figura 1. gerarchia di processi annidata che contiene un albero dei processi](images/nested-jobs-a.png)

I processi annidati possono essere usati anche per gestire gruppi di processi peer. Nella gerarchia dei processi illustrata nella figura 2, il processo 1 è il processo padre del processo 2. Si noti che una gerarchia di processi può contenere solo una parte di un albero dei processi. Nella figura 2, P0 non si trova nella gerarchia, ma i processi figlio da P1 a P5 lo sono.

![figura 2. gerarchia di processi annidata che contiene processi peer](images/nested-jobs-b.png)

## <a name="creating-a-nested-job-hierarchy"></a>Creazione di una gerarchia di processi annidati

I processi in una gerarchia di processi vengono associati in modo esplicito a un oggetto processo usando la [**funzione AssignProcessToJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject) o associati in modo implicito durante la creazione del processo, come per i processi autonomi. L'ordine in cui vengono creati i processi e i processi assegnati determinano se è possibile creare una gerarchia.

Per compilare una gerarchia di processi usando l'associazione esplicita, tutti gli oggetti processo devono essere creati usando [**CreateJobObject,**](/windows/desktop/api/WinBase/nf-winbase-createjobobjecta)quindi [**AssignProcessToJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject) deve essere chiamato più volte per ogni processo per associare il processo a ogni processo a cui deve appartenere. Per assicurarsi che la gerarchia dei processi sia valida, assegnare prima tutti i processi al processo nella radice della gerarchia, quindi assegnare un subset di processi all'oggetto processo figlio immediato e così via. Se i processi vengono assegnati ai processi in questo ordine, un processo figlio avrà sempre un subset di processi nel processo padre durante la creazione della gerarchia, necessaria per l'annidamento. Se i processi vengono assegnati ai processi in ordine casuale, a un certo punto un processo figlio avrà processi non presenti nel processo padre. Questa operazione non è consentita dall'annidamento e causerà l'esito negativo di **AssignProcessToJobObject.**

Quando i processi vengono associati in modo implicito a un processo durante la creazione del processo, un processo figlio viene associato a ogni processo nella catena di processi del processo padre. Se l'oggetto processo immediato consente la breakaway, il processo figlio si interrompe dall'oggetto processo immediato e da ogni processo nella catena di processi padre, spostando verso l'alto la gerarchia fino a raggiungere un processo che non consente la breakaway. Se l'oggetto processo immediato non consente la breakaway, il processo figlio non si interrompe anche se i processi nella catena di processi padre lo consentono.

## <a name="job-limits-and-notifications-for-nested-jobs"></a>Limiti e notifiche dei processi annidati

Per determinati limiti di risorse, il limite impostato  per i processi in una catena di processi padre determina il limite effettivo applicato per un processo figlio. Il limite effettivo per il processo figlio può essere più restrittivo rispetto al limite del relativo processo padre, ma non può essere meno restrittivo. Ad esempio, se la classe di priorità di un processo figlio è ABOVE NORMAL PRIORITY CLASS e la classe di priorità del processo padre è NORMAL PRIORITY CLASS, il limite effettivo per i processi nel processo figlio \_ \_ è NORMAL PRIORITY \_ \_ \_ \_ \_ CLASS. Tuttavia, se la classe di priorità del processo figlio è BELOW NORMAL PRIORITY CLASS, il limite effettivo per i processi nel processo figlio \_ è BELOW NORMAL PRIORITY \_ \_ \_ \_ \_ CLASS. I limiti effettivi vengono applicati per la classe di priorità, l'affinità, l'addebito del commit, il limite di tempo di esecuzione per processo, il limite di classe di pianificazione e working set minimo e massimo. Per altre informazioni sui limiti specifici delle risorse, vedere [ **SetInformationJobObject.**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject)

Quando si verificano determinati eventi, ad esempio la creazione di un nuovo processo o la violazione del limite di risorse, viene inviato un messaggio alla porta di completamento I/O associata a un processo. Un processo può anche registrarsi per ricevere notifiche quando vengono superati determinati limiti. Per un processo non annidato, il messaggio viene inviato alla porta di completamento I/O associata al processo. Per un processo annidato, il messaggio viene inviato a ogni porta di completamento I/O associata a qualsiasi processo nella catena di processi padre del processo che ha attivato il messaggio. Non è necessario che a un processo figlio sia associata una porta di completamento I/O per i messaggi attivati da inviare alle porte di completamento I/O dei processi padre più in alto nella catena di processi. Per altre informazioni su messaggi specifici, vedere [**JOBOBJECT \_ ASSOCIATE COMPLETION \_ \_ PORT**](/windows/desktop/api/WinNT/ns-winnt-jobobject_associate_completion_port).

## <a name="resource-accounting-for-nested-jobs"></a>Contabilità delle risorse per i processi annidati

Le informazioni di contabilità delle risorse per un processo annidato descrivono l'utilizzo di ogni processo associato a tale processo, inclusi i processi nei processi figlio. Ogni processo in una catena di processi rappresenta quindi le risorse aggregate usate dai propri processi e i processi di ogni processo figlio sottostante nella catena di processi.

## <a name="termination-of-nested-jobs"></a>Terminazione di processi annidati

Quando un processo in una gerarchia di processi viene terminato, il sistema termina i processi in tale processo e in tutti i relativi processi figlio, a partire dal processo figlio nella parte inferiore della gerarchia. Le risorse in sospeso usate da ogni processo terminato vengono addebitate al processo padre.

L'handle del processo deve avere il diritto di accesso JOB \_ OBJECT \_ TERMINATE, come per i processi autonomi.

 

 
