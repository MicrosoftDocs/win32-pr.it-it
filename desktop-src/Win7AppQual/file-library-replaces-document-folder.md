---
description: La raccolta file sostituisce la cartella del documento
ms.assetid: 80b97bfc-4212-4401-a4a9-d96e2f39be60
title: La raccolta file sostituisce la cartella del documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1e8d08b176ebf4b5801a73695ea03f60a38eeb5a1ca51e1d90d9119dae5fcaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118329671"
---
# <a name="file-library-replaces-document-folder"></a>La raccolta file sostituisce la cartella del documento

## <a name="affected-platforms"></a>Piattaforme interessate

**Client** - Windows 7  
**Server** - Windows Server 2008 R2  









## <a name="feature-impact"></a>Impatto sulle funzionalità

**Gravità** - Media  
**Frequenza** - Alta  











## <a name="description"></a>Descrizione

Le librerie offrono un'esperienza centralizzata simile a una cartella per l'archiviazione, la ricerca e l'accesso ai file in più posizioni, sia locali che remote.

I percorsi predefiniti usati dalle finestre di dialogo di file comuni, ad esempio Apri e Salva, sono stati modificati da Cartella documento a Raccolta documenti. Il Interfaccia utente è invariato, ma l'utente sarà ora in grado di visualizzare, esplorare ed eseguire ricerche nella libreria usando diverse visualizzazioni di disposizione. I file verranno salvati nel percorso di salvataggio predefinito della libreria, a meno che l'utente non cambi il percorso di salvataggio predefinito o non sceva una cartella diversa.

Gli sviluppatori possono creare librerie personalizzate o aggiungere percorsi a librerie esistenti usando l'interfaccia IShellLibrary. Gli utenti possono trovare librerie usando il sistema cartella nota (ad esempio, FOLDERID \_ DocumentsLibrary).

## <a name="manifestation-of-impact"></a>Manifestazione di impatto

La libreria è di per sé un file e non una cartella. Di conseguenza, le manipolazioni del percorso potrebbero causare errori a causa del tentativo da parte dell'applicazione di concatenare i file ai file.

## <a name="solution"></a>Soluzione

Quando si usa IFileDialog, è necessario usare il metodo GetResult anziché la combinazione di GetFolder e GetFilename come nelle versioni precedenti del sistema operativo. Usare le API shell, laddove possibile, per interagire con e modificare gli elementi nello spazio dei nomi della shell, ad esempio IShellItem.

## <a name="leveraging-feature-capabilities"></a>Sfruttare le funzionalità delle funzionalità

Se si vogliono creare librerie personalizzate o aggiungere percorsi a librerie esistenti, è necessario usare l'API IShellLibrary. Le librerie sono a loro volta cartelle shell, quindi è possibile enumerarle esattamente come qualsiasi altra cartella shell.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Test di compatibilità, prestazioni, affidabilità e usabilità

L'uso della finestra di dialogo file comune garantisce che gli utenti possano salvare direttamente nelle librerie.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   **Windows librerie:**https://msdn.microsoft.com/library/dd758096(VS.85).aspx
-   **Mantenere la sincronizzazione con una libreria:**https://msdn.microsoft.com/library/dd758094(VS.85).aspx\#library\_keeping\_in\_sync

 

 



