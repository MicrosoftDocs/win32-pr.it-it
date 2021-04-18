---
description: Il servizio di strumentazione COM+ consente di creare programmi di registrazione e gestione degli eventi COM+ personalizzati quando si desidera visualizzare diverse metriche delle prestazioni per i componenti COM+.
ms.assetid: 07f68734-a382-4fe5-86af-90805f61c68d
title: Concetti relativi alla strumentazione COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d86b5dbb7bb3f6db14d82220d88c58dbc0a8255
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304736"
---
# <a name="com-instrumentation-concepts"></a>Concetti relativi alla strumentazione COM+

Il servizio di strumentazione COM+ consente di creare programmi di registrazione e gestione degli eventi COM+ personalizzati quando si desidera visualizzare diverse metriche delle prestazioni per i componenti COM+. La strumentazione COM+ può essere utilizzata anche per configurare gli eventi definiti dall'utente e per convertire gli eventi COM+ nel formato Visual Studio Analyzer (VSA) quando si esegue l'aggiornamento di pacchetti MTS che ricevono eventi MTS.

> [!Note]  
> A partire da Windows Server 2003, solo gli amministratori dispongono di privilegi di accesso in lettura ai registri di traccia per gli eventi di sistema.

 

Sottoscrivendo gli eventi pubblicati dal server di pubblicazione degli eventi di sistema, i client possono implementare le [interfacce di strumentazione com+](com--instrumentation-interfaces.md) per ricevere notifiche per un'ampia gamma di metriche delle prestazioni com+, ad esempio informazioni su oggetti COM+ specifici, applicazioni com+ e servizi com+. Le metriche vengono pubblicate nel client usando il [servizio eventi com+](com--events.md), un sistema di eventi a regime di controllo libero (LCE) che archivia le informazioni sugli eventi da autori diversi in un archivio eventi nel catalogo com+.

> [!Note]  
> La strumentazione COM+ non garantisce il recapito di un evento.

 

Ogni metrica ha un timestamp che indica l'ora in cui è stata generata la metrica, non l'ora in cui è stato inviato o ricevuto. Il client può correlare il timestamp e individuare il costo di esecuzione di un'applicazione COM+, il costo di una transazione eseguita all'interno di un'applicazione COM+ o il costo di una chiamata al metodo all'interno di un'applicazione COM+.

È inoltre possibile utilizzare il servizio di strumentazione COM+ per filtrare le specifiche informazioni sulle metriche delle prestazioni che si desidera visualizzare. Ad esempio, quando si sottoscrive un'interfaccia o un metodo di strumentazione COM+, è possibile specificare le proprietà per la sottoscrizione nella struttura [**COMSVCSEVENTINFO**](/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo) , ad esempio l'ID applicazione (membro **guidApp** ) o l'ID processo (membro **dwPid** ).

Quando si specifica l'ID applicazione, si ricevono solo le metriche dell'applicazione specificata. Quando viene specificato l'ID processo, vengono ricevute le metriche dell'applicazione server e delle applicazioni di libreria specificate caricate in tale processo. L'utente può specificare l'ID dell'applicazione e l'ID del processo, ma l'ID applicazione deve essere quello dell'applicazione server in esecuzione nel processo con l'ID di processo specificato. Se non si specifica nessuno, l'utente riceve le metriche da tutte le applicazioni server e di libreria.

Le metriche di strumentazione COM+ forniscono informazioni sufficienti per consentire all'applicazione di monitoraggio di metterle in correlazione con le metriche del sistema operativo per l'analisi delle prestazioni, la pianificazione della capacità e la modellazione e la stima.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfacce di strumentazione COM+](com--instrumentation-interfaces.md)
</dt> </dl>

 

 



