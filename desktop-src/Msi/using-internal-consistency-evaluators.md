---
description: Per convalidare un database, usare uno strumento di convalida speciale per unire un file con estensione cub che contiene gli analizzatori di coerenza interni (CIEM) nel database, eseguire il servizio di verifica di sistema e segnalare i risultati.
ms.assetid: bdf38673-ee3d-47d8-ad6e-562cd5626918
title: Utilizzo degli analizzatori di coerenza interni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423e6dab453ae495dc6029b54eb039c8acc60f33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307242"
---
# <a name="using-internal-consistency-evaluators"></a>Utilizzo degli analizzatori di coerenza interni

Per convalidare un database, usare uno strumento di convalida speciale per unire un file con estensione cub che contiene gli [analizzatori di coerenza interni](internal-consistency-evaluators-ices.md) (CIEM) nel database, eseguire il servizio di verifica di sistema e segnalare i risultati. Molti di questi strumenti sono disponibili in Microsoft Windows Software Development Kit (SDK). Gli ambienti di creazione di fornitori di terze parti possono anche incorporare il sistema di convalida del ghiaccio nell'ambiente di creazione. È anche possibile scrivere il proprio strumento per eseguire la convalida del ghiaccio. La maggior parte degli strumenti di convalida del ghiaccio unisce il file con estensione cub e il database in un terzo database temporaneo. Windows Installer Visualizza avvisi, errori, informazioni di debug ed errori API durante l'esecuzione di ogni ghiaccio nel file con estensione cub. Al termine dell'esecuzione del programma di installazione, chiude il file con estensione msi, il file con estensione cub e il database temporaneo senza salvare le modifiche. Il file con estensione msi e il file con estensione cub rimangono invariati dal test di convalida.

Le azioni personalizzate del ghiaccio comunicano all'utente chiamando [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) e inviando un \_ messaggio utente INSTALLMESSAGE. Un messaggio di ghiaccio restituisce generalmente informazioni come le seguenti:

-   Nome del ghiaccio che ha rilevato un errore
-   Data di creazione del ghiaccio
-   Autore del ghiaccio
-   Data dell'Ultima modifica del ghiaccio.
-   Descrizione dell'errore dell'API che causa il guasto del ghiaccio
-   Descrizione dell'errore
-   Avviso per l'utente
-   Nome della tabella di database contenente l'errore o l'avviso
-   Nome della colonna di tabella contenente l'errore o l'avviso
-   Chiavi primarie della tabella contenente l'errore o l'avviso
-   URL di un file HTML che fornisce suggerimenti per il debug
-   Stringa che può contenere altre informazioni

Gli autori dei pacchetti di installazione possono scrivere azioni personalizzate ICE o usare il set standard di gelati inclusi nei file con estensione cub forniti con l'SDK. Per ulteriori informazioni su come scrivere un ghiaccio, vedere la pagina relativa alla [creazione di un ghiaccio](building-an-ice.md).

Una volta scritti i database appropriati per la convalida, lo sviluppatore deve raccogliere le azioni personalizzate in un database con estensione msi, denominato file con estensione cub, che contiene solo i ghiacci e le tabelle necessarie. Non è possibile installare un file con estensione cub e viene usato solo per archiviare e fornire l'accesso alle azioni personalizzate di ICE. Per ulteriori informazioni sulla creazione di file con estensione cub, vedere la pagina relativa alla [creazione di un database Ice](building-an-ice-database.md). In alternativa, gli sviluppatori possono convalidare il pacchetto di installazione usando i ghiacci esistenti descritti in [Ice Reference](ice-reference.md). Questi CIEM possono essere ottenuti da file con estensione cub standard forniti con l'SDK.

L'installazione dell'Editor tabella di database Orca o lo strumento di convalida MSIVal2 fornisce i file logo. cub, Darice. cub e Mergemod. cub. Il set di CIEM nel file logo. cub è un subset di quelli nel file Darice. cub. Se il pacchetto passa la convalida usando Darice. cub, passerà con logo. cub. Mergemod. cub contiene un set di CIEM utilizzati per convalidare i moduli unione. Per ulteriori informazioni, vedere la pagina relativa al [riferimento ghiaccio del modulo merge](merge-module-ice-reference.md).

**Per convalidare un pacchetto di installazione**

1.  Ottenere o creare le azioni personalizzate ICE appropriate. Potrebbe essere possibile usare uno o più dei ghiacci esistenti descritti nella Guida di riferimento a [Ice](ice-reference.md). Se la convalida richiede un ghiaccio non ancora presente nell'elenco, è possibile creare un nuovo ghiaccio come descritto in [creazione di un ghiaccio](building-an-ice.md).
2.  Preparare un database di ghiaccio contenente tutte le azioni personalizzate del ghiaccio. Per informazioni sulla preparazione di un file con estensione cub, vedere la sezione [creazione di un database di Ice](building-an-ice-database.md) .
3.  Fornire il file con estensione cub e il file con estensione msi a uno strumento di convalida del pacchetto, ad esempio [Orca.exe](orca-exe.md) o [Msival2.exe](msival2-exe.md).

Si noti che i moduli merge devono essere convalidati come descritto in [convalida di moduli merge](validating-merge-modules.md).

 

 



