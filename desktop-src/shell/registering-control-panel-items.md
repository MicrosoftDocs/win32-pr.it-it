---
description: Gli elementi del pannello di controllo devono essere registrati per poter essere visualizzati nella finestra del pannello di controllo.
title: Registrazione degli elementi del pannello di controllo
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 6f21f223-a293-47b5-95e9-06b7a4ff1652
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 05c2a652314babc212e17b48198e9441f4d3465d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131843"
---
# <a name="registering-control-panel-items"></a>Registrazione degli elementi del pannello di controllo

Gli elementi del pannello di controllo devono essere registrati per poter essere visualizzati nella finestra del pannello di controllo. Se l'elemento del pannello di controllo viene implementato come parte di un file con estensione exe, viene registrato come oggetto Command. La registrazione è diversa se l'elemento viene implementato come un file con estensione dll che esporta la funzione [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) .

Gli argomenti seguenti illustrano i requisiti specifici:

-   [Come registrare gli elementi del pannello di controllo eseguibile](how-to-register-an-executable-control-panel-item-registration-.md)
-   [Come registrare gli elementi del pannello di controllo DLL](how-to-register-dll-control-panel-item-registration-.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Elementi del pannello di controllo](control-panel-applications.md)
</dt> <dt>

[Linee guida sull'esperienza utente](user-experience-guidelines.md)
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
</dt> <dt>

[Accesso al pannello di controllo in modalità provvisoria in Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
