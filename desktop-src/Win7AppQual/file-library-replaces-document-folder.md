---
description: La raccolta file sostituisce la cartella del documento
ms.assetid: 80b97bfc-4212-4401-a4a9-d96e2f39be60
title: La raccolta file sostituisce la cartella del documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 699c645d574012a419f77538bcc58d61a4938120
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088379"
---
# <a name="file-library-replaces-document-folder"></a>La raccolta file sostituisce la cartella del documento

## <a name="affected-platforms"></a>Piattaforme interessate

**Client** - Windows 7  
**Server** - Windows Server 2008 R2  









## <a name="feature-impact"></a>Impatto sulle funzionalità

**Gravità** - Media  
**Frequenza** - Alta  











## <a name="description"></a>Descrizione

Le librerie offrono un'esperienza centralizzata simile a una cartella per l'archiviazione di file, la ricerca e l'accesso in più posizioni, sia locali che remote.

I percorsi predefiniti usati dalle finestre di dialogo comuni dei file, ad esempio Apri e Salva, sono stati modificati da Cartella documento a Raccolta documenti. Il Interfaccia utente è invariato, ma l'utente sarà ora in grado di visualizzare, esplorare ed eseguire ricerche nella libreria usando diverse visualizzazioni di disposizione. I file verranno salvati nel percorso di salvataggio predefinito della libreria, a meno che l'utente non cambi il percorso di salvataggio predefinito o sceva una cartella diversa.

Gli sviluppatori possono creare librerie personalizzate o aggiungere percorsi alle librerie esistenti usando l'interfaccia IShellLibrary. Gli utenti possono trovare le librerie usando il sistema cartella nota (ad esempio, FOLDERID \_ DocumentsLibrary).

## <a name="manifestation-of-impact"></a>Impatto significativo

La libreria è di per sé un file e non una cartella. Di conseguenza, le modifiche al percorso potrebbero causare errori a causa del tentativo da parte dell'applicazione di concatenare i file ai file.

## <a name="solution"></a>Soluzione

Quando si usa IFileDialog, è necessario usare il metodo GetResult anziché la combinazione di GetFolder e GetFilename come nelle versioni precedenti del sistema operativo. Usare le API shell laddove possibile per interagire con gli elementi nello spazio dei nomi della shell e modificarli, ad esempio IShellItem.

## <a name="leveraging-feature-capabilities"></a>Sfruttare le funzionalità delle funzionalità

Se si vogliono creare librerie personalizzate o aggiungere percorsi a librerie esistenti, è necessario usare l'API IShellLibrary. Le librerie sono a loro volta cartelle shell, quindi è possibile enumerarle esattamente come qualsiasi altra cartella shell.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Test di compatibilità, prestazioni, affidabilità e usabilità

L'uso della finestra di dialogo file comune garantisce che gli utenti possano salvare direttamente nelle librerie.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   **Librerie di Windows:**https://msdn.microsoft.com/library/dd758096(VS.85).aspx
-   **Mantenere la sincronizzazione con una libreria:**https://msdn.microsoft.com/library/dd758094(VS.85).aspx\#library\_keeping\_in\_sync

 

 



