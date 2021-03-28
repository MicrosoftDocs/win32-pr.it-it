---
description: Per impostazione predefinita, a partire da gli elementi del pannello di controllo di Windows Vista non vengono visualizzati quando Windows viene eseguito in modalità provvisoria.
title: Accesso al pannello di controllo in modalità provvisoria
ms.topic: article
ms.date: 05/31/2018
ms.assetid: f37bcb0f-9417-4cc4-a57d-4f67a9ccda19
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 0f7a401bbc22a7f8de3618f844bfe463fa3baa50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977415"
---
# <a name="accessing-the-control-panel-in-safe-mode"></a>Accesso al pannello di controllo in modalità provvisoria

Per impostazione predefinita, a partire da gli elementi del pannello di controllo di Windows Vista non vengono visualizzati quando Windows viene eseguito in modalità provvisoria. Per consentire la visualizzazione di un nuovo elemento del pannello di controllo in modalità provvisoria, è possibile impostare i valori del registro di sistema appropriati per il tipo di elemento. I valori vengono interpretati nel modo seguente:



| Valore | Significato                                                            |
|-------|--------------------------------------------------------------------|
| 1     | L'elemento deve essere visualizzato solo in modalità provvisoria minima.                  |
| 2     | L'elemento deve essere visualizzato in modalità provvisoria solo se la rete è abilitata. |
| 3     | L'elemento deve essere sempre visualizzato in qualsiasi forma di modalità provvisoria.            |



 

Questo esempio mostra le voci necessarie per un elemento implementato come file con estensione CPL o dll. Specifica che l'elemento deve essere visualizzato in modalità provvisoria con la rete.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.ControlPanel.EnableInSafeMode
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_DWORD] 2
```

Questo esempio mostra le voci necessarie per un elemento implementato come file con estensione exe. Specifica che l'elemento deve essere visualizzato in qualsiasi forma di modalità provvisoria.

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         System.ControlPanel.EnableInSafeMode = [REG_DWORD] 3
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Elementi del pannello di controllo](control-panel-applications.md)
</dt> <dt>

[Linee guida sull'esperienza utente](user-experience-guidelines.md)
</dt> <dt>

[Registrazione degli elementi del pannello di controllo](registering-control-panel-items.md)
</dt> <dt>

[Uso di CPLApplet](using-cplapplet.md)
</dt> <dt>

[Elaborazione del messaggio del pannello di controllo](message-processing.md)
</dt> <dt>

[Esecuzione degli elementi del pannello di controllo](executing-control-panel-items.md)
</dt> <dt>

[Estensione degli elementi del pannello di controllo di sistema](extending-system-control-panel-items.md)
</dt> <dt>

[Assegnazione delle categorie del pannello di controllo](assigning-control-panel-categories.md)
</dt> <dt>

[Creazione di collegamenti alle attività ricercabili per un elemento del pannello di controllo](creating-searchable-task-links.md)
</dt> </dl>

 

 



