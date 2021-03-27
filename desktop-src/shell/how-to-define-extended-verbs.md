---
description: È possibile utilizzare il registro di sistema per definire uno o più verbi estesi. I comandi associati verranno visualizzati solo quando l'utente fa clic con il pulsante destro del mouse su un oggetto mentre si preme il tasto MAIUSC.
ms.assetid: C6E51716-1D4F-454F-9AF4-8D0E486CB885
title: Come definire i verbi estesi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb4bd8cca04b40bb0b0b77bab5fd7546fd5bff45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979578"
---
# <a name="how-to-define-extended-verbs"></a>Come definire i verbi estesi

È possibile utilizzare il registro di sistema per definire uno o più verbi estesi. I comandi associati verranno visualizzati solo quando l'utente fa clic con il pulsante destro del mouse su un oggetto mentre si preme il tasto MAIUSC.

## <a name="instructions"></a>Istruzioni


Per definire un verbo come esteso, è sufficiente aggiungere un valore "Extended" **reg \_ SZ** alla sottochiave del verbo. Al valore non devono essere associati dati. La voce del registro di sistema di esempio seguente mostra l'esempio della sezione precedente, con "doit" definito come verbo esteso.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      (Default) = MyProgram Application
      Shell
         (Default) = doit
         open
            command
               (Default) = C:\MyDir\MyProgram.exe "%1"
         doit
            (Default) = &Do It
            extended
            command
               (Default) = C:\MyDir\MyProgram.exe /d "%1"
         print
            command
               (Default) = C:\MyDir\MyProgram.exe /p "%1"
         printto
            command
               (Default) = C:\MyDir\MyProgram.exe /p "%1" "%2" %3 %4
```

 

 



