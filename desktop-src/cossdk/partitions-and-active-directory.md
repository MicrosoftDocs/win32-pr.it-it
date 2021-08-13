---
description: Oltre alle partizioni, che contengono una o più applicazioni, COM+ include anche set di partizioni che contengono una o più partizioni.
ms.assetid: 0b1a6daa-55e1-4a74-be01-e39473e3c0cc
title: Partizioni e Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 144dde53c6247dcf09dbf9540ce535afb12725822b8e9895f7eb33b569135089
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462141"
---
# <a name="partitions-and-active-directory"></a>Partizioni e Active Directory

Oltre alle partizioni, che contengono una o più applicazioni, COM+ include anche set di *partizioni*, che contengono una o più partizioni. Creati in Active Directory, i set di partizioni consentono agli utenti di un dominio di accedere alle applicazioni COM+ in tutto il dominio. Durante la creazione, ogni utente o unità organizzativa specifica viene assegnato o mappato a un set di partizioni.

Un singolo utente o unità organizzativa può accedere a più partizioni e alle relative applicazioni perché esiste una correlazione uno-a-uno tra un'identità utente o un'unità organizzativa e un set di partizioni. Senza un set di partizioni, un utente o un'unità organizzativa avrebbe bisogno di più identità utente per accedere alle applicazioni in partizioni diverse.

Per rendere le applicazioni COM+ disponibili per gli utenti di dominio, un amministratore deve eseguire attività sia nel controller di dominio in cui risiede Active Directory che nel server in cui è installata l'applicazione COM+.

## <a name="on-the-domain-controller"></a>Nel controller di dominio

L'amministratore crea prima una partizione all'interno di Active Directory. La creazione di una partizione COM+ viene eseguita tramite l'uso dello strumento amministrativo Utenti e computer di Active Directory o a livello di codice tramite Active Directory Services Interface (ADSI).

Dopo aver creato la partizione in Active Directory, l'amministratore crea un set di partizioni. Nella creazione di un set di partizioni, l'amministratore definisce le partizioni incluse in tale set. La creazione di un set di partizioni COM+ viene eseguita tramite l'uso dello strumento amministrativo Utenti e computer di Active Directory o a livello di codice tramite l'interfaccia ADSI (Active Directory Services Interface).

Infine, l'amministratore esegue il mapping di utenti di dominio o unità organizzative (OU) al set di partizioni appena creato. Questa operazione viene eseguita visualizzando  la pagina Proprietà di un utente, accedendo alla scheda Set di partizioni **COM+** e selezionando un set di partizioni dalla casella di riepilogo.

## <a name="on-the-com-application-server"></a>Nel server applicazioni COM+

L'amministratore crea una nuova partizione, specificando lo stesso nome della partizione e lo stesso ID di partizione (GUID) della partizione creata in Active Directory nel controller di dominio. Questa operazione viene eseguita usando la **cartella Partizioni COM+ all'interno** dello strumento amministrativo Servizi componenti. Per semplificare questa attività, lo strumento Servizi componenti consente all'amministratore di esplorare Active Directory per selezionare la partizione desiderata e il relativo GUID.

Dopo la creazione della partizione di dominio nel server applicazioni, la partizione predefinita di un utente diventa la partizione predefinita del set di partizioni in Active Directory. Infine, l'amministratore può installare l'applicazione COM+ nella partizione appena creata nel server applicazioni.

Per altre informazioni sull'amministrazione delle partizioni per l'accesso da parte degli utenti di dominio, vedere la Guida associata allo strumento Utenti e computer di Active Directory amministrativo.

## <a name="mapping-user-identities-and-ous-to-partition-sets"></a>Mapping di identità utente e unità organizzative a set di partizioni

È possibile eseguire il mapping di utenti e unità organizzative a set di partizioni. Mappando le unità organizzative ai set di partizioni, un amministratore può associare più utenti a un set di partizioni contemporaneamente anziché dover eseguire il mapping di più identità utente. È possibile eseguire il mapping di una singola identità utente o unità organizzativa a un solo set di partizioni. In generale, il mapping delle identità utente o delle unità organizzative ai set di partizioni esegue le operazioni seguenti:

-   Garantisce che le applicazioni siano disponibili per gli utenti appropriati nel dominio
-   Consente a COM+ di determinare la partizione in cui si trova un'applicazione
-   Stabilisce il diritto di un utente di accedere a una determinata applicazione

Per associare partizioni a set di partizioni all'interno di Active Directory e per eseguire il mapping di utenti e unità organizzative a tali set di partizioni, gli amministratori usano gli strumenti di amministrazione Utenti e computer di Active Directory e Servizi componenti. Quando viene creata una partizione all'interno di Active Directory, un amministratore deve configurare localmente la partizione nel computer in cui deve essere installata l'applicazione COM+ pertinente. Questa configurazione locale delle partizioni create all'interno di Active Directory viene eseguita tramite lo strumento amministrativo Servizi componenti.

Se non è stato eseguito il mapping di un'identità utente di dominio a un set di partizioni, all'utente viene concesso l'accesso dall'unità organizzativa dell'utente, di cui è stato eseguito il mapping alla partizione. Se l'unità organizzativa dell'utente non è mappata a un set di partizioni, ma la successiva unità organizzativa più alta nella gerarchia viene mappata a tale set di partizioni, l'utente può accedere alla partizione.

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

 

 



