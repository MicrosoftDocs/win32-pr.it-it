---
description: È possibile usare il Registro di sistema per definire uno o più verbi estesi. I comandi associati verranno visualizzati solo quando l'utente fa clic con il pulsante destro del mouse su un oggetto mentre preme MAIUSC.
ms.assetid: C6E51716-1D4F-454F-9AF4-8D0E486CB885
title: Come definire verbi estesi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef73244a03101de02653625912701b81aa9e8e11d975f96dd417eaa137bfba07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859718"
---
# <a name="how-to-define-extended-verbs"></a>Come definire verbi estesi

È possibile usare il Registro di sistema per definire uno o più verbi estesi. I comandi associati verranno visualizzati solo quando l'utente fa clic con il pulsante destro del mouse su un oggetto mentre preme MAIUSC.

## <a name="instructions"></a>Istruzioni


Per definire un verbo come esteso, è sufficiente aggiungere un valore **\_ REG SZ** "esteso" alla sottochiave del verbo. Al valore non devono essere associati dati. La voce del Registro di sistema di esempio seguente illustra l'esempio della sezione precedente, con "doit" definito come verbo esteso.

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

 

 



