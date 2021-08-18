---
description: Il servizio di strumentazione COM+ consente di creare programmi di registrazione e gestione degli eventi COM+ quando si vogliono visualizzare diverse metriche delle prestazioni per i componenti COM+.
ms.assetid: 07f68734-a382-4fe5-86af-90805f61c68d
title: Concetti relativi alla strumentazione COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 160a546c07ea4204f1f4da3ba4c56c76a6eed6b52a8d397d470d0bc34b76adc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118549507"
---
# <a name="com-instrumentation-concepts"></a>Concetti relativi alla strumentazione COM+

Il servizio di strumentazione COM+ consente di creare programmi di registrazione e gestione degli eventi COM+ quando si vogliono visualizzare diverse metriche delle prestazioni per i componenti COM+. La strumentazione COM+ può essere usata anche per configurare eventi definiti dall'utente e convertire eventi COM+ in formato Visual Studio Analyzer (VSA) quando si aggiornano pacchetti MTS che ricevono eventi MTS.

> [!Note]  
> A Windows Server 2003, solo gli amministratori hanno privilegi di accesso in lettura ai log di traccia per gli eventi di sistema.

 

Sottoscrivendo gli eventi pubblicati dall'autore degli eventi di sistema, i client possono implementare le interfacce di strumentazione [COM+](com--instrumentation-interfaces.md) per ricevere notifiche per un'ampia gamma di metriche delle prestazioni COM+, ad esempio informazioni su oggetti COM+, applicazioni COM+ e servizi COM+ specifici. Le metriche vengono pubblicate nel client usando il servizio eventi [COM+,](com--events.md)un sistema di eventi ad accoppiato libero (LCE) che archivia le informazioni sugli eventi di diversi editori in un archivio eventi nel catalogo COM+.

> [!Note]  
> La strumentazione COM+ non garantisce il recapito di un evento.

 

Ogni metrica ha un timestamp che indica l'ora in cui è stata generata la metrica, non l'ora in cui è stata inviata o ricevuta. Il client può correlare il timestamp e scoprire il costo dell'esecuzione di un'applicazione COM+, il costo di una transazione eseguita all'interno di un'applicazione COM+ o il costo di una chiamata al metodo all'interno di un'applicazione COM+.

È anche possibile usare il servizio strumentazione COM+ per filtrare le informazioni specifiche sulle metriche delle prestazioni che si desidera visualizzare. Ad esempio, quando si sottoscrive un metodo o un'interfaccia di strumentazione COM+, è possibile specificare le proprietà per la sottoscrizione nella struttura [**COMSVCSEVENTINFO,**](/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo) ad esempio l'ID applicazione (membro **guidApp)** o l'ID processo (membro **dwPid).**

Quando viene specificato l'ID applicazione, si ricevono solo le metriche dall'applicazione specificata. Quando viene specificato l'ID processo, si ricevono le metriche dall'applicazione server e dalle applicazioni di libreria specificate caricate in tale processo. L'utente può specificare sia l'ID applicazione che l'ID processo, ma l'ID applicazione deve essere quello dell'applicazione server in esecuzione nel processo con l'ID processo specificato. Se non viene specificato nessuno dei due, l'utente riceve le metriche da tutte le applicazioni server e libreria.

Le metriche di strumentazione COM+ forniscono informazioni sufficienti per l'applicazione di monitoraggio per correlarle con le metriche del sistema operativo per l'analisi delle prestazioni, la pianificazione della capacità e per la modellazione e la stima.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfacce di strumentazione COM+](com--instrumentation-interfaces.md)
</dt> </dl>

 

 



