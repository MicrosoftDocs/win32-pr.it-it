---
description: Un consumer logico è un'istanza di una classe di consumer di eventi permanenti.
ms.assetid: fd984de8-0fe6-4b32-8e8c-4e2db84b4cc0
ms.tgt_platform: multiple
title: Creazione di un consumer logico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dcbd62f2eee57a9e254d5700344d7b8da414469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317570"
---
# <a name="creating-a-logical-consumer"></a>Creazione di un consumer logico

Un consumer logico è un'istanza di una classe di consumer di eventi permanenti. Lo scopo principale di un consumer logico è fornire al consumer fisico i parametri per le attività eseguite dal consumer fisico. Per altre informazioni, vedere [creazione di una nuova classe di consumer di eventi permanenti](creating-a-new-permanent-event-consumer-class.md). Il consumer permanente deve avere lo stesso [**CreatorSID**](--eventconsumer.md) nelle istanze consumer, Filter e binding. Per altre informazioni, vedere [ricezione di eventi](receiving-events-securely.md)in modo sicuro. Per un esempio dell'uso di un consumer logico, vedere [esecuzione di uno script basato su un evento](running-a-script-based-on-an-event.md), che mostra l'uso della classe consumer standard [**ActiveScriptEventConsumer**](activescripteventconsumer.md) per configurare un consumer permanente.

Nella procedura riportata di seguito viene descritto come creare un consumer logico.

**Per creare un consumer logico**

1.  Creare un'istanza della classe consumer permanente.
2.  Inserire le proprietà dell'istanza con i parametri dell'azione che il consumer fisico deve eseguire.

Nell'esempio di codice MOF riportato di seguito viene descritto un consumer logico che contiene uno script.

``` syntax
#pragma namespace("\\\\.\\root\\subscription")

instance of ActiveScriptEventConsumer as $CONSUMER
{
    Name = "MyConsumerName";
    ScriptingEngine = "VBScript";
    ScriptText = 

        "Set objFS = CreateObject(\"Scripting.FileSystemObject\")\n"
        "Set objFile = objFS.OpenTextFile(\"C:\\\\ASEC.log\", 8, true);\n"
        "objFile.WriteLine \"Time: \" + new Date() + \";\n"
        "objFile.WriteLine \"Entry made by: \\\"ActiveScript\\\"\";\n"
        "objFile.Close\n";
    
    // this is the Administrators SID in array of bytes format
    CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0}; 
};
```

Dopo aver creato il consumer logico, è necessario collegare ogni filtro a un filtro eventi per assegnare l'azione a un evento specifico. Per ulteriori informazioni, vedere [creazione di un filtro eventi](creating-an-event-filter.md).

 

 



