---
description: Quando si sviluppano applicazioni COM+, le attività principali includono la progettazione di componenti COM per incapsulare la logica dell'applicazione e l'integrazione di questi componenti in un'applicazione COM+, la creazione dell'applicazione COM+ e l'amministrazione dell'applicazione tramite la distribuzione e la manutenzione.
ms.assetid: 8c6ec901-1eeb-46b0-8a3a-26d8eff99f6d
title: Sviluppo di applicazioni COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54526cc0fd900dbf92f8a69986b9aafc8e41a59f3964eafa2317b196ffbf6f0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047486"
---
# <a name="developing-com-applications"></a>Sviluppo di applicazioni COM+

Quando si sviluppano applicazioni COM+, le attività principali includono la progettazione di componenti COM per incapsulare la logica dell'applicazione e l'integrazione di questi componenti in un'applicazione COM+, la creazione dell'applicazione COM+ e l'amministrazione dell'applicazione tramite la distribuzione e la manutenzione.

## <a name="designing-com-components"></a>Progettazione di componenti COM

I passaggi seguenti descrivono una procedura generale per una buona progettazione dei componenti:

1.  Definire le classi COM e le classi di implementazione.
2.  Raggruppare le classi in componenti.
3.  Selezionare il set di servizi COM+ per il componente, anche se non vengono specificati tutti durante lo sviluppo del componente. Questi servizi possono essere specificati in un secondo momento usando lo strumento amministrativo Servizi componenti o il modello a oggetti di amministrazione COM+. Per altre informazioni sul modello a oggetti di amministrazione COM+, vedere Automazione dell'amministrazione [COM+.](automating-com--administration.md)

## <a name="creating-the-com-application"></a>Creazione dell'applicazione COM+

Dopo aver progettato i componenti COM, lo sviluppatore integra i componenti in un'applicazione COM+ e configura l'applicazione. I passaggi seguenti descrivono il processo:

1.  Integrare i componenti in un'applicazione COM+. È possibile integrare i componenti in un'applicazione COM+ esistente o creare una nuova applicazione (vuota) per i componenti. Vedere [Creazione di applicazioni COM+.](creating-com--applications.md)
2.  Specificare il set corretto di attributi per ogni classe (se presente e se non specificato nello strumento di sviluppo). Questi attributi esprimono le dipendenze dei componenti da qualsiasi servizio COM+ su cui potrebbe basarsi l'implementazione (ad esempio, transazioni, componenti in coda, sicurezza, pool di oggetti e attivazione JUST-In-Time).
3.  Configurare il framework di sicurezza (ruoli e assegnazione di ruoli a classi, interfacce e metodi).
4.  Configurare attributi specifici dell'ambiente per classi e applicazioni , ad esempio le dimensioni predefinite del pool di oggetti. Questi attributi specifici dell'ambiente possono essere successivamente impostati (o modificati) dall'amministratore di sistema.
5.  Esportare l'applicazione per la ridistribuzione e la distribuzione.

Per informazioni più dettagliate sui passaggi per la progettazione di applicazioni distribuite, vedere [Progettazione di applicazioni COM+.](designing-com--applications.md)

## <a name="administering-com-applications"></a>Amministrazione di applicazioni COM+

In genere, uno sviluppatore fornisce un'applicazione COM+ parzialmente configurata all'amministratore di sistema. L'amministratore può quindi personalizzare l'applicazione per uno o più ambienti specifici, ad esempio aggiungendo account utente in ruoli e nomi di server in un cluster di applicazioni. Le attività dell'amministratore includono quanto segue:

-   Installazione dell'applicazione COM+ parzialmente configurata in un computer amministrativo.
-   Fornire attributi specifici dell'ambiente, ad esempio i membri del ruolo e le dimensioni del pool di oggetti.
-   Esportare nuovamente l'applicazione COM+ completamente configurata.
-   Creazione di un proxy di applicazione (se è necessario accedere all'applicazione in modalità remota).

Dopo che un'applicazione è stata completamente configurata per un ambiente specifico, l'amministratore può distribuirla nei computer di test o di produzione. Ciò comporta l'installazione dell'applicazione COM+ completamente configurata in uno o più computer.

Per informazioni dettagliate sulle procedure di amministrazione COM+, vedere lo strumento di amministrazione Servizi componenti.

 

 



