---
description: Microsoft Security Configuration Tool set è un set di strumenti di Microsoft Management Console (MMC) che semplificano la configurazione e l'analisi della sicurezza del sistema.
ms.assetid: c6558789-84eb-4998-a2c1-725d8a64d255
title: Allegati di sicurezza del servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f47cdd0ca3799615125900a3ae6b0b78c26f4abc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343091"
---
# <a name="service-security-attachments"></a>Allegati di sicurezza del servizio

Microsoft Security Configuration Tool set è un set di strumenti di Microsoft Management Console (MMC) che semplificano la configurazione e l'analisi della sicurezza del sistema. Alcuni servizi, tuttavia, hanno esigenze di configurazione specializzate che vanno oltre le impostazioni di sicurezza fornite dal set di strumenti standard. Per gestire tali esigenze, è possibile estendere la funzionalità del set di strumenti scrivendo un allegato che gestisce le attività di sicurezza specifiche del servizio.

Lo spooler, ad esempio, è un servizio di Windows NT che definisce oggetti privati, che devono essere protetti, ad esempio stampanti. Questa funzionalità non viene gestita dal set di strumenti standard e pertanto richiede un allegato per gestire la configurazione e l'analisi degli oggetti stampante. La configurazione dei parametri di sicurezza generale, ad esempio i criteri di chiamata del servizio, è ancora gestita dal set di strumenti di configurazione della sicurezza.

Gli allegati dei servizi di sicurezza estendono le funzionalità dello strumento di configurazione della sicurezza impostato per supportare configurazioni specifiche del servizio.

Un allegato è costituito da due componenti:

-   Estensione di snap-in di MMC che implementa l'interfaccia utente dell'allegato.
-   Motore di allegati che elabora le attività di analisi e configurazione della sicurezza specifiche del servizio.

L'estensione dello snap-in allegato è ospitata dagli snap-in Configurazione sicurezza. Si tratta di snap-in di MMC che forniscono all'utente le interfacce per configurare e analizzare le impostazioni di sicurezza generali per un servizio. Le impostazioni specifiche del servizio vengono configurate utilizzando l'estensione dello snap-in allegato.

Quando l'utente modifica un'impostazione di configurazione, gli snap-in configurazione di sicurezza archiviano le nuove informazioni e quindi passano la richiesta al motore di configurazione della sicurezza. Il motore elabora la richiesta e imposta il servizio sulla nuova configurazione. Se la richiesta ha effetto su un'impostazione di sicurezza standard, viene gestita dal motore. Se la richiesta è specifica del servizio, il motore chiama il motore degli allegati appropriato per gestire la richiesta.

Nella figura seguente viene illustrato il funzionamento del motore di allegati e dell'estensione dello snap-in nel Framework del set di strumenti di configurazione della sicurezza.

![motore allegati e snap-in](images/model1a.png)

Per ulteriori informazioni sull'utilizzo del set di strumenti di configurazione della sicurezza Microsoft, cercare configurazione di sicurezza utilizzando il motore di ricerca preferito.

 

 



