---
description: La funzione RegOpenUserClassesRoot fornisce una visualizzazione unita per i processi, ad esempio i servizi, che gestiscono client diversi dall'utente interattivo.
ms.assetid: 3815d487-2d58-4ba8-85d2-cae6a642a791
title: Visualizzazione unita di HKEY_CLASSES_ROOT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8597db976922db9ca348488b0092c41ba7c7489
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317655"
---
# <a name="merged-view-of-hkey_classes_root"></a>Visualizzazione unita della \_ radice delle classi HKEY \_

La funzione [**RegOpenUserClassesRoot**](/windows/desktop/api/Winreg/nf-winreg-regopenuserclassesroot) fornisce una visualizzazione unita per i processi, ad esempio i servizi, che gestiscono client diversi dall'utente interattivo. In questo caso, la **chiave \_ \_ radice delle classi HKEY** fornisce una visualizzazione del registro di sistema che unisce le informazioni dalle classi **\_ \_ software del computer \\ \\ locale di HKEY** con le informazioni provenienti dalle **\_ \_ \\ \\ classi software utente corrente di HKEY**.

Il sistema utilizza le regole seguenti per unire le informazioni dalle due origini:

-   La visualizzazione unita include tutte le sottochiavi della chiave delle **\_ \_ \\ \\ classi software dell'utente corrente di HKEY** .
-   La visualizzazione unita include tutte le sottochiavi immediate della chiave delle **\_ \_ \\ \\ classi software del computer locale HKEY** che non duplicano le sottochiavi delle **\_ \_ \\ \\ classi software utente correnti di HKEY**.
-   Alla fine di questo argomento è riportato un elenco di sottochiavi disponibili sia nelle classi **\_ \_ \\ \\ software del computer locale HKEY** che nelle **\_ \_ \\ \\ classi software utente corrente di HKEY**. Le sottochiavi immediate di queste chiavi dall'albero **del \_ \_ computer locale HKEY** sono incluse nella visualizzazione unita solo se non sono duplicati di sottochiavi immediate dall'albero **\_ \_ utente corrente di HKEY** . La visualizzazione unita non include il contenuto **del \_ \_ computer locale HKEY** delle sottochiavi duplicate.

Se un'applicazione viene eseguita con diritti di amministratore e il controllo dell'account utente è disabilitato, il runtime COM ignora la configurazione COM per singolo utente e accede solo alla configurazione COM per computer. Le applicazioni che richiedono diritti di amministratore devono registrare gli oggetti COM dipendenti durante l'installazione nell'archivio di configurazione COM per computer (**HKEY \_ \_ \\ \\ le classi software del computer locale**). Per altre informazioni, vedere [AC: UAC: COM Per-User Configuration](/previous-versions/bb756926(v=msdn.10)).

**Windows Server 2003 e Windows XP/2000:** Le applicazioni possono registrare oggetti COM dipendenti nell'archivio di configurazione COM per computer o per singolo utente (**HKEY le \_ \_ \\ \\ classi software del computer locale** o **HKEY \_ \_ \\ \\ le classi software dell'utente corrente**).

Nell'esempio seguente viene illustrato un set di sottochiavi nel **\_ \_ computer locale HKEY** e la HKEY delle chiavi **\_ \_ utente correnti** e la visualizzazione unita risultante della **\_ \_ radice delle classi HKEY**.

**HKEY \_ \_ \\ \\ Classi software del computer locale**    **CLSID**       *2*       *4*          **InprocServer32**          **LocalServer32**       *7*

**HKEY \_ \_ \\ \\ Classi software utente correnti**    **CLSID**       *1*       *4*          **LocalServer**       *6*       *10*          **LocalServer**

**HKEY \_ Classi \_ radice**    **CLSID**       *1*       *2*       *4*          **InprocServer32**          **LocalServer**          **LocalServer32**       *6*       *7*       *10*          **LocalServer**

Le sottochiavi riportate di seguito sono disponibili sia nelle classi **\_ \_ software del computer locale \\ \\ HKEY** che nelle **\_ \_ \\ \\ classi software utente correnti di HKEY**. Dall'albero **del \_ \_ computer locale HKEY** , le sottochiavi immediate di queste chiavi sono incluse nella visualizzazione unita solo se non sono duplicati di sottochiavi immediate dall'albero **\_ \_ utente corrente di HKEY** . La visualizzazione unita non include il contenuto **del \_ \_ computer locale HKEY** delle sottochiavi duplicate.

**\**_ _*\*\\ shellex**  
**\*\\\\ContextMenuHandlers shellex**  
**\*\\\\PropertySheetHandlers shellex**  
**AppID**  
**ClsID**  
**Categorie di componenti**  
**Unità**  
**Unità \\ ShellEx**  
**Unità \\ ShellEx \\ ContextMenuHandlers**  
**Unità \\ ShellEx \\ PropertySheetHandlers**  
**FileType**  
**Cartella**  
**\\ShellEx cartella**  
**Cartella \\ ShellEx \\ ColumnHandler**  
**Cartella \\ ShellEx \\ ContextMenuHandlers**  
**Cartella \\ ShellEx \\ ExtShellFolderViews**  
**Cartella \\ ShellEx \\ PropertySheetHandlers**  
**Componenti del programma di installazione \\**  
**Funzionalità del programma di installazione \\**  
**Prodotti del programma di installazione \\**  
**Interfaccia**  
**MIME**  
**\\Database MIME**  
**Set di caratteri del \\ database MIME \\**  
**Tabella \\ codici del database MIME \\**  
**Tipo di contenuto del \\ database MIME \\**  
**TypeLib**  


 

 
