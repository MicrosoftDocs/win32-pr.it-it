---
description: La responsabilità principale di qualsiasi elemento del pannello di controllo consiste nel visualizzare una finestra che consente all'utente di visualizzare e modificare le impostazioni.
title: Linee guida sull'esperienza utente
ms.topic: article
ms.date: 09/24/2020
ms.assetid: f03a154b-9781-4718-8244-3d57fee0755e
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e25f8885c2444a51d5d5d8cc917121c7f3b26a09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995101"
---
# <a name="user-experience-guidelines"></a>Linee guida sull'esperienza utente

La responsabilità principale di qualsiasi elemento del pannello di controllo consiste nel visualizzare una finestra che consente all'utente di visualizzare e modificare le impostazioni. Vedere le [linee guida sull'esperienza utente dei pannelli di controllo](../uxguide/winenv-ctrl-panels.md) per il comportamento e la progettazione degli elementi del pannello di controllo. Le linee guida descritte in questo argomento mostrano un metodo del flusso di attività per organizzare un elemento del pannello di controllo. Questa operazione inserisce le impostazioni più importanti in un home page. Le impostazioni usate meno di frequente vengono inserite nelle pagine spoke o a cui è possibile accedere dai collegamenti in un riquadro laterale.

Il pannello di controllo include molti elementi che seguono queste linee guida, ad esempio la facilità di accesso al centro e la rete e la condivisione. Gli altri elementi del pannello di controllo usano il formato della finestra delle proprietà della finestra di dialogo a schede come nelle versioni precedenti di Windows. Gli esempi includono l'elemento del mouse e le opzioni Internet. L'utilizzo del formato della finestra delle proprietà deve essere sospeso. Se si creano nuovi elementi del pannello di controllo, è necessario seguire le linee guida per il flusso di attività.

In passato, gli elementi del pannello di controllo venivano inclusi in un pacchetto come file con estensione CPL. Non è più necessario. È necessario implementare nuovi elementi del pannello di controllo come file exe autonomo o come opzione di flag della riga di comando per il file eseguibile principale dell'applicazione.

> [!Note]  
> Nei sistemi a 64 bit gli elementi del pannello di controllo a 32 bit vengono visualizzati nel pannello di controllo quando è selezionata l'opzione **Visualizza cartella elementi del pannello di controllo 32-bit** . Gli elementi a 32 bit devono trovarsi nella cartella% SystemRoot% \\ SysWow64 da visualizzare. Non richiedono ulteriori registrazioni.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Elementi del pannello di controllo](control-panel-applications.md)
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
</dt> <dt>

[Accesso al pannello di controllo in modalità provvisoria](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 



