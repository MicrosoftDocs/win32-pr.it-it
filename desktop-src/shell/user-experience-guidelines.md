---
description: La responsabilità principale di qualsiasi Pannello di controllo elemento è visualizzare una finestra che consente all'utente di visualizzare e modificare le impostazioni.
title: Linee guida sull'esperienza utente
ms.topic: article
ms.date: 09/24/2020
ms.assetid: f03a154b-9781-4718-8244-3d57fee0755e
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 15ef54d44a466f3c766075eae771ccac9d74e20c0622d6092530f1015a538425
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857080"
---
# <a name="user-experience-guidelines"></a>Linee guida sull'esperienza utente

La responsabilità principale di qualsiasi Pannello di controllo elemento è visualizzare una finestra che consente all'utente di visualizzare e modificare le impostazioni. Vedere le [linee guida per l'esperienza utente dei](../uxguide/winenv-ctrl-panels.md) Pannelli di controllo per il comportamento e la progettazione Pannello di controllo elementi. Le linee guida descritte in questo argomento illustrano un metodo del flusso di attività per organizzare un Pannello di controllo elemento. In questo modo, le impostazioni più importanti vengono home page. Le impostazioni usate meno di frequente vengono inserite nelle pagine spoke o a cui si accede dai collegamenti in un riquadro laterale.

Il Pannello di controllo include molti elementi che seguono queste linee guida, ad esempio Centro accessibilità e Centro connessioni di rete e condivisione. Altri Pannello di controllo usano il formato della finestra di dialogo a schede come nelle versioni precedenti di Windows. Ad esempio, l'elemento Mouse e Le opzioni Internet. L'uso del formato della finestra delle proprietà deve essere interrotto. Se si creano nuovi elementi Pannello di controllo, è necessario seguire le linee guida del flusso di attività.

In passato, Pannello di controllo elementi erano in pacchetto come .cpl file. Questo non è più necessario. I Pannello di controllo devono essere implementati come file .exe autonomo o come opzione flag della riga di comando per il file eseguibile principale dell'applicazione.

> [!Note]  
> Nei sistemi a 64 bit, gli elementi Pannello di controllo a 32 bit vengono visualizzati nel Pannello di controllo quando è selezionata l'opzione Visualizza Pannello di controllo elementi a **32 bit.** Gli elementi a 32 bit devono trovarsi nella cartella %SystemRoot% \\ SysWOW64 da visualizzare. Non richiedono ulteriori registrazioni.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pannello di controllo elementi](control-panel-applications.md)
</dt> <dt>

[Registrazione di Pannello di controllo elementi](registering-control-panel-items.md)
</dt> <dt>

[Uso di CPLApplet](using-cplapplet.md)
</dt> <dt>

[Pannello di controllo di messaggi](message-processing.md)
</dt> <dt>

[Esecuzione di Pannello di controllo elementi](executing-control-panel-items.md)
</dt> <dt>

[Estensione degli elementi Pannello di controllo sistema](extending-system-control-panel-items.md)
</dt> <dt>

[Assegnazione di Pannello di controllo categorie](assigning-control-panel-categories.md)
</dt> <dt>

[Creazione di collegamenti di attività ricercabili per un Pannello di controllo ricerca](creating-searchable-task-links.md)
</dt> <dt>

[Accesso al Pannello di controllo in modalità Cassaforte predefinita](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 



