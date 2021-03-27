---
description: In Windows 7 e versioni successive, è possibile usare la voce sottocomandi nel registro di sistema per creare menu a cascata usando la procedura descritta in questo argomento.
title: Creare menu a cascata con la voce del registro di sistema sottocomandi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8b1168daae5ea927f079c66eb436c099f8b3d96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994693"
---
# <a name="how-to-create-cascading-menus-with-the-subcommands-registry-entry"></a>Come creare menu a cascata con la voce del registro di sistema sottocomandi

In Windows 7 e versioni successive, è possibile usare la voce sottocomandi nel registro di sistema per creare menu a cascata usando la procedura descritta in questo argomento.

## <a name="instructions"></a>Istruzioni

### <a name="step-1"></a>Passaggio 1:

Creare una nuova sottochiave in **HKEY \_ classi \_ radice** \\ *ProgID* \\ **Shell**, dove *ProgID* è il tipo di file per cui si vuole aggiungere un menu a cascata. È possibile assegnare alla nuova sottochiave un nome qualsiasi. Nella parte restante di questo argomento verrà chiamato *CascadeMenu*, come illustrato nell'esempio seguente.

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         CascadeMenu
```

### <a name="step-2"></a>Passaggio 2:

Aggiungere una voce denominata "MUIVerb", di tipo **reg \_ SZ** o **reg \_ expand \_ SZ**, alla sottochiave *CascadeMenu* . Assegnare a questa voce un valore stringa, ad esempio "menu test Cascade". In genere, questa stringa viene fornita come riferimento a una risorsa nel formato " @file , Resource". Il valore (predefinito) per la sottochiave *CascadeMenu* non deve essere impostato.

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         CascadeMenu
            (Default)
            MUIVerb = Test Cascade Menu
```

### <a name="step-3"></a>Passaggio 3:

Aggiungere una voce denominata "subcommands", di tipo **reg \_ SZ** o **reg \_ expand \_ SZ**, alla sottochiave *CascadeMenu* . Assegnare a questa voce un elenco delimitato da punti e virgola dei verbi che devono essere visualizzati nel menu, nell'ordine di visualizzazione desiderato.

```
HKEY_CLASSES_ROOT
   ProgID
      Shell
         CascadeMenu
            SubCommands = Windows.delete;Windows.properties;Windows.rename;Windows.cut;Windows.copy;Windows.paste
```

### <a name="step-4"></a>Passaggio 4:

Popolare la sottochiave **CommandStore** con le implementazioni dei verbi per tutti i metodi di implementazione di verbi statici personalizzati usati nella voce dei sottocomandi. Per esempio:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  CommandStore
                     Shell
                        VerbName
                           command
                              (Default) = notepad.exe %1
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di menu a cascata statici](creating-static-cascading-menus.md)
</dt> </dl>

 

 



