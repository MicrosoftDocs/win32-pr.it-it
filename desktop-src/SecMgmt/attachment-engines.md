---
description: Un motore di allegati è una DLL che gestisce le richieste di configurazione e analisi specifiche del servizio.
ms.assetid: bbca486a-9eec-4510-b5fd-435972182a69
title: Motori allegati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9af0711caa5ceada7c16ae11b6470568a76d16ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883606"
---
# <a name="attachment-engines"></a>Motori allegati

Un motore di allegati è una DLL che gestisce le richieste di configurazione e analisi specifiche del servizio.

L'utente esegue una configurazione e una richiesta di analisi specifiche del servizio usando l'estensione dello snap-in allegato. Questa richiesta viene quindi passata tramite gli snap-in configurazione di sicurezza al motore di configurazione della sicurezza generale, che a sua volta passa l'elaborazione specifica del servizio al motore di allegati appropriato. Il motore dell'allegato si connette quindi al servizio e ne modifica la configurazione. In altre parole, il motore di allegati fornisce l'elaborazione back-end che supporta l'estensione dello snap-in allegato.

Un motore di allegati deve implementare le tre funzioni seguenti:

-   [**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md), che calcola la differenza tra la configurazione del servizio e la configurazione archiviata nel database di sicurezza. Le differenze vengono scritte nel database di sicurezza.
-   [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md), che configura il servizio come specificato nell'interfaccia utente dello snap-in.
-   [**SceSvcAttachmentUpdate**](scesvcattachmentupdate.md), che aggiorna la configurazione di base e l'analisi della configurazione per il servizio nel database di sicurezza.

Per semplificare l'implementazione delle funzioni precedenti, il set di strumenti di configurazione della sicurezza fornisce le funzioni e le strutture di supporto che l'applicazione può utilizzare per eseguire query e impostare le informazioni nel database di sicurezza. Per altre informazioni, vedere [funzioni di callback degli allegati](management-functions.md).

Quando si crea una DLL del motore di allegati, è necessario installarla e quindi registrarla con il motore di configurazione di sicurezza. Per registrare la DLL, aggiungere una chiave specifica al registro di sistema. Quando viene avviato, il motore di configurazione della sicurezza controlla il registro di sistema e carica tutte le dll del motore allegati registrato. Passa quindi le richieste di configurazione e analisi specifiche del servizio al motore di allegati appropriato. Le richieste di configurazione e analisi standard, che non sono specifiche del servizio, vengono gestite dal motore di configurazione della sicurezza.

 

 



