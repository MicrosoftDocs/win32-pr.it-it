---
description: Un consumer logico è un'istanza di una classe consumer di eventi permanente.
ms.assetid: fd984de8-0fe6-4b32-8e8c-4e2db84b4cc0
ms.tgt_platform: multiple
title: Creazione di un consumer logico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9514ce3f1c7982a96692dcdea62ec9bb92ebf99dd4c47cfe1a64b70257dcfc2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030661"
---
# <a name="creating-a-logical-consumer"></a>Creazione di un consumer logico

Un consumer logico è un'istanza di una classe consumer di eventi permanente. Lo scopo principale di un consumer logico è fornire al consumer fisico i parametri per le attività eseguite dal consumer fisico. Per altre informazioni, vedere [Creazione di una nuova classe consumer di eventi permanente.](creating-a-new-permanent-event-consumer-class.md) Il consumer permanente deve avere lo stesso [**CreatorSID**](--eventconsumer.md) nelle istanze di consumer, filtro e associazione. Per altre informazioni, vedere [Ricezione di eventi in modo sicuro.](receiving-events-securely.md) Per un esempio d'uso di un consumer logico, vedere Esecuzione di uno [script](running-a-script-based-on-an-event.md)basato su un evento , che illustra l'uso della classe consumer standard [**ActiveScriptEventConsumer**](activescripteventconsumer.md) per configurare un consumer permanente.

Nella procedura seguente viene descritto come creare un consumer logico.

**Per creare un consumer logico**

1.  Creare un'istanza della classe consumer permanente.
2.  Compilare le proprietà dell'istanza con i parametri dell'azione che il consumer fisico deve eseguire.

L'esempio di codice MOF seguente descrive un consumer logico che contiene uno script.

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

Dopo aver creato il consumer logico, è necessario collegare ogni filtro a un filtro eventi per assegnare l'azione a un evento specifico. Per altre informazioni, vedere [Creazione di un filtro eventi.](creating-an-event-filter.md)

 

 



