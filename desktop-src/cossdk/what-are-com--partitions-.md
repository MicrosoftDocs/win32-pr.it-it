---
description: Una partizione COM+ è un contenitore logico che consente l'esecuzione delle applicazioni indipendentemente da altre configurazioni di tali applicazioni.
ms.assetid: c1290d10-968f-44f0-8099-d69c9e706c9e
title: Che cosa sono le partizioni COM+?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edc678089948770181d98af065afa414741055062ed2e942215de5d7cb8bc7b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070266"
---
# <a name="what-are-com-partitions"></a>Che cosa sono le partizioni COM+?

Una partizione COM+ è un contenitore logico che consente l'esecuzione delle applicazioni indipendentemente da altre configurazioni di tali applicazioni. Ogni configurazione di un'applicazione viene installata in una partizione separata e può essere gestita separatamente, in base alle esigenze specifiche degli utenti.

Durante l'attivazione di un componente COM+, il servizio partizioni determina la configurazione del componente da attivare, in base all'identità dell'utente che richiede l'attivazione del componente. Ad esempio, una singola organizzazione con due gruppi separati, Production e Training, potrebbe implementare partizioni COM+ per consentire ai due gruppi di usare configurazioni diverse di un'applicazione COM+ nello stesso computer.

**Windows XP:** La possibilità di creare, configurare o delegare partizioni COM+ non è disponibile. La partizione globale è l'unica partizione COM+ disponibile.

**Windows 2000:** Il servizio partizioni COM+ non è disponibile in Windows 2000.

## <a name="benefits-of-using-com-partitions"></a>Vantaggi dell'uso di partizioni COM+

L'uso di partizioni COM+ offre diversi vantaggi, tra cui i seguenti:

-   Le organizzazioni possono ridurre il costo totale di proprietà (TCO) usando meno server applicazioni fisici per supportare gli utenti che necessitano di più configurazioni dell'applicazione.
-   Il sovraccarico amministrativo è ridotto. Invece di dover configurare e gestire più computer, gli amministratori devono solo configurare e gestire più partizioni nello stesso computer. Inoltre, le partizioni possono essere gestite a livello di codice tramite l'aggiunta di una nuova interfaccia di programmazione COM+.
-   La sicurezza può essere implementata e gestita partizione per partizione per utenti locali, utenti di dominio e unità organizzative.
-   I programmatori e gli amministratori possono usare gli strumenti di sviluppo e amministrazione di Microsoft, ad esempio Windows SDK, Utenti e computer di Active Directory e lo strumento amministrativo Servizi componenti, per gestire le partizioni COM+. La funzionalità partizioni è completamente integrata in questi strumenti.

## <a name="primary-usage-scenario"></a>Scenario di utilizzo primario

Uno dei motivi principali per cui i clienti distribuiscono la funzionalità partizioni COM+ è l'hosting di applicazioni basate sul Web. Si supponga, ad esempio, che una piccola società di software sviluppi un'applicazione COM+ per l'uso da parte del personale ospedaliero. L'applicazione, che è un'applicazione distribuita basata sul Web, consente agli ospedali di archiviare e recuperare le cartelle sanitarie dei pazienti usando un database SQL Server ricovero.

Si supponga che la società di software abbia tre clienti: Hospital A, Hospital B e Hospital C. Mentre ogni cliente esegue il lato client dell'applicazione COM+ in locale nei computer desktop, il lato server dell'applicazione COM+ risiede nel server Web interno della società software ed è accessibile dai clienti tramite il Web.

Poiché ogni ospedale ha un proprio set di requisiti di archiviazione e recupero e un proprio set di dati dei pazienti personalizzati, la società di software deve fornire un modo per eseguire contemporaneamente più configurazioni della parte server dell'applicazione sul server Web. Le partizioni COM+ offrono una soluzione a questo problema.

La figura seguente illustra lo scenario delle partizioni per l'applicazione COM+ della società software.

![Diagramma che illustra uno scenario di partizioni per un'applicazione COM+, con un'applicazione client-server nel database SQL server.](images/c4a96ff9-9afd-43c7-807c-4593cb77f51b.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Restrizioni di progettazione delle applicazioni](application-design-restrictions.md)
</dt> <dt>

[Componenti e partizioni in coda COM+](com--queued-components-and-partitions.md)
</dt> <dt>

[Implementazione della partizione](partition-implementation.md)
</dt> <dt>

[Registrazione e attivazione di componenti nelle partizioni](registering-and-activating-components-in-partitions.md)
</dt> </dl>

 

 



