---
description: Oltre alla normale registrazione di Component Object Model (COM), è necessario completare i passaggi seguenti per registrare i gestori di sovrimpressione delle icone.
ms.assetid: 73EE5E69-969B-409E-9E8F-5837720EA0B3
title: Come registrare i gestori di sovrimpressione delle icone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cb58747adc9b754481f43fec825a4588e1606ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994656"
---
# <a name="how-to-register-icon-overlay-handlers"></a><span data-ttu-id="ef75f-103">Come registrare i gestori di sovrimpressione delle icone</span><span class="sxs-lookup"><span data-stu-id="ef75f-103">How to Register Icon Overlay Handlers</span></span>

<span data-ttu-id="ef75f-104">Oltre alla normale registrazione di Component Object Model (COM), è necessario completare i passaggi seguenti per registrare i gestori di sovrimpressione delle icone.</span><span class="sxs-lookup"><span data-stu-id="ef75f-104">In addition to normal Component Object Model (COM) registration, the following steps must be completed in order to register icon overlay handlers.</span></span>

## <a name="instructions"></a><span data-ttu-id="ef75f-105">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="ef75f-105">Instructions</span></span>

### <a name="step-1-create-a-subkey-named-for-the-handler-under-this-key"></a><span data-ttu-id="ef75f-106">Passaggio 1: creare una sottochiave denominata per il gestore in questa chiave</span><span class="sxs-lookup"><span data-stu-id="ef75f-106">Step 1: Create a subkey named for the handler under this key</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  ShellIconOverlayIdentifiers
```

### <a name="step-2-set-the-default-value-of-the-subkey-to-the-string-form-of-the-objects-class-identifier-clsidguid"></a><span data-ttu-id="ef75f-107">Passaggio 2: impostare il valore predefinito della sottochiave sul formato stringa del GUID dell'identificatore di classe (CLSID) dell'oggetto</span><span class="sxs-lookup"><span data-stu-id="ef75f-107">Step 2: Set the default value of the subkey to the string form of the object's class identifier (CLSID)GUID</span></span>

<span data-ttu-id="ef75f-108">Nell'esempio seguente viene illustrato come registrare un gestore sovrimpressione di icona denominato sovrimpressione.</span><span class="sxs-lookup"><span data-stu-id="ef75f-108">The following example illustrates how to register an icon overlay handler named MyOverlay.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  ShellIconOverlayIdentifiers
                     MyOverlay
                        (Default) = {MyOverlay CLSID GUID}
```

 

 



