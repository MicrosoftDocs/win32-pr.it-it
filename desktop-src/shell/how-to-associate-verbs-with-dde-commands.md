---
description: Viene illustrato come richiamare un comando DDE utilizzando un verbo della shell.
ms.assetid: 65DDD992-5E96-447E-9151-2CCA740822A1
title: Come associare i verbi ai comandi DDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7174a22c993d93c347c8a0368fa7d1798362070f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979607"
---
# <a name="how-to-associate-verbs-with-dde-commands"></a>Come associare i verbi ai comandi DDE

La chiamata di un verbo avvia normalmente l'applicazione specificata dalla sottochiave del comando del verbo. Tuttavia, se l'applicazione supporta Dynamic Data Exchange (DDE), è possibile fare in modo che la shell avvii una conversazione DDE.

Per specificare che la chiamata di un verbo deve avviare una conversazione DDE, attenersi alla seguente procedura.

## <a name="instructions"></a>Istruzioni

### <a name="step-1"></a>Passaggio 1:

Aggiungere una sottochiave **DDEExec** alla chiave del verbo.

### <a name="step-2"></a>Passaggio 2:

Impostare il valore predefinito di **DDEExec** sulla stringa di comando DDE.

## <a name="remarks"></a>Commenti

La chiave **DDEExec** dispone di tre sottochiavi facoltative che forniscono un certo controllo sul processo DDE:

-   **applicazione**. Impostare il valore predefinito della sottochiave sul nome dell'applicazione da utilizzare per stabilire la conversazione DDE. Se non è presente alcuna sottochiave dell' **applicazione** , come nome dell'applicazione viene usato il valore predefinito della sottochiave del **comando** del verbo.
-   **argomento**. Impostare il valore predefinito della sottochiave sul nome dell'argomento della conversazione DDE. Se non è presente alcuna sottochiave dell' **argomento** , viene usato System come nome dell'argomento.
-   **ifexec**. Impostare il valore predefinito della sottochiave sul comando DDE da utilizzare se non è possibile avviare la conversazione DDE. Quando l'avvio ha esito negativo, viene avviata l'applicazione specificata dal valore predefinito della sottochiave del **comando** del verbo. Se esiste una chiave **ifexec** , il relativo valore predefinito verrà usato come comando DDE. Se non è presente alcuna sottochiave **ifexec** , il valore predefinito della chiave **DDEExec** verrà usato nuovamente come comando DDE.

Nell'esempio seguente viene specificato che per richiamare il verbo aperto per il programma. 1 viene avviata una conversazione DDE con un comando DDE aperto ("%1") e un nome applicazione di programma.

```
HKEY_CLASSES_ROOT
   MyProgram.1
      (Default) = MyProgram Application
      Shell
         (Default) = doit
         open
            command
               (Default) = C:\MyDir\MyProgram.exe "%1"
            ddeexec
               (Default) = Open("%1")
               application
                  (Default) = MyProgram
```

 

 



