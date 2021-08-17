---
title: Ripristino del sistema
description: Poiché il computer viene usato nel tempo, i punti di ripristino vengono raccolti nell'archivio dati senza alcuna gestione o intervento richiesto dall'utente.
ms.assetid: 9581eff5-44d0-407e-b7cb-d3e13910a936
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99d7e54fd12bbb05dacd0c388c1867319189924d761a43d90c6f2a9f718f26e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857521"
---
# <a name="restoring-the-system"></a>Ripristino del sistema

Poiché il computer viene usato nel tempo, i punti di ripristino vengono raccolti nell'archivio dati senza alcuna gestione o intervento richiesto dall'utente. Se l'utente deve ripristinare lo stato precedente del sistema, i punti di ripristino disponibili vengono resi visibili all'utente Ripristino configurazione di sistema'interfaccia utente. L'utente può scegliere uno di questi punti di ripristino. L'unico modo per accedere a questo archivio di punti di ripristino è tramite l'Ripristino configurazione di sistema utente e l'API Ripristino configurazione di sistema; ciò consente di proteggere l'integrità dei dati ed evitare modifiche accidentali apportate dall'utente, dalle applicazioni o da altri agenti.

Per ripristinare un sistema, Ripristino configurazione di sistema le modifiche apportate ai file monitorati, ricapitolando lo stato del file al momento del punto di ripristino selezionato. Sostituisce quindi il Registro di sistema corrente con quello salvato per il punto di ripristino selezionato.

Per assicurarsi che l'applicazione abbia il comportamento desiderato dopo un ripristino, eseguire le operazioni seguenti:

-   Non archiviare le informazioni nel Registro di sistema che impediscono l'accesso degli utenti ai file di dati personali o alle applicazioni durante il ripristino del sistema. In caso contrario, è necessario fornire un meccanismo in base al quale l'utente può scaricare e reinstallare le applicazioni senza dover pagare di nuovo.
-   Usare [l'API Ripristino configurazione di sistema per](system-restore-api.md) creare punti di ripristino significativi durante l'installazione e la disinstallazione.
-   In Windows XP, i file binari dell'applicazione chiave da proteggere devono usare estensioni coerenti con quelle usate in Filelist.xml. Per altre informazioni, vedere [Estensioni di file monitorate.](monitored-file-extensions.md) Questo file non viene usato da Windows 7 e Windows Vista. Non usare tipi di estensione monitorati per i file modificabili dall'utente. Ad esempio, se si denoma il file di dati personali di un utente usando l'estensione .ini, l'utente potrebbe perdere il lavoro a causa di un ripristino del sistema.

 

 




