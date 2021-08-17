---
description: Un motore degli allegati è una DLL che gestisce le richieste di analisi e configurazione specifiche del servizio.
ms.assetid: bbca486a-9eec-4510-b5fd-435972182a69
title: Motori degli allegati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62e09996bfb58e0447ec8e25bb627af6a4c93751a86f9f73f3499cf7f8b0fdb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118895054"
---
# <a name="attachment-engines"></a>Motori degli allegati

Un motore degli allegati è una DLL che gestisce le richieste di analisi e configurazione specifiche del servizio.

L'utente effettua una richiesta di configurazione e analisi specifica del servizio usando l'estensione dello snap-in degli allegati. Questa richiesta viene quindi passata tramite gli snap-in Configurazione di sicurezza al motore di configurazione della sicurezza generale, che a sua volta passa l'elaborazione specifica del servizio al motore degli allegati appropriato. Il motore degli allegati si connette quindi al servizio e ne modifica la configurazione. In altre parole, il motore degli allegati fornisce l'elaborazione back-end che supporta l'estensione dello snap-in degli allegati.

Un motore degli allegati deve implementare le tre funzioni seguenti:

-   [**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md), che calcola la differenza tra la configurazione del servizio e la configurazione archiviata nel database di sicurezza. Le differenze vengono scritte nel database di sicurezza.
-   [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md), che configura il servizio come specificato nell'interfaccia utente dello snap-in.
-   [**SceSvcAttachmentUpdate**](scesvcattachmentupdate.md), che aggiorna la configurazione di base e l'analisi della configurazione per il servizio nel database di sicurezza.

Per semplificare l'implementazione delle funzioni precedenti, il set di strumenti di configurazione della sicurezza fornisce funzioni e strutture di supporto che l'applicazione può usare per eseguire query e impostare informazioni nel database di sicurezza. Per altre informazioni, vedere [Funzioni di callback degli allegati.](management-functions.md)

Quando si crea una DLL del motore degli allegati, è necessario installarla e quindi registrarla con il motore di configurazione della sicurezza. Per registrare la DLL, aggiungere una chiave specifica al Registro di sistema. All'avvio, il motore di configurazione della sicurezza controlla il Registro di sistema e carica tutte le DLL del motore degli allegati registrate. Passa quindi le richieste di configurazione e analisi specifiche del servizio al motore degli allegati appropriato. Le richieste di configurazione e analisi standard, quelle non specifiche del servizio, vengono gestite dal motore di configurazione della sicurezza.

 

 



