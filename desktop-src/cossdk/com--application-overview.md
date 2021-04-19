---
description: Un'applicazione COM+ è l'unità primaria di amministrazione e protezione per i servizi componenti ed è costituita da un gruppo di componenti COM che in genere eseguono funzioni correlate.
ms.assetid: 82e94acb-e7ce-4423-a720-26ee65d0d7b4
title: Panoramica dell'applicazione COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3365e0c0e7598d8f1eb2f466e8a2cea2d93edf4
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "106320227"
---
# <a name="com-application-overview"></a>Panoramica dell'applicazione COM+

Un'applicazione COM+ è l'unità primaria di amministrazione e protezione per i servizi componenti ed è costituita da un gruppo di componenti COM che in genere eseguono funzioni correlate. Questi componenti sono ulteriormente costituiti da interfacce e metodi, come illustrato nella figura seguente.

![Diagramma che mostra le interfacce e i metodi all'interno di caselle, in ordine di metodo all'interno di un componente all'interno dell'applicazione COM+.](images/487518b4-0460-4b2d-a834-c4ea57755ffd.png)

È possibile utilizzare lo strumento di amministrazione Servizi componenti per creare nuove applicazioni COM+, aggiungere componenti alle applicazioni e impostare gli attributi per un'applicazione e i relativi componenti.

Grazie alla creazione di gruppi logici di componenti COM come applicazioni COM+, è possibile sfruttare i vantaggi di COM+ seguenti:

-   Un ambito di distribuzione per i componenti COM.
-   Un ambito di configurazione comune per i componenti COM, inclusi i limiti di sicurezza e l'accodamento.
-   Archiviazione di attributi componente non fornita dallo sviluppatore del componente, ad esempio transazioni e sincronizzazione.
-   Librerie a collegamento dinamico (dll) del componente caricate in processi (DLLHost.exe) su richiesta.
-   Processi del server gestito per ospitare i componenti.
-   Creazione e gestione dei thread utilizzati dai componenti di.
-   Accesso all'oggetto di contesto per i dispenser di risorse, che consente di associare automaticamente le risorse acquisite al contesto. Per ulteriori informazioni sui componenti COM e i contesti, vedere [contesti com+](com--contexts.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sviluppo di applicazioni COM+](developing-com--applications.md)
</dt> <dt>

[Parti di un'applicazione COM+](parts-of-a-com--application.md)
</dt> <dt>

[Tipi di applicazioni COM+](types-of-com--applications.md)
</dt> </dl>

 

 



