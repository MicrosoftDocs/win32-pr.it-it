---
description: Oltre alle partizioni, che contengono una o più applicazioni, COM+ include anche set di partizioni, che contengono una o più partizioni.
ms.assetid: 0b1a6daa-55e1-4a74-be01-e39473e3c0cc
title: Partizioni e Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b08e7b70c4b474e7b7bd949f530fb73973d39c6a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304815"
---
# <a name="partitions-and-active-directory"></a>Partizioni e Active Directory

Oltre alle partizioni, che contengono una o più applicazioni, COM+ include anche *set* di partizioni, che contengono una o più partizioni. Creati in Active Directory, i set di partizioni consentono agli utenti di un dominio di accedere alle applicazioni COM+ in tutto il dominio. Durante la creazione, ogni utente specifico o unità organizzativa (OU) viene assegnato o mappato a un set di partizioni.

Un singolo utente o unità organizzativa può accedere a più partizioni e alle relative applicazioni perché esiste una correlazione uno-a-uno tra un'identità utente o un'unità organizzativa e un set di partizioni. Senza un set di partizioni, un utente o un'unità organizzativa dovrebbe avere più identità utente per accedere alle applicazioni in partizioni diverse.

Per rendere le applicazioni COM+ disponibili per gli utenti di dominio, un amministratore deve eseguire le attività sia sul controller di dominio in cui risiede Active Directory che sul server in cui è installata l'applicazione COM+.

## <a name="on-the-domain-controller"></a>Nel controller di dominio

L'amministratore crea innanzitutto una partizione all'interno Active Directory. La creazione di una partizione COM+ viene eseguita tramite l'utilizzo dello strumento di amministrazione Active Directory utenti e computer oppure a livello di codice tramite l'interfaccia ADSI (Active Directory Services Interface).

Dopo la creazione della partizione all'interno di Active Directory, l'amministratore crea quindi un set di partizioni. Durante la creazione di un set di partizioni, l'amministratore definisce le partizioni incluse nel set. La creazione di un set di partizioni COM+ viene eseguita tramite l'utilizzo dello strumento di amministrazione Active Directory utenti e computer oppure a livello di codice tramite l'interfaccia ADSI (Active Directory Services Interface).

Infine, l'amministratore esegue il mapping di utenti di dominio o unità organizzative (OU) al set di partizioni appena creato. Questa operazione viene eseguita visualizzando la pagina delle **Proprietà** di un utente, accedendo alla scheda **set di partizioni com+** e selezionando un set di partizioni dalla casella di riepilogo.

## <a name="on-the-com-application-server"></a>Sul server applicazioni COM+

L'amministratore crea una nuova partizione, specificando lo stesso nome di partizione e ID di partizione (GUID) della partizione creata all'interno Active Directory nel controller di dominio. Questa operazione viene eseguita utilizzando la cartella **partizioni com+** nello strumento di amministrazione Servizi componenti. Per semplificare questa attività, lo strumento Servizi componenti consente all'amministratore di esplorare Active Directory per selezionare la partizione desiderata e il relativo GUID.

Quando la partizione di dominio è stata creata nel server applicazioni, la partizione predefinita di un utente diventa la partizione predefinita del set di partizioni nella Active Directory. Infine, l'amministratore può installare l'applicazione COM+ nella partizione appena creata nel server applicazioni.

Per ulteriori informazioni sull'amministrazione delle partizioni per l'accesso da parte degli utenti di dominio, vedere la Guida associata allo strumento di amministrazione Active Directory utenti e computer.

## <a name="mapping-user-identities-and-ous-to-partition-sets"></a>Mapping di identità utente e unità organizzative a set di partizioni

È possibile eseguire il mapping di utenti e ou a un set di partizioni. Eseguendo il mapping di unità organizzative a set di partizioni, un amministratore può associare più utenti a un set di partizioni in una sola volta anziché dover eseguire il mapping di più identità utente. È possibile eseguire il mapping di una singola identità utente o unità organizzativa a un solo set di partizioni. In generale, il mapping di identità utente o unità organizzative a set di partizioni esegue le operazioni seguenti:

-   Garantisce che le applicazioni siano disponibili per gli utenti appropriati nel dominio
-   Consente a COM+ di determinare la partizione in cui si trova un'applicazione
-   Stabilisce il diritto di un utente di accedere a un'applicazione specifica

Per associare partizioni a set di partizioni all'interno Active Directory e per eseguire il mapping di utenti e unità organizzative a tali set di partizioni, gli amministratori utilizzano gli strumenti di amministrazione Active Directory utenti e computer e Servizi componenti. Quando viene creata una partizione all'interno Active Directory, un amministratore deve configurare localmente tale partizione nel computer in cui deve essere installata l'applicazione COM+ pertinente. Questa configurazione locale delle partizioni create all'interno Active Directory viene eseguita tramite lo strumento di amministrazione Servizi componenti.

Se non è stato eseguito il mapping di un'identità utente di dominio a un set di partizioni, all'utente viene concesso l'accesso da parte dell'unità organizzativa dell'utente, mappata alla partizione. Se l'unità organizzativa dell'utente non è mappata a un set di partizioni ma viene eseguito il mapping dell'unità organizzativa successiva più alta nella gerarchia a tale set di partizioni, l'utente potrà accedere alla partizione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Partizioni predefinite](default-partitions.md)
</dt> <dt>

[Partizioni locali](local-partitions.md)
</dt> <dt>

[Proprietà partizione](partition-properties.md)
</dt> <dt>

[Partizione globale](the-global-partition.md)
</dt> </dl>

 

 



