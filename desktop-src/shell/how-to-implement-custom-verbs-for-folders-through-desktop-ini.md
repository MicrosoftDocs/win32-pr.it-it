---
description: In Windows 7 e versioni successive, è possibile aggiungere verbi a una cartella usando Desktop.ini. Per ulteriori informazioni sui file di Desktop.ini, vedere How to Customize Folders with Desktop.ini.
ms.assetid: F03AB35D-FBFE-46C2-A37F-F70C18219B9A
title: Come implementare verbi personalizzati per le cartelle tramite Desktop.ini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 133726133abe884863a0b4d2abc0cc76aab1310a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979546"
---
# <a name="how-to-implement-custom-verbs-for-folders-through-desktopini"></a>Come implementare verbi personalizzati per le cartelle tramite Desktop.ini

In Windows 7 e versioni successive, è possibile aggiungere verbi a una cartella usando Desktop.ini. Per ulteriori informazioni sui file di Desktop.ini, vedere [How to Customize Folders with Desktop.ini](how-to-customize-folders-with-desktop-ini.md).

> [!Note]  
> I file di Desktop.ini devono essere sempre contrassegnati come nascosti dal **sistema**  +   , in modo che non vengano visualizzati dagli utenti.

 

Per aggiungere verbi personalizzati per le cartelle tramite un file di Desktop.ini, seguire questa procedura.

## <a name="instructions"></a>Istruzioni

### <a name="step-1"></a>Passaggio 1:

Creare una cartella contrassegnata come di sola **lettura** o di **sistema**.

### <a name="step-2"></a>Passaggio 2:

Creare un file di Desktop.ini che includa un \[ . ShellClassInfo \] DirectoryClass = cartella ProgID.

### <a name="step-3"></a>Passaggio 3:

Nel registro di sistema creare **\_ le classi HKEY \_ radice** \\ **ProgID** con un valore CanUseForDirectory. Il valore CanUseForDirectory evita l'utilizzo improprio dei ProgID impostati per non partecipare all'implementazione di verbi personalizzati per le cartelle tramite Desktop.ini.

### <a name="step-4"></a>Passaggio 4:

Aggiungere i verbi nella sottochiave ProgID della **cartella** , ad esempio:

```
HKEY_CLASSES_ROOT
   CustomFolderType
      Shell
         MyVerb
            command
               (Default) = %SystemRoot%\system32\notepad.exe %1\desktop.ini
```

## <a name="remarks"></a>Commenti

> [!Note]  
> Questi verbi possono essere i verbi predefiniti, nel qual caso fare doppio clic sulla cartella per attivare il verbo.

 

 

 



