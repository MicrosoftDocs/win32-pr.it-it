---
description: Illustra la chiamata di un comando DDE usando un verbo shell.
ms.assetid: 65DDD992-5E96-447E-9151-2CCA740822A1
title: Come associare verbi ai comandi DDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 216cfca1548ed16dfea2f018fc3a1607d5c29d080f0f54541ace0491813a73d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090581"
---
# <a name="how-to-associate-verbs-with-dde-commands"></a>Come associare verbi ai comandi DDE

La chiamata di un verbo in genere avvia l'applicazione specificata dalla sottochiave del comando del verbo. Tuttavia, se l'applicazione supporta Dynamic Data Exchange (DDE), è possibile fare in modo che la shell avvii una conversazione DDE.

Per specificare che la chiamata di un verbo deve avviare una conversazione DDE, seguire questa procedura.

## <a name="instructions"></a>Istruzioni

### <a name="step-1"></a>Passaggio 1:

Aggiungere una **sottochiave ddeexec** alla chiave del verbo.

### <a name="step-2"></a>Passaggio 2:

Impostare il valore predefinito **di ddeexec sulla** stringa di comando DDE.

## <a name="remarks"></a>Commenti

La **chiave ddeexec** ha tre sottochiavi facoltative che forniscono un certo controllo sul processo DDE:

-   **applicazione**. Impostare il valore predefinito di questa sottochiave sul nome dell'applicazione da usare per stabilire la conversazione DDE. Se non è presente **alcuna sottochiave** dell'applicazione, come nome dell'applicazione viene usato il valore predefinito della sottochiave **del** comando del verbo.
-   **Argomento**. Impostare il valore predefinito di questa sottochiave sul nome dell'argomento della conversazione DDE. Se non è presente alcuna **sottochiave** dell'argomento, come nome dell'argomento viene usato System.
-   **ifexec**. Impostare il valore predefinito di questa sottochiave sul comando DDE da usare se non è possibile avviare la conversazione DDE. Quando l'avvio ha esito negativo, viene avviata l'applicazione specificata dal valore predefinito della sottochiave **del** comando del verbo. Se esiste **una chiave ifexec,** il relativo valore predefinito verrà quindi usato come comando DDE. Se non è presente **alcuna sottochiave ifexec,** il valore predefinito della **chiave ddeexec** verrà usato nuovamente come comando DDE.

L'esempio seguente specifica che richiamando il verbo aperto per MyProgram.1 viene avviata una conversazione DDE con un comando DDE Open("%1") e un nome di applicazione MyProgram.

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

 

 



