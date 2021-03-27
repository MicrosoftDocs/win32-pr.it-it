---
description: In questa sezione viene illustrata la creazione di menu di scelta rapida (contesto) e l'implementazione di gestori di menu di scelta rapida.
title: Menu di scelta rapida (contesto) e gestori di menu di scelta rapida
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 956f3b10-2bc6-4f1f-a6ed-7184f94b545a
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 286dd9c860ae79e5124439439da97f206b4aa436
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225931"
---
# <a name="shortcut-context-menus-and-shortcut-menu-handlers"></a>Menu di scelta rapida (contesto) e gestori di menu di scelta rapida

In questa sezione viene illustrata la creazione di menu di scelta rapida (contesto) e l'implementazione di gestori di menu di scelta rapida.

Questa sezione relativa ai tipi di file e alle associazioni di file è organizzata nel modo seguente:

-   [Verbi e associazioni di file](fa-verbs.md)
-   [Scelta di un metodo di menu di scelta rapida statico o dinamico](shortcut-choose-method.md)
-   [Procedure consigliate per i gestori di menu di scelta rapida e più verbi](verbs-best-practices.md)
-   [Creazione di gestori di menu di scelta rapida](context-menu-handlers.md)
-   [Creazione di menu a cascata statici](creating-static-cascading-menus.md)
-   [Come escludere e controllare la visibilità del verbo](how-to-suppress-and-control-visibility.md)
-   [Come utilizzare il modello di selezione dei verbi](how-to-employ-the-verb-selection-model.md)
-   [Come usare gli attributi degli elementi](how-to-use-item-attributes.md)
-   [Come implementare verbi personalizzati per le cartelle tramite Desktop.ini](how-to-implement-custom-verbs-for-folders-through-desktop-ini.md)
-   [Personalizzazione di un menu di scelta rapida tramite verbi dinamici](shortcut-menu-using-dynamic-verbs.md)
-   [Come implementare l'interfaccia IContextMenu](how-to-implement-the-icontextmenu-interface.md)
-   [Riferimento al menu di scelta rapida](context-menu-reference.md)

## <a name="additional-resources"></a>Risorse aggiuntive

Per informazioni di base concettuali correlate, vedere gli argomenti seguenti:

-   [Introduzione alle associazioni di file](fa-intro.md).
-   Per estendere la shell con i gestori di tipi di file, vedere [creazione di gestori di estensioni della shell](handlers.md).
-   Per creare un archivio dati della shell, vedere [Implementing the Basic Folder Object Interfaces](nse-implement.md).

Per informazioni di riferimento correlate documentazione, vedere gli argomenti seguenti:

-   Per eseguire un verbo su un elemento della shell, vedere il metodo [**InvokeVerb**](folderitem-invokeverb.md) .
-   Per recuperare una raccolta di verbi che possono essere eseguiti su un elemento della shell, vedere il metodo [**verbs**](folderitem-verbs.md) .
-   Per eseguire un'operazione su un file specificato, vedere le funzioni [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) o [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) .

 

 



