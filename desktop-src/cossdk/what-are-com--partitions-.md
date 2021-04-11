---
description: Una partizione COM+ è un contenitore logico che consente l'esecuzione delle applicazioni indipendentemente da altre configurazioni di tali applicazioni.
ms.assetid: c1290d10-968f-44f0-8099-d69c9e706c9e
title: Che cosa sono le partizioni COM+?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69acdae724bb0c9211d147a985f7571c5e7c052f
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "104132126"
---
# <a name="what-are-com-partitions"></a>Che cosa sono le partizioni COM+?

Una partizione COM+ è un contenitore logico che consente l'esecuzione delle applicazioni indipendentemente da altre configurazioni di tali applicazioni. Ogni configurazione di un'applicazione viene installata in una partizione separata e può essere gestita separatamente, in base alle esigenze specifiche degli utenti.

Durante l'attivazione di un componente COM+, il servizio partizioni determina la configurazione del componente da attivare, in base all'identità dell'utente che richiede l'attivazione del componente. Ad esempio, una singola organizzazione che dispone di due gruppi distinti, produzione e training, potrebbe implementare partizioni COM+ come modo per consentire ai due gruppi di utilizzare configurazioni diverse di un'applicazione COM+ nello stesso computer.

**Windows XP:** La possibilità di creare, configurare o delegare partizioni COM+ non è disponibile. La partizione globale è l'unica partizione COM+ disponibile.

**Windows 2000:** Il servizio partizioni COM+ non è disponibile in Windows 2000.

## <a name="benefits-of-using-com-partitions"></a>Vantaggi dell'utilizzo di partizioni COM+

L'utilizzo di partizioni COM+ offre diversi vantaggi, tra cui:

-   Le organizzazioni possono ridurre il costo totale di proprietà (TCO) usando un minor numero di server di applicazioni fisiche per supportare gli utenti che necessitano di più configurazioni dell'applicazione.
-   Il sovraccarico amministrativo è ridotto. Anziché dover configurare e gestire più computer, è necessario che gli amministratori configurano e gestiscano solo più partizioni nello stesso computer. Inoltre, le partizioni possono essere gestite a livello di codice tramite l'aggiunta di una nuova interfaccia di programmazione COM+.
-   La sicurezza può essere implementata e gestita in base a una partizione per partizione per utenti locali, utenti di dominio e unità organizzative (OU).
-   Programmatori e amministratori possono utilizzare gli strumenti di sviluppo e amministrazione di Microsoft, ad esempio Windows SDK, Active Directory utenti e computer e lo strumento di amministrazione Servizi componenti, per gestire le partizioni COM+. La funzionalità partizioni è completamente integrata in questi strumenti.

## <a name="primary-usage-scenario"></a>Scenario di utilizzo primario

Un motivo principale per cui i clienti possono distribuire la funzionalità partizioni COM+ consiste nell'ospitare applicazioni basate sul Web. Si supponga, ad esempio, che una piccola azienda di software sviluppa un'applicazione COM+ da utilizzare per il personale dell'ospedale. L'applicazione, che è un'applicazione basata sul Web distribuita, fornisce agli ospedali un modo per archiviare e recuperare le registrazioni cliniche dei pazienti usando un database SQL Server.

Si supponga che la società software abbia tre clienti: Hospital A, Hospital B e Hospital C. Sebbene ogni cliente esegua il lato client dell'applicazione COM+ localmente nei propri computer desktop, il lato server dell'applicazione COM+ risiede nel server Web interno della società software ed è accessibile dai clienti tramite il Web.

Poiché ogni ospedale dispone di un proprio set di requisiti di archiviazione e recupero e di un proprio set di dati personalizzati dei pazienti, l'azienda software deve fornire un modo per eseguire contemporaneamente più configurazioni della parte server dell'applicazione nel server Web. Le partizioni COM+ forniscono una soluzione a questo problema.

Nella figura seguente viene illustrato lo scenario relativo alle partizioni per l'applicazione COM+ della società software.

![Diagramma che mostra uno scenario di partizioni per un'applicazione COM+, con un'applicazione client per l'applicazione server al database di SQL Server.](images/c4a96ff9-9afd-43c7-807c-4593cb77f51b.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Limitazioni relative alla progettazione di applicazioni](application-design-restrictions.md)
</dt> <dt>

[Componenti e partizioni in coda COM+](com--queued-components-and-partitions.md)
</dt> <dt>

[Implementazione della partizione](partition-implementation.md)
</dt> <dt>

[Registrazione e attivazione di componenti nelle partizioni](registering-and-activating-components-in-partitions.md)
</dt> </dl>

 

 



