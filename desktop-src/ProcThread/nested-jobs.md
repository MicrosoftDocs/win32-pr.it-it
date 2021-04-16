---
description: Un'applicazione può utilizzare processi annidati per gestire subset di processi. I processi annidati consentono anche a un'applicazione che usa processi di ospitare altre applicazioni che usano anche i processi.
ms.assetid: FA22493B-CD29-49A7-BDAC-349FA96B8C9E
title: Processi annidati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abf105c70ec8e83b395fcce56c6274d4838358bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104557834"
---
# <a name="nested-jobs"></a>Processi annidati

Un'applicazione può utilizzare processi annidati per gestire subset di processi. I processi annidati consentono anche a un'applicazione che usa processi di ospitare altre applicazioni che usano anche i processi.

**Windows 7, Windows server 2008 R2, Windows XP con SP3, Windows server 2008, Windows Vista e Windows server 2003:** Un processo può essere associato a un singolo processo. I processi annidati sono stati introdotti in Windows 8 e Windows Server 2012.

Questo argomento fornisce una panoramica dell'annidamento dei processi e del comportamento dei processi annidati:

-   [Gerarchie di processi annidate](#nested-job-hierarchies)
-   [Creazione di una gerarchia di processi annidati](#creating-a-nested-job-hierarchy)
-   [Limiti e notifiche dei processi annidati](#job-limits-and-notifications-for-nested-jobs)
-   [Contabilità delle risorse per i processi annidati](#resource-accounting-for-nested-jobs)
-   [Terminazione dei processi annidati](#termination-of-nested-jobs)

Per informazioni generali sui processi e sugli oggetti processo, vedere [oggetti processo](job-objects.md).

## <a name="nested-job-hierarchies"></a>Gerarchie di processi annidate

I processi annidati hanno una relazione padre-figlio in cui ogni processo figlio contiene un subset dei processi nel processo padre. Se un processo che si trova già in un processo viene aggiunto a un altro processo, i processi sono annidati per impostazione predefinita se il sistema può formare una gerarchia di processi valida e nessuno dei due imposta i limiti dell'interfaccia utente ([**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) con **JobObjectBasicUIRestrictions**).

Nella figura 1 viene illustrata una gerarchia di processi che contiene una struttura ad albero di processi con etichetta P0-P7. Il processo 1 è il processo *padre* del processo 2 e il processo 4 ed è un *predecessore* del processo 3. Il processo 2 è l' *elemento padre diretto* del processo 3. Il processo 3 è l' *elemento figlio immediato* del processo 2. I processi 1, 2 e 3 formano una *catena* di processi in cui i processi 1 e 2 sono la catena di processi *padre* del processo 3. Il processo finale in una catena di processi è il *processo immediato* dei processi in tale processo. Nella figura 1, il processo 3 è il processo immediato dei processi P2, P3 e P4.

![Figura 1. una gerarchia di processi annidata che contiene un albero del processo](images/nested-jobs-a.png)

I processi annidati possono essere usati anche per gestire i gruppi di processi peer. Nella gerarchia dei processi illustrata nella figura 2, il processo 1 è il processo padre del processo 2. Si noti che una gerarchia di processi potrebbe contenere solo parte di un albero di processi. Nella figura 2, P0 non si trova nella gerarchia, ma i processi figlio da P1 a P5 sono.

![Figura 2. gerarchia di processi annidati che contiene processi peer](images/nested-jobs-b.png)

## <a name="creating-a-nested-job-hierarchy"></a>Creazione di una gerarchia di processi annidati

I processi in una gerarchia di processi sono associati in modo esplicito a un oggetto processo tramite la funzione [**AssignProcessToJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject) o associati in modo implicito durante la creazione del processo, come per i processi autonomi. L'ordine in cui vengono creati i processi e vengono assegnati i processi determina se è possibile creare una gerarchia.

Per compilare una gerarchia di processi utilizzando un'associazione esplicita, tutti gli oggetti processo devono essere creati utilizzando [**CreateJobObject**](/windows/desktop/api/WinBase/nf-winbase-createjobobjecta), quindi [**AssignProcessToJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject) deve essere chiamato più volte per ogni processo per associare il processo a ogni processo a cui deve appartenere. Per assicurarsi che la gerarchia processi sia valida, assegnare prima tutti i processi al processo alla radice della gerarchia, quindi assegnare un subset di processi all'oggetto processo figlio immediato e così via. Se i processi vengono assegnati ai processi in questo ordine, un processo figlio disporrà sempre di un subset di processi nel processo padre durante la creazione della gerarchia, necessaria per l'annidamento. Se i processi vengono assegnati ai processi in ordine casuale, a un certo punto un processo figlio avrà processi non inclusi nel processo padre. Questa operazione non è consentita dall'annidamento e causerà l'esito negativo di **AssignProcessToJobObject** .

Quando i processi sono associati in modo implicito a un processo durante la creazione del processo, un processo figlio viene associato a ogni processo nella catena di processi del processo padre. Se l'oggetto processo immediato consente la separazione, il processo figlio si interrompe dall'oggetto processo immediato e da ogni processo nella catena di processi padre, spostandolo fino a raggiungere un processo che non consente la separazione. Se l'oggetto processo immediato non consente la fuga, il processo figlio non si interrompe neanche se i processi nella catena di processi padre lo consentono.

## <a name="job-limits-and-notifications-for-nested-jobs"></a>Limiti e notifiche dei processi annidati

Per determinati limiti di risorse, il limite impostato per i processi in una catena di processi padre determina il *limite effettivo* applicato per un processo figlio. Il limite effettivo per il processo figlio può essere più restrittivo rispetto al limite del padre, ma non può essere meno restrittivo. Se, ad esempio, la classe di priorità di un processo figlio è al di sopra della classe di priorità normale \_ \_ \_ e la classe di priorità del processo padre è la classe di priorità normale \_ \_ , il limite effettivo per i processi nel processo figlio è la \_ classe di priorità normale \_ . Tuttavia, se la classe di priorità del processo figlio è inferiore alla \_ \_ classe di priorità normale \_ , il limite effettivo per i processi nel processo figlio è inferiore alla \_ classe di priorità normale \_ \_ . I limiti effettivi vengono applicati per la classe di priorità, l'affinità, l'addebito del commit, il limite di tempo di esecuzione per processo, il limite della classe di pianificazione e working set minimo e massimo. Per ulteriori informazioni sui limiti di risorse specifici, vedere [ **SetInformationJobObject.**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject)

Quando si verificano determinati eventi, ad esempio la creazione di nuovi processi o la violazione del limite di risorse, viene inviato un messaggio alla porta di completamento I/O associata a un processo. Un processo può inoltre registrarsi per ricevere notifiche quando vengono superati determinati limiti. Per un processo non annidato, il messaggio viene inviato alla porta di completamento I/O associata al processo. Per un processo annidato, il messaggio viene inviato a tutte le porte di completamento I/O associate a qualsiasi processo nella catena di processi padre del processo che ha attivato il messaggio. Un processo figlio non deve necessariamente disporre di una porta di completamento di I/O associata per i messaggi da esso inviati alle porte di completamento I/O dei processi padre più in alto nella catena di processi. Per ulteriori informazioni su messaggi specifici, vedere la pagina relativa alla [**\_ \_ \_ porta di completamento associata JOBOBJECT**](/windows/desktop/api/WinNT/ns-winnt-jobobject_associate_completion_port).

## <a name="resource-accounting-for-nested-jobs"></a>Contabilità delle risorse per i processi annidati

Le informazioni sull'accounting delle risorse per un processo annidato descrivono l'utilizzo di ogni processo associato a tale processo, inclusi i processi nei processi figlio. Ogni processo in una catena di processi rappresenta quindi le risorse aggregate utilizzate dai rispettivi processi e i processi di ogni processo figlio sotto di esso nella catena di processi.

## <a name="termination-of-nested-jobs"></a>Terminazione dei processi annidati

Quando un processo in una gerarchia di processi viene terminato, il sistema termina i processi del processo e di tutti i relativi processi figlio, a partire dal processo figlio nella parte inferiore della gerarchia. Le risorse in attesa utilizzate da ogni processo terminato vengono addebitate al processo padre.

L'handle di processo deve avere l' \_ oggetto processo \_ Termina accesso a destra, come per i processi autonomi.

 

 
