---
description: In Windows 7 e versioni successive, è possibile usare la sottochiave ExtendedSubCommandsKey per creare menu a cascata estesi.
ms.assetid: 6E8B4FB7-D4DB-4DBC-AF6F-59D02CB6AB13
title: Creare menu a cascata con la voce del registro di sistema ExtendedSubCommandsKey
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 220a38825ae250a0d58d30bc7de93f290f819eb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756515"
---
# <a name="how-to-create-cascading-menus-with-the-extendedsubcommandskey-registry-entry"></a>Come creare menu a cascata con la voce del registro di sistema ExtendedSubCommandsKey

In Windows 7 e versioni successive, è possibile usare la sottochiave **ExtendedSubCommandsKey** per creare menu a cascata estesi.

Lo screenshot seguente è un esempio di menu a cascata esteso.

![screenshot che mostra il menu a cascata esteso per i dispositivi](images/file-assoc/extendedsubcommandskey.png)

Poiché **la \_ \_ radice delle classi HKEY** è una combinazione di **HKEY \_ Current \_ User** e **HKEY \_ Local \_ computer**, è possibile registrare i sottoverbi nella sottochiave **HKEY \_ Current \_ User** \\  \\ **Classes** . Il vantaggio di questa operazione è che non è necessaria l'autorizzazione con privilegi elevati. Altre associazioni di file possono riutilizzare l'intero set di verbi specificando la stessa sottochiave **ExtendedSubCommandsKey** . Se non è necessario riutilizzare questo set di verbi, è possibile elencare i verbi sotto l'elemento padre. In questo caso, assicurarsi che il valore predefinito dell'elemento padre sia vuoto, come illustrato nell'esempio di voce del registro di sistema in questa sezione.

## <a name="instructions"></a>Istruzioni

### <a name="step-1"></a>Passaggio 1:

Creare una sottochiave in **HKEY \_ classi \_ radice** \\ *ProgID* \\ **Shell** \\ *CascadeMenuKey* e assegnare a CascadeMenuKey un nome come *CascadeTest*, ad esempio. Aggiungere quindi una voce MUIVerb di tipo **reg \_ SZ** e assegnarle un nome, ad esempio test Cascade menu 2, come illustrato nell'esempio di registro di sistema seguente.

```
HKEY_CLASSES_ROOT
   txtfile
      shell
         CascadeTest
            MUIVerb = Test Cascade Menu 2
```

### <a name="step-2"></a>Passaggio 2:

Nella sottochiave *CascadeTest* creata aggiungere una sottochiave **ExtendedSubCommandsKey** e quindi aggiungere il documento sottocomandi (di tipo **reg \_ SZ**), ad esempio:

```
HKEY_CLASSES_ROOT
   txtfile
      Shell
         Test Cascade Menu 2
            (Default)
            ExtendedSubCommandsKey
               Layout
               Properties
               Select all
```

Verificare che il valore predefinito della sottochiave del *menu 2 di test Cascade* sia vuoto e visualizzato come **(valore non impostato)**.

### <a name="step-3"></a>Passaggio 3:

Popolare i sottoverbi utilizzando una delle seguenti implementazioni di verbi statici. Si noti che la sottochiave CommandFlags rappresenta i valori EXPCMDFLAGS. Se si desidera aggiungere un separatore prima o dopo la voce di menu a cascata, utilizzare ECF \_ SEPARATORBEFORE (0x20) o ECF \_ SEPARATORAFTER (0x40). Per una descrizione di questi flag di Windows 7 e versioni successive, vedere [**IExplorerCommand:: GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags). ECF \_ SEPARATORBEFORE funziona solo per le voci di menu di primo livello. MUIVerb è di tipo **reg \_ SZ** e CommandFlags è di tipo **reg \_ DWORD**.

```
HKEY_CLASSES_ROOT
   txtile
      Shell
         Test Cascade Menu 2
            (Default)
            ExtendedSubCommandsKey
               Shell
                  cmd1
                     MUIVerb = Notepad
                     command
                        (Default) = %SystemRoot%\system32\notepad.exe %1
                  cmd2
                     MUIVerb = Wordpad
                     CommandFlags = 0x20
                     command
                        (Default) = C:\Program Files\Windows NT\Accessories\wordpad.exe %1
```

## <a name="remarks"></a>Commenti

Lo screenshot seguente illustra i precedenti esempi di voci della chiave del registro di sistema.

![screenshot che mostra un esempio di menu a cascata che mostra le scelte del blocco note e di WordPad](images/file-assoc/testcascademenu2.png)

 

 



