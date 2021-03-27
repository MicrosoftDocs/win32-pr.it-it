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
# <a name="how-to-register-icon-overlay-handlers"></a>Come registrare i gestori di sovrimpressione delle icone

Oltre alla normale registrazione di Component Object Model (COM), è necessario completare i passaggi seguenti per registrare i gestori di sovrimpressione delle icone.

## <a name="instructions"></a>Istruzioni

### <a name="step-1-create-a-subkey-named-for-the-handler-under-this-key"></a>Passaggio 1: creare una sottochiave denominata per il gestore in questa chiave

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  ShellIconOverlayIdentifiers
```

### <a name="step-2-set-the-default-value-of-the-subkey-to-the-string-form-of-the-objects-class-identifier-clsidguid"></a>Passaggio 2: impostare il valore predefinito della sottochiave sul formato stringa del GUID dell'identificatore di classe (CLSID) dell'oggetto

Nell'esempio seguente viene illustrato come registrare un gestore sovrimpressione di icona denominato sovrimpressione.

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

 

 



