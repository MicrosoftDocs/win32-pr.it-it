---
description: Per impostazione predefinita, a Windows vista Pannello di controllo gli elementi non vengono visualizzati quando Windows viene eseguito in modalità sicura.
title: Accesso al Pannello di controllo in Cassaforte predefinita
ms.topic: article
ms.date: 05/31/2018
ms.assetid: f37bcb0f-9417-4cc4-a57d-4f67a9ccda19
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 777a44c7fe30b0481096a1c5d62c98410277a3bc76169925aff4ae5e59e549d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710791"
---
# <a name="accessing-the-control-panel-in-safe-mode"></a>Accesso al Pannello di controllo in Cassaforte predefinita

Per impostazione predefinita, a Windows vista Pannello di controllo gli elementi non vengono visualizzati quando Windows viene eseguito in modalità sicura. Per consentire la visualizzazione di Pannello di controllo nuovo elemento in modalità sicura, è possibile impostare i valori del Registro di sistema appropriati per il tipo di elemento. I valori vengono interpretati come segue:



| Valore | Significato                                                            |
|-------|--------------------------------------------------------------------|
| 1     | L'elemento deve essere visualizzato solo in modalità provvisoria minima.                  |
| 2     | L'elemento deve essere visualizzato in modalità sicura solo se la rete è abilitata. |
| 3     | L'elemento deve essere sempre visualizzato in qualsiasi forma di modalità sicura.            |



 

Questo esempio illustra le voci necessarie per un elemento implementato come .cpl o .dll file. Specifica che l'elemento deve essere visualizzato in modalità sicura con rete.

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

In questo esempio vengono illustrate le voci necessarie per un elemento implementato come file .exe. Specifica che l'elemento deve essere visualizzato in qualsiasi forma di modalità sicura.

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         System.ControlPanel.EnableInSafeMode = [REG_DWORD] 3
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pannello di controllo elementi](control-panel-applications.md)
</dt> <dt>

[Linee guida sull'esperienza utente](user-experience-guidelines.md)
</dt> <dt>

[Registrazione di Pannello di controllo elementi](registering-control-panel-items.md)
</dt> <dt>

[Uso di CPLApplet](using-cplapplet.md)
</dt> <dt>

[Pannello di controllo di messaggi](message-processing.md)
</dt> <dt>

[Esecuzione di Pannello di controllo elementi](executing-control-panel-items.md)
</dt> <dt>

[Estensione degli elementi di Pannello di controllo sistema](extending-system-control-panel-items.md)
</dt> <dt>

[Assegnazione di Pannello di controllo categorie](assigning-control-panel-categories.md)
</dt> <dt>

[Creazione di collegamenti di attività ricercabili per un Pannello di controllo ricerca](creating-searchable-task-links.md)
</dt> </dl>

 

 



