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
# <a name="how-to-define-extended-verbs"></a><span data-ttu-id="6026f-104">Come definire i verbi estesi</span><span class="sxs-lookup"><span data-stu-id="6026f-104">How to Define Extended Verbs</span></span>

<span data-ttu-id="6026f-105">È possibile utilizzare il registro di sistema per definire uno o più verbi estesi.</span><span class="sxs-lookup"><span data-stu-id="6026f-105">You can use the registry to define one or more extended verbs.</span></span> <span data-ttu-id="6026f-106">I comandi associati verranno visualizzati solo quando l'utente fa clic con il pulsante destro del mouse su un oggetto mentre si preme il tasto MAIUSC.</span><span class="sxs-lookup"><span data-stu-id="6026f-106">The associated commands will be displayed only when the user right-clicks an object while pressing the SHIFT key.</span></span>

## <a name="instructions"></a><span data-ttu-id="6026f-107">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="6026f-107">Instructions</span></span>


<span data-ttu-id="6026f-108">Per definire un verbo come esteso, è sufficiente aggiungere un valore "Extended" **reg \_ SZ** alla sottochiave del verbo.</span><span class="sxs-lookup"><span data-stu-id="6026f-108">To define a verb as extended, simply add an "extended" **REG\_SZ** value to the verb's subkey.</span></span> <span data-ttu-id="6026f-109">Al valore non devono essere associati dati.</span><span class="sxs-lookup"><span data-stu-id="6026f-109">The value should not have any data associated with it.</span></span> <span data-ttu-id="6026f-110">La voce del registro di sistema di esempio seguente mostra l'esempio della sezione precedente, con "doit" definito come verbo esteso.</span><span class="sxs-lookup"><span data-stu-id="6026f-110">The following sample registry entry shows the example from the previous section, with "doit" defined as an extended verb.</span></span>

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

 

 



