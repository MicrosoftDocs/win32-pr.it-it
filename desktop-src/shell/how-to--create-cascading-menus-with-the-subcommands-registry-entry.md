---
description: In Windows 7 e versioni successive, è possibile usare la voce SubCommands nel Registro di sistema per creare menu a catena usando la procedura descritta in questo argomento.
title: Creare menu a catena con la voce del Registro di sistema SubCommands
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f12eb473d45a3d3aef1b7cf8e7f6cc51a0d97aa5b9e60ee39681c80af459988
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111801"
---
# <a name="how-to-create-cascading-menus-with-the-subcommands-registry-entry"></a>Come creare menu a catena con la voce del Registro di sistema SubCommands

In Windows 7 e versioni successive, è possibile usare la voce SubCommands nel Registro di sistema per creare menu a catena usando la procedura descritta in questo argomento.

## <a name="instructions"></a>Istruzioni

### <a name="step-1"></a>Passaggio 1:

Creare una nuova sottochiave in **HKEY \_ CLASSES \_ ROOT** ProgID shell , dove ProgID è il tipo di file per cui si vuole \\  \\ aggiungere un menu a cascata.  È possibile assegnare a questa nuova sottochiave il nome che si desidera assegnare. Per il resto di questo argomento, si chiamerà *CascadeMenu*, come illustrato nell'esempio seguente.

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         CascadeMenu
```

### <a name="step-2"></a>Passaggio 2:

Aggiungere una voce denominata "MUIVerb", di tipo **REG \_ SZ** o **REG EXPAND \_ \_ SZ,** alla *sottochiave CascadeMenu.* Assegnare a questa voce un valore stringa, ad esempio "Test Cascade Menu". In genere, questa stringa viene fornita come riferimento alla risorsa nel formato @file ", resource". Il valore (predefinito) per la *sottochiave CascadeMenu* non deve essere impostato.

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         CascadeMenu
            (Default)
            MUIVerb = Test Cascade Menu
```

### <a name="step-3"></a>Passaggio 3:

Aggiungere una voce denominata "SubCommands", di tipo **REG \_ SZ** o **REG EXPAND \_ \_ SZ,** alla *sottochiave CascadeMenu.* Assegnare a questa voce un elenco delimitato da punto e virgola dei verbi che devono essere visualizzati nel menu nell'ordine desiderato.

```
HKEY_CLASSES_ROOT
   ProgID
      Shell
         CascadeMenu
            SubCommands = Windows.delete;Windows.properties;Windows.rename;Windows.cut;Windows.copy;Windows.paste
```

### <a name="step-4"></a>Passaggio 4:

Popolare la sottochiave **CommandStore** con implementazioni di verbi per tutti i metodi di implementazione di verbi statici personalizzati usati nella voce SubCommands. Per esempio:

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

 

 



