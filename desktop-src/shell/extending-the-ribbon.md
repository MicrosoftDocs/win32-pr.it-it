---
description: Informazioni su come estendere la barra multifunzione di Esplora risorse.
title: Estensione della barra multifunzione
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0C043FF8-3862-4F02-8700-BB556C4F35B8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 6a0a3af3ac21e0bac0471bc9a987849536303556
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525321"
---
# <a name="extending-the-ribbon"></a>Estensione della barra multifunzione

In Esplora risorse, la barra multifunzione consente di semplificare e rendere più individuabili le attività comuni di gestione dei file degli utenti finali, ma sono state apportate modifiche per gli sviluppatori di app. La barra dei comandi precedente, ad esempio, è stata liberamente estendibile, ma al momento la barra multifunzione è più limitata. Inoltre, la barra multifunzione non viene visualizzata per impostazione predefinita per tutte le estensioni dello spazio dei nomi, quindi è necessario acconsentire esplicitamente per ottenere la barra multifunzione. in caso contrario, si otterrà la barra dei comandi precedente.

Le azioni disponibili per gli utenti sulla barra multifunzione rientrano in tre categorie di estensibilità:

-   L'estendibilità non è necessaria. Esempi: copia, incolla, Elimina. Windows gestisce automaticamente questi verbi.
-   L'estendibilità non è attualmente consentita: esempi: zip, chiusura sessione e altre azioni personalizzate. Utilizzare il menu di scelta rapida per coprire questi scenari.
-   L'estendibilità è incorporata nell'azione stessa. Esempi: ricerca, posta elettronica, stampa, nuovo elemento. È necessario registrarsi per questi verbi per includere l'app o il formato di file nella barra multifunzione.

Questo documento descrive come è possibile acconsentire esplicitamente per ottenere la barra multifunzione e come eseguire la registrazione per gestire i verbi della barra multifunzione specifici.

## <a name="opting-in-to-the-ribbon"></a>Scelta della barra multifunzione

Per acconsentire esplicitamente alla barra multifunzione, l'implementazione di [**IShellFolder2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2) deve specificare la **\_ barra multifunzione EP** in [**IExplorerPaneVisibility:: GetPaneState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerpanevisibility-getpanestate) e restituire **EPS \_ Force** EPS \| **\_ default \_ on**.

## <a name="extending-the-ribbon-for-file-extensions"></a>Estensione della barra multifunzione per le estensioni di file

Questi pulsanti della barra multifunzione sono estendibili in base alle estensioni di file:

-   Estrai tutto
-   Montaggio \| Burn (ISO)
-   Riproduci \| tutto \| Aggiungi a playlist (verbo: Accoda)
-   Apri
-   Modifica
-   Proprietà

Quando si esegue la registrazione per gestire in modo statico i verbi pertinenti per i nuovi tipi di file, la barra multifunzione gestisce i verbi in modo appropriato. Si esegue la registrazione come per i verbi del menu di scelta rapida. Per ulteriori informazioni sulle associazioni di file e sulla registrazione per i verbi, vedere [verbi e associazioni di file](fa-verbs.md) e [creazione di gestori di menu di scelta rapida](context-menu-handlers.md).

## <a name="registering-as-a-default-handler-for-actionids"></a>Registrazione come gestore predefinito per dizionario

Per prima cosa, registrare il ProgId nella sottochiave AssocActionId appropriata. Ogni sottochiave AssocActionId rappresenta un verbo o un'azione che gli utenti possono richiamare dalla barra multifunzione. In questo esempio l'app esegue la registrazione per il ActionID ZipSelection per estendere il pulsante "Estrai tutto" sulla barra multifunzione.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         Explorer.AssocActionId.ZipSelection
            shell
               open
                  command
                     (Default) = %SystemRoot%\[Your App].exe
      Microsoft
         Windows
            CurrentVersion
               Your App Name
                  Capabilities
                     URL Protocol
                     FriendlyTypeName = @%SystemRoot%\explorer.exe,-1234
```

Una volta completata la registrazione, è necessario registrarsi per gestire i protocolli esattamente come si farebbe normalmente, come descritto in [programmi predefiniti](default-programs.md).

 

 



