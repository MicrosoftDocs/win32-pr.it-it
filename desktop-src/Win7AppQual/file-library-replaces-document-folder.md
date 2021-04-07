---
description: .
ms.assetid: 80b97bfc-4212-4401-a4a9-d96e2f39be60
title: La libreria di file sostituisce la cartella del documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15431f5fb5fb5e73dbaf171625a0a6582fa7add2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884785"
---
# <a name="file-library-replaces-document-folder"></a>La libreria di file sostituisce la cartella del documento

## <a name="affected-platforms"></a>Piattaforme interessate

**Client** -Windows 7  
**Server** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Effetto sulle funzionalità

**Gravità** -medio  
**Frequenza** -alta  











## <a name="description"></a>Descrizione

Le librerie offrono un'esperienza centralizzata simile a una cartella per l'archiviazione di file, la ricerca e l'accesso in più posizioni, sia locali che remote.

I percorsi predefiniti usati dalle finestre di dialogo file comuni (ad esempio, Apri e Salva) sono stati modificati dalla cartella documenti alla raccolta documenti. L'interfaccia utente è invariata, ma ora l'utente sarà in grado di visualizzare, esplorare ed eseguire ricerche nella libreria usando varie visualizzazioni di disposizione. I file verranno salvati nel percorso di salvataggio predefinito della libreria, a meno che l'utente non modifichi il percorso di salvataggio predefinito o scelga un'altra cartella.

Gli sviluppatori possono creare librerie personalizzate o aggiungere percorsi alle librerie esistenti usando l'interfaccia IShellLibrary. Gli utenti possono trovare le librerie usando il sistema di cartelle note, ad esempio FOLDERID \_ documentsLibrary.

## <a name="manifestation-of-impact"></a>Manifesto di effetto

La libreria è a sua volta un file e non una cartella. Le manipolazioni del percorso potrebbero pertanto causare errori dovuti al tentativo da parte dell'applicazione di concatenare i file ai file.

## <a name="solution"></a>Soluzione

Quando si usa IFileDialog, è necessario usare il metodo GetResult invece della combinazione di GetFolder e GetFileName come nelle versioni precedenti del sistema operativo. Usare le API della shell laddove possibile per interagire con gli elementi nello spazio dei nomi della shell, ad esempio IShellItem, e modificarli.

## <a name="leveraging-feature-capabilities"></a>Sfruttando le funzionalità

Se si vuole creare librerie personalizzate o aggiungere percorsi alle librerie esistenti, è necessario usare l'API IShellLibrary. Le librerie sono stesse cartelle della shell, in modo che sia possibile enumerarle come qualsiasi altra cartella della shell.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Compatibilità, prestazioni, affidabilità e test di usabilità

Utilizzando la finestra di dialogo file comune si garantisce che gli utenti possano salvare direttamente le proprie raccolte.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   **Librerie di Windows:**https://msdn.microsoft.com/library/dd758096(VS.85).aspx
-   **Mantenimento della sincronizzazione con una libreria:**https://msdn.microsoft.com/library/dd758094(VS.85).aspx\#library\_keeping\_in\_sync

 

 



