---
description: Un motore di allegati è una DLL che elabora le richieste di configurazione e analisi specifiche del servizio. In altre parole, gestisce l'elaborazione che non può essere gestita dal set di strumenti di configurazione della sicurezza standard.
ms.assetid: c04779f4-f1e9-40b0-9f00-0176afb1b839
title: Creazione di un motore di allegati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96b16e768956e61fe76406777da2bce9affbfa2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315355"
---
# <a name="creating-an-attachment-engine"></a>Creazione di un motore di allegati

Un motore di allegati è una DLL che elabora le richieste di configurazione e analisi specifiche del servizio. In altre parole, gestisce l'elaborazione che non può essere gestita dal set di strumenti di configurazione della sicurezza standard.

Per creare un motore di allegati, è necessario implementare le tre funzioni seguenti:

-   [**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md), che calcola la differenza tra la configurazione del servizio e la configurazione archiviata nel database di sicurezza. Queste differenze vengono scritte nel database di sicurezza. Per ulteriori informazioni, vedere [implementazione di SceSvcAttachmentAnalyze](implementing-scesvcattachmentanalyze.md).
-   [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md), che configura il servizio come specificato nell'interfaccia utente dello snap-in. Per ulteriori informazioni, vedere [implementazione di SceSvcAttachmentConfig](implementing-scesvcattachmentconfig.md).
-   [**SceSvcAttachmentUpdate**](scesvcattachmentupdate.md), che aggiorna la configurazione di base e l'analisi della configurazione per il servizio nel database di sicurezza. Per ulteriori informazioni, vedere [implementazione di SceSvcAttachmentUpdate](implementing-scesvcattachmentupdate.md).

Il set di strumenti di configurazione della sicurezza implementa un set di funzioni di supporto che l'applicazione può chiamare per eseguire query e impostare le informazioni nel database di sicurezza. Per altre informazioni, vedere [funzioni di callback degli allegati](management-functions.md).

Dopo aver creato una DLL del motore allegati, è necessario registrarla con il set di strumenti di configurazione della sicurezza. Questo processo è descritto in [registrazione di un motore di allegati](registering-an-attachment-engine.md).

Oltre a creare un motore di allegati, è necessario creare anche un'estensione dello snap-in allegato. L'estensione dello snap-in fornisce un'interfaccia utente per attività specifiche del servizio. Quando l'utente specifica una nuova configurazione usando un'estensione dello snap-in, la richiesta viene passata al motore degli allegati appropriato. Il motore si connette quindi al servizio e ne modifica la configurazione. Se non si implementa un'estensione dello snap-in, gli utenti non avranno alcun modo per modificare la configurazione o l'analisi del servizio. Per ulteriori informazioni su come creare un'estensione dello snap-in allegato, vedere [creazione di un'estensione dello snap-in allegato](creating-an-attachment-snap-in-extension.md).

 

 



