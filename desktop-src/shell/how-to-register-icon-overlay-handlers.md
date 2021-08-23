---
description: Oltre alla normale registrazione Component Object Model (COM), è necessario completare i passaggi seguenti per registrare i gestori di sovrimpressione delle icone.
ms.assetid: 73EE5E69-969B-409E-9E8F-5837720EA0B3
title: Come registrare gestori di sovrimpressione delle icone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a0e62d95b224b131f03c2bd976ddf7c01d7cb3de7ad6995f21568dc7e990d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714911"
---
# <a name="how-to-register-icon-overlay-handlers"></a>Come registrare gestori di sovrimpressione delle icone

Oltre alla normale registrazione Component Object Model (COM), è necessario completare i passaggi seguenti per registrare i gestori di sovrimpressione delle icone.

## <a name="instructions"></a>Istruzioni

### <a name="step-1-create-a-subkey-named-for-the-handler-under-this-key"></a>Passaggio 1: Creare una sottochiave denominata per il gestore sotto questa chiave

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  ShellIconOverlayIdentifiers
```

### <a name="step-2-set-the-default-value-of-the-subkey-to-the-string-form-of-the-objects-class-identifier-clsidguid"></a>Passaggio 2: Impostare il valore predefinito della sottochiave sul formato stringa dell'identificatore di classe dell'oggetto (CLSID)GUID

L'esempio seguente illustra come registrare un gestore di sovrimpressione dell'icona denominato MyOverlay.

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

 

 



