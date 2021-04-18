---
description: Specificare un'icona e un'etichetta personalizzate per un'unità.
ms.assetid: B6EF7F84-7747-4689-B740-A91CA8E394D7
title: Assegnare un'etichetta e un'icona personalizzate a una lettera di unità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 848c076db443c502a667d67e0b7b49ce51db4ce6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979631"
---
# <a name="how-to-assign-a-custom-icon-and-label-to-a-drive-letter"></a>Come assegnare un'etichetta e un'icona personalizzate a una lettera di unità

Specificare un'icona e un'etichetta personalizzate per un'unità.

## <a name="instructions"></a>Istruzioni

### <a name="step-1-replacing-the-standard-drive-icon-with-a-custom-icon-in-windows-2000"></a>Passaggio 1: sostituzione dell'icona dell'unità standard con un'icona personalizzata in Windows 2000

Per sostituire l'icona dell'unità standard con un'icona personalizzata in Windows 2000, aggiungere una sottochiave denominata per la lettera di unità alla chiave seguente.

```
HKEY_CLASSES_ROOT
   Applications
      Explorer.exe
         Drives
```

Nell'esempio seguente vengono specificate un'icona e un'etichetta personalizzate per l'unità E:. L'icona si trova nel file di \\MyDrive.exe C: mydir \\ con un indice in base zero di tre.

Per Windows 2000:

```
HKEY_CLASSES_ROOT
   Applications
      Explorer.exe
         Drives
            E
               DefaultIcon
                  (Default) = C:\MyDir\MyDrive.exe,3
               DefaultLabel
                  (Default) = MyDrive
```

### <a name="step-2-replacing-the-standard-drive-icon-with-a-custom-icon-in-all-other-versions-of-windows"></a>Passaggio 2: sostituzione dell'icona dell'unità standard con un'icona personalizzata in tutte le altre versioni di Windows

Per sostituire l'icona dell'unità standard con un'icona personalizzata in tutte le versioni di Windows diverse da Windows 2000, aggiungere una sottochiave denominata per la lettera di unità alla chiave seguente.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  DriveIcons
```

Nell'esempio seguente vengono specificate un'icona e un'etichetta personalizzate per l'unità E:. L'icona si trova nel file di \\MyDrive.exe C: mydir \\ con un indice in base zero di tre.

Per tutte le altre versioni di Windows:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  DriveIcons
                     E
                        DefaultIcon
                           (Default) = C:\MyDir\MyDrive.exe,3
                        DefaultLabel
                           (Default) = MyDrive
```

### <a name="step-3-calling-the-shupdateimage-event"></a>Passaggio 3: chiamata all'evento SHUpdateImage

In tutte le versioni di Windows, se si modifica un tipo di file o un'icona di unità, è necessario chiamare anche SHUpdateImage per notificare alla shell di aggiornare le icone attualmente visualizzate.

## <a name="remarks"></a>Commenti

La lettera di unità non deve essere seguita da due punti (:). Aggiungere una sottochiave **DefaultIcon** alla sottochiave della lettera di unità e impostare il relativo valore predefinito su una stringa che contiene la posizione dell'icona. La prima parte della stringa contiene il percorso completo del file dell'icona. Se nel file è presente più di un'icona, il percorso è seguito da una virgola, quindi dall'indice in base zero dell'icona.

 

 



