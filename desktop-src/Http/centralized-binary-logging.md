---
title: Registrazione binaria centralizzata
description: La registrazione binaria centralizzata è un tipo di registrazione lato server che può essere abilitata nella sessione del server.
ms.assetid: 957a7bc4-9db3-4153-b0a9-e53b3cc514c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2006270a6bdb2b06748214bff6170b369de791456577caeb62a9abc4b625bb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047571"
---
# <a name="centralized-binary-logging"></a>Registrazione binaria centralizzata

La registrazione binaria centralizzata è un tipo di registrazione lato server che può essere abilitata nella sessione del server. La registrazione binaria centralizzata funziona come forma centralizzata di registrazione per tutti i gruppi di URL creati nella sessione del server e consente a tutti i gruppi di URL nella sessione del server di inviare dati di log binari non formattati a un singolo file di log. Questo tipo di registrazione può essere abilitato solo nella sessione del server. non può essere abilitato nel gruppo di URL.

## <a name="when-to-use-centralized-binary-logging"></a>Quando usare la registrazione binaria centralizzata

Quando la sessione del server contiene numerosi gruppi di URL, il processo di creazione di centinaia di file di log formattati per singoli gruppi di URL e scrittura dei dati di log su un disco può utilizzare rapidamente risorse preziose di CPU e memoria, creando problemi di prestazioni e scalabilità. La registrazione binaria centralizzata riduce al minimo la quantità di risorse di sistema usate per la registrazione, fornendo allo stesso tempo dati di log dettagliati per le organizzazioni che la richiedono.

La registrazione binaria centralizzata è una proprietà di sessione del server che, se abilitata, configura la registrazione per tutti i gruppi di URL nella sessione del server. Quando è abilitata la registrazione binaria centralizzata, i dati non possono essere registrati o formattati per singoli gruppi di URL. Il file di log di registrazione binaria centralizzato ha un'estensione di file di log binario Internet (con estensione ibl). Questa estensione di file garantisce che le utilità di testo non tetino di aprire e leggere il file di log di registrazione binaria centrale.

## <a name="extracting-data-from-the-centralized-binary-log-file"></a>Estrazione di dati dal file di log binario centralizzato

Per estrarre dati da un file di log non elaborato, vengono eseguiti i passaggi seguenti:

-   Creare uno strumento che individua ed estrae i dati desiderati dal file non elaborato e converte i dati in testo formattato. È possibile visualizzare le descrizioni di un file di intestazione e del formato di file di log in IIS 6.0 Software Development Kit su MSDN.
-   Usare lo strumento Parser di log per estrarre dati dal file non elaborato. Lo strumento Log Parser e la relativa documentazione per l'utente sono inclusi in STRUMENTI DI IIS 6.0 Resource Kit.

## <a name="centralized-binary-logging-file-format"></a>Formato di file di registrazione binaria centralizzato

Il file di log di registrazione binaria centralizzata non elaborato è costituito da record a lunghezza fissa o record di indice contenenti identificatori di stringa. I record dell'indice vengono visualizzati perché, nel tentativo di registrare il maggior numero possibile di informazioni, i campi stringa a lunghezza variabile vengono sostituiti da identificatori numerici, ovvero indici, che eseranno il mapping della stringa di lunghezza variabile all'identificatore registrato.

Il file di log non elaborato non è leggibile dall'utente e non può essere letto usando la maggior parte degli analizzatori di log disponibili. Per estrarre dati da un file di log non elaborato, è possibile creare uno strumento che individua ed estrae i dati e quindi lo converte in testo formattato.

Per altre informazioni, vedere [Registrazione binaria centralizzata](/previous-versions/windows/it-pro/windows-server-2003/cc758733(v=ws.10)) in Microsoft TechNet.

 

 