---
title: Ripristino del sistema
description: Quando il computer viene usato nel tempo, i punti di ripristino vengono raccolti nell'archivio dati senza alcuna gestione o intervento richiesto dall'utente.
ms.assetid: 9581eff5-44d0-407e-b7cb-d3e13910a936
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c5ff4aef88ec9eca591ee3c1afb1ad570689a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298233"
---
# <a name="restoring-the-system"></a>Ripristino del sistema

Quando il computer viene usato nel tempo, i punti di ripristino vengono raccolti nell'archivio dati senza alcuna gestione o intervento richiesto dall'utente. Se l'utente deve sempre ripristinare lo stato precedente del sistema, i punti di ripristino disponibili vengono resi visibili all'utente tramite l'interfaccia utente di ripristino del sistema. L'utente può scegliere uno di questi punti di ripristino. L'unico modo per accedere a questo archivio dei punti di ripristino è tramite l'interfaccia utente di ripristino del sistema e l'API di ripristino del sistema. Ciò consente di proteggere l'integrità dei dati ed evitare modifiche accidentali apportate dall'utente, dalle applicazioni o da altri agenti.

Per ripristinare un sistema, ripristino configurazione di sistema Annulla le modifiche apportate ai file monitorati, riacquisendo lo stato del file al momento del punto di ripristino selezionato. Sostituisce quindi il registro di sistema corrente con quello salvato per il punto di ripristino selezionato.

Per assicurarsi che l'applicazione abbia il comportamento desiderato dopo un ripristino, eseguire le operazioni seguenti:

-   Non archiviare nel registro di sistema le informazioni che impediscono agli utenti di accedere ai file di dati personali o alle applicazioni in ripristino configurazione di sistema. In caso contrario, è necessario fornire un meccanismo mediante il quale l'utente può scaricare e reinstallare le applicazioni senza doverle pagare di nuovo.
-   Utilizzare l' [API ripristino configurazione di sistema](system-restore-api.md) per creare punti di ripristino significativi in fase di installazione e disinstallazione.
-   In Windows XP, i file binari dell'applicazione chiave da proteggere devono utilizzare le estensioni coerenti con quelle utilizzate in Filelist.xml. Per altre informazioni, vedere [estensioni di file monitorate](monitored-file-extensions.md). Questo file non viene utilizzato da Windows 7 e Windows Vista. Non usare i tipi di estensione monitorati per i file modificabili dall'utente. Ad esempio, se si rinomina un file di dati personali di un utente usando Extension. ini, l'utente potrebbe perdere lavoro in seguito a un ripristino del sistema.

 

 




