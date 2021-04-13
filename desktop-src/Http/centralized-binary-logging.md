---
title: Registrazione binaria centralizzata
description: La registrazione binaria centralizzata è un tipo di registrazione lato server che può essere abilitata nella sessione del server.
ms.assetid: 957a7bc4-9db3-4153-b0a9-e53b3cc514c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64bc7bdc6f7a5fce78ff66e58b4c50eac36be3f9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337246"
---
# <a name="centralized-binary-logging"></a>Registrazione binaria centralizzata

La registrazione binaria centralizzata è un tipo di registrazione lato server che può essere abilitata nella sessione del server. Funzioni di registrazione binarie centralizzate come forma centralizzata di registrazione per tutti i gruppi di URL creati nella sessione del server e consente a tutti i gruppi di URL nella sessione del server di inviare dati di log binari e non formattati a un singolo file di log. Questo tipo di registrazione può essere abilitato solo nella sessione del server. non può essere abilitata nel gruppo URL.

## <a name="when-to-use-centralized-binary-logging"></a>Quando usare la registrazione binaria centralizzata

Quando la sessione del server include numerosi gruppi di URL, il processo di creazione di centinaia di file di log formattati per i singoli gruppi di URL e la scrittura dei dati di log su un disco può utilizzare rapidamente risorse di CPU e memoria, creando in questo modo problemi di prestazioni e scalabilità. La registrazione binaria centralizzata riduce al minimo la quantità di risorse di sistema utilizzate per la registrazione, fornendo allo stesso tempo dati di log dettagliati per le organizzazioni che lo richiedono.

La registrazione binaria centralizzata è una proprietà della sessione del server che, quando abilitata, configura la registrazione per tutti i gruppi di URL nella sessione del server. Quando è abilitata la registrazione binaria centralizzata, i dati non possono essere registrati o formattati per i singoli gruppi di URL. Il file di log di registrazione binaria centralizzata ha un'estensione di file di log binario Internet (IBL). Questa estensione del nome file garantisce che le utilità di testo non tenti di aprire e leggere il file di log di registrazione binaria centrale.

## <a name="extracting-data-from-the-centralized-binary-log-file"></a>Estrazione di dati dal file di log binario centralizzato

Per estrarre i dati da un file di log non elaborato vengono eseguiti i passaggi seguenti:

-   Creare uno strumento che consente di individuare ed estrarre i dati desiderati dal file non elaborato e di convertire i dati in testo formattato. È possibile visualizzare le descrizioni dei file di intestazione e del formato del file di log in IIS 6,0 Software Development Kit in MSDN.
-   Usare lo strumento log parser per estrarre i dati dal file non elaborato. Lo strumento di log parser e la relativa documentazione utente associata sono inclusi negli strumenti di IIS 6,0 Resource Kit.

## <a name="centralized-binary-logging-file-format"></a>Formato file di registrazione binario centralizzato

Il file di log di registrazione binaria non elaborata è costituito da record a lunghezza fissa o da record di indice che contengono identificatori di stringa. I record di indice vengono visualizzati perché, nel tentativo di registrare il maggior numero possibile di informazioni, i campi stringa a lunghezza variabile vengono sostituiti da identificatori numerici, ovvero indici, che eseguono il mapping della stringa a lunghezza variabile all'identificatore registrato.

Il file di log non elaborato non è leggibile e non può essere letto con la maggior parte degli analizzatori di log disponibili. Per estrarre dati da un file di log non elaborato, è possibile creare uno strumento che consente di individuare ed estrarre i dati e quindi di convertirli in testo formattato.

Per ulteriori informazioni, vedere la pagina relativa alla [registrazione binaria centralizzata](/previous-versions/windows/it-pro/windows-server-2003/cc758733(v=ws.10)) in Microsoft TechNet.

 

 