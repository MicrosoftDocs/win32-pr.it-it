---
description: Informazioni su come estendere la barra multifunzione Windows Explorer.
title: Estensione della barra multifunzione
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0C043FF8-3862-4F02-8700-BB556C4F35B8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 635698461f897a08248ea99bf68d534ea8ad24763f926460d2e9ce64181ba2a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860852"
---
# <a name="extending-the-ribbon"></a>Estensione della barra multifunzione

In Windows Explorer, la barra multifunzione consente di semplificare e individuare le attività comuni di gestione dei file degli utenti finali, ma sono presenti modifiche per gli sviluppatori di app. Ad esempio, la barra dei comandi precedente era liberamente estendibile, ma al momento la barra multifunzione è più limitata. Inoltre, la barra multifunzione non viene visualizzata per impostazione predefinita per tutte le estensioni dello spazio dei nomi, quindi è necessario acconsentire esplicitamente per ottenere la barra multifunzione. In caso contrario, si ottiene la barra dei comandi precedente.

Le azioni disponibili per gli utenti sulla barra multifunzione rientrano in tre categorie di estendibilità:

-   L'estendibilità non è necessaria. Esempi: Copia, Incolla, Elimina. Windows gestisce automaticamente questi verbi.
-   L'estendibilità non è attualmente consentita: Esempi: Zip, Chiudi sessione e altre azioni personalizzate. Usare il menu di scelta rapida per coprire questi scenari.
-   L'estendibilità è incorporata nell'azione stessa. Esempi: Ricerca, Posta elettronica, Stampa, Nuovo elemento. È necessario registrarsi per questi verbi per includere l'app o il formato di file nella barra multifunzione.

Questo documento descrive come è possibile acconsentire esplicitamente per ottenere la barra multifunzione e come registrarsi per gestire verbi della barra multifunzione specifici.

## <a name="opting-in-to-the-ribbon"></a>Consenso esplicito alla barra multifunzione

Per acconsentire esplicitamente alla barra multifunzione, l'implementazione [**di IShellFolder2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2) deve specificare **EP \_ Ribbon** in [**IExplorerPaneVisibility::GetPaneState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerpanevisibility-getpanestate) e restituire **EPS \_ FORCE** \| **EPS \_ DEFAULT \_ ON**.

## <a name="extending-the-ribbon-for-file-extensions"></a>Estensione della barra multifunzione per le estensioni di file

Questi pulsanti della barra multifunzione sono estendibili in base alle estensioni di file:

-   Estrai tutto
-   Mount \| Burn (iso)
-   Riproduci \| tutto Aggiungi a playlist \| (verbo: Accodamento)
-   Apri
-   Modifica
-   Proprietà

Quando si esegue la registrazione per gestire in modo statico i verbi pertinenti per i nuovi tipi di file, la barra multifunzione gestisce i verbi in modo appropriato. La registrazione viene come per i verbi del menu di scelta rapida. Per altre informazioni sulle associazioni di file e sulla registrazione per i verbi, vedere [Verbi](fa-verbs.md) e associazioni di file e [Creazione di gestori di menu di scelta rapida.](context-menu-handlers.md)

## <a name="registering-as-a-default-handler-for-actionids"></a>Registrazione come gestore predefinito per ActionIds

Registrare prima di tutto ProgId nella sottochiave AssocActionId appropriata. Ogni sottochiave AssocActionId rappresenta un verbo o un'azione che gli utenti possono richiamare dalla barra multifunzione. In questo esempio l'app si registra per ZipSelection ActionID per estendere il pulsante "Estrai tutto" sulla barra multifunzione.

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

Al termine della registrazione, è necessario eseguire la registrazione per gestire i protocolli come si farebbe normalmente, come descritto in [Programmi predefiniti](default-programs.md).

 

 



