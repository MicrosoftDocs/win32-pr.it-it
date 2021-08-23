---
description: In questa sezione viene illustrata la creazione di menu di scelta rapida e l'implementazione di gestori di menu di scelta rapida (verbo).
title: Menu di scelta rapida e gestori del menu di scelta rapida
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 956f3b10-2bc6-4f1f-a6ed-7184f94b545a
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 5c091588ff3fefb94d7cd06656c4d7206156b03932c4876f20ad0f26aa03b8b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119715731"
---
# <a name="shortcut-context-menus-and-shortcut-menu-handlers"></a>Menu di scelta rapida e gestori del menu di scelta rapida

In questa sezione viene illustrata la creazione di menu di scelta rapida e l'implementazione di gestori di menu di scelta rapida (verbo).

Questa sezione sui tipi di file e sulle associazioni di file è organizzata come segue:

-   [Verbi e associazioni di file](fa-verbs.md)
-   [Scelta di un metodo di menu di scelta rapida statico o dinamico](shortcut-choose-method.md)
-   [Procedure consigliate per gestori di menu di scelta rapida e più verbi](verbs-best-practices.md)
-   [Creazione di gestori del menu di scelta rapida](context-menu-handlers.md)
-   [Creazione di menu a cascata statici](creating-static-cascading-menus.md)
-   [Come eliminare e controllare la visibilità dei verbi](how-to-suppress-and-control-visibility.md)
-   [Come usare il modello di selezione dei verbi](how-to-employ-the-verb-selection-model.md)
-   [Come usare gli attributi degli elementi](how-to-use-item-attributes.md)
-   [Come implementare verbi personalizzati per le cartelle tramite Desktop.ini](how-to-implement-custom-verbs-for-folders-through-desktop-ini.md)
-   [Personalizzazione di un menu di scelta rapida tramite verbi dinamici](shortcut-menu-using-dynamic-verbs.md)
-   [Come implementare l'interfaccia IContextMenu](how-to-implement-the-icontextmenu-interface.md)
-   [Riferimento al menu di scelta rapida](context-menu-reference.md)

## <a name="additional-resources"></a>Risorse aggiuntive

Per informazioni concettuali correlate, vedere gli argomenti seguenti:

-   [Introduzione alle associazioni di file](fa-intro.md).
-   Per estendere la shell con gestori di tipi di file, vedere [Creazione di gestori di estensioni della shell.](handlers.md)
-   Per creare un archivio dati shell, vedere [Implementazione delle interfacce dell'oggetto cartella di base.](nse-implement.md)

Per informazioni di riferimento correlate, vedere gli argomenti seguenti:

-   Per eseguire un verbo su un elemento della shell, vedere il [**metodo InvokeVerb.**](folderitem-invokeverb.md)
-   Per recuperare una raccolta di verbi che possono essere eseguiti su un elemento della shell, vedere il [**metodo Verbs.**](folderitem-verbs.md)
-   Per eseguire un'operazione su un file specificato, vedere le funzioni [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) [**o ShellExecuteEx.**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)

 

 



