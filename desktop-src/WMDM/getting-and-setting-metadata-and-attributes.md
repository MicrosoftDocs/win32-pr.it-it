---
title: Recupero e impostazione di metadati e attributi
description: Recupero e impostazione di metadati e attributi
ms.assetid: 83534998-4e7d-49b6-a160-ef9a0ddea5db
keywords:
- Windows Gestione dispositivi multimediali, attributi
- Gestione dispositivi, attributi
- applicazioni desktop, attributi
- provider di servizi, attributi
- guida per programmatori,attributi
- attributes
- Windows Gestione dispositivi multimediali, metadati
- Gestione dispositivi, metadati
- applicazioni desktop, metadati
- provider di servizi, metadati
- guida alla programmazione, metadati
- metadata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d92c8311c3fff3c4785116604e53652c4f07b6b63b3a2c4389cc3dd4b6a5f35a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957561"
---
# <a name="getting-and-setting-metadata-and-attributes"></a>Recupero e impostazione di metadati e attributi

Un'applicazione può ottenere due tipi di informazioni su uno spazio di archiviazione o un dispositivo: attributi e metadati. Gli attributi sono valori booleani più semplici che in genere descrivono le informazioni file system, ad esempio se una archiviazione ha oggetti figlio, se può essere rinominata, letta o eliminata e così via. Gli attributi vengono recuperati come valori flag chiamando [**IWMDMStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) o [**IWMDMStorage2::GetAttributes2.**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2) Gli attributi vengono impostati chiamando [**IWMDMStorage3::SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata).

Un'applicazione può anche richiedere dati più complessi (numerici, stringa o altri tipi di dati) come *metadati*. I valori dei metadati sono identificati da nomi di stringa univoci. Windows Gestione dispositivi multimediali definisce un elenco di costanti stringa che possono essere usate per richiedere valori. Questi valori definiti sono elencati in [Costanti dei metadati.](metadata-constants.md) Un provider di servizi può definire costanti proprie, ma un'applicazione chiamante deve essere a conoscenza di queste definizioni per richiedere o impostare questi valori di metadati personalizzati. L'applicazione richiede i metadati chiamando [**IWMDMStorage3::GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) o [**IWMDMStorage4::GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata).

Un aspetto importante del recupero e dell'impostazione di metadati e attributi è comprendere da dove provengono i valori recuperati. Il provider di servizi o il dispositivo può ottenere questi valori da molte posizioni diverse, tra cui:

-   Dall'intestazione del file. In un file ASF, ad esempio, la velocità in bit viene archiviata nell'intestazione del file.
-   Da valori impostati in modo esplicito dall'applicazione quando si chiama un metodo. Questi valori possono essere salvati in un archivio di metadati esterno nel provider di servizi o nel dispositivo. Questo archivio può persistere o meno quando il dispositivo si disconnette o si spegne. Ad esempio, il numero di giochi e le classificazioni a stella utente vengono in genere archiviati in archivi esterni nel computer o nel dispositivo.
-   Esaminando le informazioni fornite dal file system. Ad esempio, se un file è di sola lettura o se una cartella ha elementi figlio.
-   Aprendo e analizzando i dati del file.

È importante tenere presente che una proprietà potrebbe essere archiviata in più di un percorso (all'interno dell'intestazione del file e anche in un archivio locale) e che potrebbe essere modificabile o meno. Ad esempio, la modifica di una descrizione di file può essere persistente o meno. Se il provider di servizi archivia la descrizione in locale, non verrà mantenuta nel dispositivo. Analogamente, se la descrizione del file viene tratta dall'intestazione del file, la modifica sarà persistente solo se il provider di servizi o il dispositivo si apre e modifica i dati dell'intestazione. La maggior parte delle applicazioni effettua un tentativo migliore modificando i valori desiderati, ma non dipende dalle proprietà da modificare in modo permanente.

Altre informazioni su come ottenere e impostare i valori sono disponibili nelle sezioni appropriate per gli sviluppatori di applicazioni e gli sviluppatori di provider di servizi più avanti nella documentazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Attività comuni ad applicazioni e provider di servizi**](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 




