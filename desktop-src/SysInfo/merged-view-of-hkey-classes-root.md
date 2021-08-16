---
description: La funzione RegOpenUserClassesRoot fornisce una visualizzazione unita per i processi, ad esempio i servizi, che gestiscono client diversi dall'utente interattivo.
ms.assetid: 3815d487-2d58-4ba8-85d2-cae6a642a791
title: Visualizzazione unita di HKEY_CLASSES_ROOT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a52b48be32ec524cdac42808d7f4efddfc78854b56133e647d6f5a9b06ae88bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885419"
---
# <a name="merged-view-of-hkey_classes_root"></a>Visualizzazione unita di HKEY \_ CLASSES \_ ROOT

La [**funzione RegOpenUserClassesRoot**](/windows/desktop/api/Winreg/nf-winreg-regopenuserclassesroot) fornisce una visualizzazione unita per i processi, ad esempio i servizi, che gestiscono client diversi dall'utente interattivo. In questo caso, la **chiave HKEY \_ CLASSES \_ ROOT** fornisce una visualizzazione del Registro di sistema che unisce le informazioni delle classi software HKEY LOCAL MACHINE con le informazioni delle classi software **HKEY \_ \_ \\ \\ CURRENT** **\_ \_ USER \\ \\**.

Il sistema usa le regole seguenti per unire le informazioni provenienti dalle due origini:

-   La vista unita include tutte le sottochiavi della **chiave HKEY \_ CURRENT USER \_ Software \\ \\ Classes.**
-   La vista unita include tutte le sottochiavi immediate della chiave **HKEY \_ LOCAL MACHINE \_ Software \\ \\ Classes** che non duplicano le sottochiavi **delle classi software HKEY \_ CURRENT \_ USER \\ \\**.
-   Alla fine di questo argomento è disponibile un elenco di sottochiavi disponibili sia in **HKEY \_ LOCAL MACHINE Software \_ \\ \\ Classes** che **in HKEY CURRENT USER Software \_ \_ \\ \\ Classes**. Le sottochiavi immediate di queste chiavi dall'albero **HKEY \_ LOCAL \_ MACHINE** sono incluse nella visualizzazione unita solo se non sono duplicati di sottochiavi immediate dall'albero **HKEY \_ CURRENT \_ USER.** La vista unita non include il contenuto **HKEY \_ LOCAL \_ MACHINE** delle sottochiavi duplicate.

Se un'applicazione viene eseguita con diritti di amministratore e controllo dell'account utente è disabilitato, il runtime COM ignora la configurazione COM per utente e accede solo alla configurazione COM per computer. Le applicazioni che richiedono diritti di amministratore devono registrare gli oggetti COM dipendenti durante l'installazione nell'archivio di configurazione COM per computer (**HKEY \_ LOCAL MACHINE Software \_ \\ \\ Classes**). Per altre informazioni, vedere [Ac: UAC: COM Per-User Configuration](/previous-versions/bb756926(v=msdn.10)).

**Windows Server 2003 e Windows XP/2000:** Le applicazioni possono registrare oggetti COM dipendenti nell'archivio di configurazione COM per computer o per utente (**HKEY \_ LOCAL MACHINE Software \_ \\ \\ Classes** o **HKEY CURRENT USER Software \_ \_ \\ \\ Classes**).

L'esempio seguente illustra un set di sottochiavi nelle chiavi **HKEY \_ LOCAL \_ MACHINE** e **HKEY \_ CURRENT \_ USER** e la visualizzazione unita risultante **di HKEY CLASSES \_ \_ ROOT**.

**HKEY \_ CLASSI \_ \\ SOFTWARE \\ LOCAL MACHINE**    **CLSID**       *2*       *4*          **inprocserver32**          **localserver32**       *7*

**HKEY \_ CURRENT \_ USER \\ Classi \\ software**    **CLSID**       *1*       *4*          **localserver**       *6*       *10*          **localserver**

**HKEY \_ CLASSES \_ ROOT****CLSID***1**2 4***inprocserver32****localserver localserver32***6 7**10***localserver**                                                                                      

Le sottochiavi seguenti sono disponibili nelle classi software **HKEY \_ LOCAL MACHINE \_ \\ e \\** **HKEY CURRENT USER Software \_ \_ \\ \\ Classes**. Dall'albero **HKEY \_ LOCAL \_ MACHINE,** le sottochiavi immediate di queste chiavi vengono incluse nella visualizzazione unita solo se non sono duplicati di sottochiavi immediate dall'albero **HKEY \_ CURRENT \_ USER.** La vista unita non include il contenuto **HKEY \_ LOCAL \_ MACHINE** delle sottochiavi duplicate.

**\***  
**\*\\shellex**  
**\*\\Shellex \\ ContextMenuHandlers**  
**\*\\Shellex \\ PropertySheetHandlers**  
**AppID**  
**Clsid**  
**Categorie di componenti**  
**Unità**  
**Shellex \\ unità**  
**Unità \\ shellex \\ ContextMenuHandlers**  
**Unità \\ shellex \\ PropertySheetHandlers**  
**Filetype**  
**Cartella**  
**Shellex \\ della cartella**  
**Shell \\ della cartellaex \\ ColumnHandler**  
**Shell \\ di cartelleex \\ ContextMenuHandlers**  
**Shell \\ di cartelleex \\ ExtShellFolderViews**  
**Shell \\ di cartelleex \\ PropertySheetHandlers**  
**Componenti del \\ programma di installazione**  
**Funzionalità del \\ programma di installazione**  
**Prodotti del programma di \\ installazione**  
**Interfaccia**  
**Mime**  
**Mime \\ Database**  
**Set \\ di caratteri del database Mime \\**  
**Tabella \\ codici del database \\ Mime**  
**Tipo \\ di contenuto del database \\ Mime**  
**Typelib**  


 

 
