---
title: Recupero e impostazione di metadati e attributi
description: Recupero e impostazione di metadati e attributi
ms.assetid: 83534998-4e7d-49b6-a160-ef9a0ddea5db
keywords:
- Windows Media Gestione dispositivi, attributi
- Gestione dispositivi, attributi
- applicazioni desktop, attributi
- provider di servizi, attributi
- Guida per programmatori, attributi
- attributes
- Windows Media Gestione dispositivi, metadati
- Gestione dispositivi, metadati
- applicazioni desktop, metadati
- provider di servizi, metadati
- Guida per programmatori, metadati
- metadata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8697f62dac44f5aab4b08aa4f6c516ac35a17e4e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856350"
---
# <a name="getting-and-setting-metadata-and-attributes"></a>Recupero e impostazione di metadati e attributi

Un'applicazione può ottenere due tipi di informazioni su uno spazio di archiviazione o un dispositivo: attributi e metadati. Gli attributi sono valori booleani più semplici che in genere descrivono file system informazioni, ad esempio se una risorsa di archiviazione dispone di oggetti figlio, se può essere rinominata, letta o eliminata e così via. Gli attributi vengono recuperati come valori di flag chiamando [**IWMDMStorage:: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) o [**IWMDMStorage2:: GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2). Gli attributi vengono impostati chiamando [**IWMDMStorage3:: tometadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata).

Un'applicazione può anche richiedere dati più complessi (numerici, stringa o altri tipi di dati) come *metadati*. I valori dei metadati sono identificati da nomi di stringa univoci. Windows Media Gestione dispositivi definisce un elenco di costanti stringa che è possibile utilizzare per richiedere valori; questi valori definiti sono elencati nelle [costanti dei metadati](metadata-constants.md). Un provider di servizi può definire le proprie costanti, ma un'applicazione chiamante deve tenere conto di tali definizioni per richiedere o impostare questi valori di metadati personalizzati. L'applicazione richiede i metadati chiamando [**IWMDMStorage3:: GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) o [**IWMDMStorage4:: GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata).

Un aspetto importante del recupero e dell'impostazione di metadati e attributi consiste nel comprendere la provenienza dei valori recuperati. Il provider di servizi o il dispositivo può ottenere questi valori da diverse posizioni, incluse le seguenti:

-   Dall'intestazione del file. Ad esempio, in un file ASF la velocità in bit viene archiviata nell'intestazione del file.
-   Da valori impostati in modo esplicito dall'applicazione quando si chiama un metodo. Questi valori possono essere salvati in un archivio di metadati esterno nel provider di servizi o nel dispositivo. Questo archivio può essere mantenuto o meno quando il dispositivo si disconnette o si spegne. Ad esempio, il numero di Play e le classificazioni a stelle utente vengono in genere archiviati in archivi esterni del computer o del dispositivo.
-   Esaminando le informazioni fornite dal file system. Ad esempio, se un file è di sola lettura o se una cartella contiene elementi figlio.
-   Aprendo e analizzando i dati del file.

È importante tenere presente che una proprietà può essere archiviata in più di una posizione (all'interno dell'intestazione del file e anche in un archivio locale) e che può essere o meno modificabile. Ad esempio, la modifica di una descrizione di file può essere persistente; Se il provider di servizi archivia la descrizione localmente, non verrà mantenute nel dispositivo. Analogamente, se la descrizione del file viene ricavata dall'intestazione del file, la modifica di questa operazione sarà permanente solo se il provider di servizi o il dispositivo viene aperto e modifica i dati dell'intestazione. La maggior parte delle applicazioni esegue un tentativo migliore modificando i valori desiderati, ma non dipende da alcuna proprietà che venga modificata in modo permanente.

Ulteriori informazioni su come ottenere e impostare i valori sono fornite nelle sezioni appropriate per gli sviluppatori di applicazioni e gli sviluppatori di provider di servizi più avanti nella documentazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Attività comuni per le applicazioni e i provider di servizi**](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 




