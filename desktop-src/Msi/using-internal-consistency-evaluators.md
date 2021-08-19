---
description: Per convalidare un database, usare uno speciale strumento di convalida per unire un file con estensione cub contenente gli analizzatori di coerenza interna (ICE) nel database, eseguire le ICE e segnalare i risultati.
ms.assetid: bdf38673-ee3d-47d8-ad6e-562cd5626918
title: Uso degli analizzatori di coerenza interna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdd0964b43bdf237c01b2645ca9556ed5560cefd2b047cc108a8919060d1fad9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012749"
---
# <a name="using-internal-consistency-evaluators"></a>Uso degli analizzatori di coerenza interna

Per convalidare un database, usare uno speciale strumento di [](internal-consistency-evaluators-ices.md) convalida per unire un file con estensione cub contenente gli analizzatori di coerenza interna (ICE) nel database, eseguire le ICE e segnalare i risultati. Diversi strumenti di questo tipo sono disponibili in Microsoft Windows Software Development Kit (SDK). Anche gli ambienti di creazione di fornitori di terze parti possono incorporare il sistema di convalida ICE nell'ambiente di creazione. È anche possibile scrivere uno strumento personalizzato per eseguire la convalida ICE. La maggior parte degli strumenti di convalida ICE unisce il file con estensione cub e il database in un terzo database temporaneo. Windows Il programma di installazione visualizza avvisi, errori, informazioni di debug ed errori api durante l'esecuzione di ogni ICE nel file con estensione cub. Al termine dell'esecuzione, il programma di installazione chiude il file .msi, il file CUB e il database temporaneo senza salvare le modifiche. Il .msi file e il file con estensione cub rimangono invariati dal test di convalida.

Le azioni personalizzate ICE comunicano all'utente chiamando [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) e pubblicando un messaggio INSTALLMESSAGE \_ USER. Un messaggio ICE restituisce in genere informazioni come le seguenti:

-   Nome dell'ice che ha rilevato un errore
-   Data di creazione dell'ice
-   Autore di ICE
-   Data dell'ultima modifica dell'ice.
-   Descrizione dell'errore API che causa l'errore ICE
-   Descrizione dell'errore
-   Avviso per l'utente
-   Nome della tabella di database contenente l'errore o l'avviso
-   Nome della colonna della tabella contenente l'errore o l'avviso
-   Chiavi primarie della tabella contenente l'errore o l'avviso
-   URL di un file HTML che contiene suggerimenti per il debug
-   Stringa che può contenere altre informazioni

Gli autori dei pacchetti di installazione possono scrivere azioni personalizzate ICE o usare il set standard di ICE inclusi nei file con estensione cub forniti con l'SDK. Per altre informazioni su come scrivere un ice, vedere [Building an ICE](building-an-ice.md).

Dopo aver scritto gli ICE appropriati per la convalida, uno sviluppatore deve raccogliere insieme le azioni personalizzate in un database .msi, denominato file con estensione cub, che contiene solo le ICE e le relative tabelle necessarie. Non è possibile installare un file con estensione cub e viene usato solo per archiviare e fornire l'accesso alle azioni personalizzate ICE. Per altre informazioni sulla creazione di file con estensione cub, vedere [Compilazione di un database ICE.](building-an-ice-database.md) In alternativa, gli sviluppatori possono convalidare il pacchetto di installazione usando le ICE esistenti descritte in [Ice Reference](ice-reference.md). Questi ICE possono essere ottenuti dai file con estensione cub standard forniti con l'SDK.

L'installazione dell'editor di tabelle di database Orca o dello strumento di convalida msival2 fornisce i file Logo.cub, Darice.cub e Mergemod.cub. Il set di ICE nel file Logo.cub è un subset di quelli nel file Darice.cub. Se il pacchetto supera la convalida usando Darice.cub, passerà con Logo.cub. Mergemod.cub contiene un set di ICE usate per convalidare i moduli unione. Per altre informazioni, vedere [Informazioni di riferimento su ICE del modulo di merge](merge-module-ice-reference.md).

**Per convalidare un pacchetto di installazione**

1.  Ottenere o creare le azioni personalizzate ICE appropriate. Potrebbe essere possibile usare uno o più ICE esistenti descritti in [Ice Reference](ice-reference.md). Se la convalida richiede un ice non ancora in questo elenco, è possibile creare un nuovo ICE come descritto in [Creazione di un ICE.](building-an-ice.md)
2.  Preparare un database ICE contenente tutte le azioni personalizzate ICE. Per informazioni sulla preparazione di un file con estensione cub, vedere la sezione Creazione di un database [ICE.](building-an-ice-database.md)
3.  Fornire il file con estensione cub e il file .msi a uno strumento di convalida del pacchetto, ad esempio [Orca.exe](orca-exe.md) [ oMsival2.exe](msival2-exe.md).

Si noti che i moduli unione devono essere convalidati come descritto in [Convalida dei moduli unione](validating-merge-modules.md).

 

 



