---
description: Quando si sviluppano applicazioni COM+, le attività principali includono la progettazione di componenti COM per incapsulare la logica dell'applicazione e l'integrazione di questi componenti in un'applicazione COM+, la creazione dell'applicazione COM+ e l'amministrazione dell'applicazione tramite la distribuzione e la manutenzione.
ms.assetid: 8c6ec901-1eeb-46b0-8a3a-26d8eff99f6d
title: Sviluppo di applicazioni COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ee6495b7d8f7b2cc059b113f4250042cfd59b99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523242"
---
# <a name="developing-com-applications"></a>Sviluppo di applicazioni COM+

Quando si sviluppano applicazioni COM+, le attività principali includono la progettazione di componenti COM per incapsulare la logica dell'applicazione e l'integrazione di questi componenti in un'applicazione COM+, la creazione dell'applicazione COM+ e l'amministrazione dell'applicazione tramite la distribuzione e la manutenzione.

## <a name="designing-com-components"></a>Progettazione di componenti COM

Nei passaggi seguenti viene descritta una procedura generale per la progettazione di un componente efficace:

1.  Definire le classi COM e le classi di implementazione.
2.  Raggruppare le classi in componenti.
3.  Selezionare il set di servizi COM+ per il componente, anche se non vengono specificati tutti quando si sviluppa il componente. Questi servizi possono essere specificati in un secondo momento utilizzando lo strumento di amministrazione Servizi componenti o il modello a oggetti di amministrazione COM+. per ulteriori informazioni sul modello a oggetti di amministrazione com+, vedere [automazione dell'amministrazione com+](automating-com--administration.md) .

## <a name="creating-the-com-application"></a>Creazione dell'applicazione COM+

Dopo aver progettato i componenti COM, lo sviluppatore integra i componenti in un'applicazione COM+ e configura l'applicazione. I passaggi seguenti descrivono il processo:

1.  Integrare i componenti in un'applicazione COM+. È possibile integrare i componenti in un'applicazione COM+ esistente o creare una nuova applicazione (vuota) per i componenti. Vedere [creazione di applicazioni com+](creating-com--applications.md).
2.  Specificare il set di attributi corretto per ogni classe (se presente) e se non è specificato nello strumento di sviluppo. Questi attributi esprimono le dipendenze dei componenti da qualsiasi servizio COM+ su cui può basarsi l'implementazione (ad esempio, transazioni, componenti in coda, sicurezza, pool di oggetti e attivazione JIT).
3.  Configurare il Framework di sicurezza (ruoli e assegnazione di ruoli a classi, interfacce e metodi).
4.  Configurare gli attributi specifici dell'ambiente sulle classi e sulle applicazioni, ad esempio le dimensioni predefinite del pool di oggetti. Questi attributi specifici dell'ambiente possono essere impostati o modificati in un secondo momento dall'amministratore di sistema.
5.  Esportare l'applicazione per la ridistribuzione e la distribuzione.

Per informazioni più dettagliate sui passaggi per la progettazione di applicazioni distribuite, vedere [progettazione di applicazioni com+](designing-com--applications.md).

## <a name="administering-com-applications"></a>Amministrazione di applicazioni COM+

In genere, uno sviluppatore Invia un'applicazione COM+ parzialmente configurata all'amministratore di sistema. L'amministratore può quindi personalizzare l'applicazione per uno o più ambienti specifici, ad esempio aggiungendo account utente in ruoli e nomi di server in un cluster di applicazioni. Le attività dell'amministratore includono quanto segue:

-   Installazione dell'applicazione COM+ parzialmente configurata in un computer amministrativo.
-   Fornire attributi specifici dell'ambiente, ad esempio i membri del ruolo e le dimensioni del pool di oggetti.
-   Riesportazione dell'applicazione COM+ completamente configurata.
-   Creazione di un proxy di applicazione (se l'applicazione deve essere accessibile in modalità remota).

Dopo che un'applicazione è stata completamente configurata per un ambiente specifico, l'amministratore può quindi distribuirla nei computer di test o di produzione. Questa operazione comporta l'installazione dell'applicazione COM+ completamente configurata in uno o più computer.

Per informazioni dettagliate sulle procedure di amministrazione COM+, vedere lo strumento di amministrazione Servizi componenti.

 

 



