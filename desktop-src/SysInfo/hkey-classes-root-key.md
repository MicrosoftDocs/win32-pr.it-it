---
description: La \_ chiave radice delle classi HKEY \_ (HKCR) contiene le associazioni dell'estensione di file e le informazioni di registrazione della classe com, ad esempio ProgID, CLSID e IID. È destinato principalmente alla compatibilità con il registro di sistema in Windows a 16 bit.
ms.assetid: b404875f-11e1-48f2-98d2-0378a0646ed3
title: Chiave di HKEY_CLASSES_ROOT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e7aebe0e59424eb5ff7584fe61c2c5089eb887b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884809"
---
# <a name="hkey_classes_root-key"></a>\_Chiave radice delle classi HKEY \_

La **chiave \_ \_ radice delle classi HKEY** (**HKCR**) contiene le associazioni dell'estensione di file e le informazioni di registrazione della classe com, ad esempio [ProgID](../com/-progid--key.md), [CLSID](../com/clsid-key-hklm.md)e [IID](../com/interface-key.md). È destinato principalmente alla compatibilità con il registro di sistema in Windows a 16 bit.

Le informazioni relative alla registrazione e all'estensione di file della classe vengono archiviate nel **\_ \_ computer locale HKEY** e nelle chiavi **\_ \_ utente correnti di HKEY** . La **chiave \_ \_ \\ \\ classi software del computer locale HKEY** contiene le impostazioni predefinite che possono essere applicate a tutti gli utenti nel computer locale. La **chiave \_ \_ \\ \\ classi software dell'utente corrente di HKEY** contiene impostazioni che si applicano solo all'utente interattivo. La **chiave \_ \_ radice delle classi HKEY** fornisce una visualizzazione del registro di sistema che unisce le informazioni di queste due origini. **HKEY \_ La \_ radice delle classi** fornisce anche questa visualizzazione unita per le applicazioni progettate per le versioni precedenti di Windows.

Le impostazioni specifiche dell'utente hanno priorità rispetto alle impostazioni predefinite. Ad esempio, l'impostazione predefinita potrebbe specificare un'applicazione specifica per gestire i file con estensione doc. Tuttavia, un utente può eseguire l'override di questa impostazione specificando un'applicazione diversa nel registro di sistema.

Le funzioni del registro di sistema, ad esempio [**RegOpenKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regopenkeyexa) o [**RegQueryValueEx**](/windows/desktop/api/Winreg/nf-winreg-regqueryvalueexa) , consentono di specificare la chiave **\_ \_ radice delle classi HKEY** . Quando si chiamano queste funzioni da un processo in esecuzione nell'account utente interattivo, il sistema unisce le impostazioni predefinite nelle **\_ \_ \\ \\ classi software del computer locale di HKEY** con le impostazioni dell'utente interattivo **in \_ \_ classi del \\ software \\ utente corrente di HKEY**. Per altre informazioni sull'Unione di queste impostazioni, vedere [visualizzazione unita della radice delle \_ classi \_ HKEY](merged-view-of-hkey-classes-root.md).

Per modificare le impostazioni dell'utente interattivo, archiviare le modifiche in **HKEY \_ \_ \\ \\ classi software utente corrente** anziché **HKEY \_ classi \_ radice**.

Per modificare le impostazioni predefinite, archiviare le modifiche in **HKEY \_ le \_ \\ \\ classi software del computer locale**. Se si scrivono chiavi in una chiave in **HKEY \_ classi \_ radice**, il sistema archivia le informazioni in **\_ classi del \_ \\ software \\ del computer locale di HKEY**. Se si scrivono i valori in una chiave **nella \_ \_ radice delle classi HKEY** e la chiave esiste già **in \_ \_ \\ \\ classi software utente correnti di HKEY**, il sistema memorizzerà le informazioni in tale posizione invece che nelle **\_ \_ \\ \\ classi software del computer locale HKEY**.

I processi in esecuzione in un contesto di sicurezza diverso da quello dell'utente interattivo non devono utilizzare la chiave **\_ \_ radice delle classi HKEY** con le funzioni del registro di sistema. Al contrario, questi processi possono aprire in modo esplicito la chiave delle **\_ \_ \\ \\ classi software del computer locale HKEY** per accedere alle impostazioni predefinite. Per aprire una chiave del registro di sistema che unisce il contenuto delle **\_ \_ \\ \\ classi software del computer locale HKEY** con le impostazioni per un utente specifico, questi processi possono chiamare la funzione [**RegOpenUserClassesRoot**](/windows/desktop/api/Winreg/nf-winreg-regopenuserclassesroot) . [Un thread che rappresenta un client](/windows/desktop/SecAuthZ/client-impersonation) può ad esempio chiamare **RegOpenUserClassesRoot** se è necessario recuperare una visualizzazione unita per il client rappresentato. Si noti che **RegOpenUserClassesRoot** ha esito negativo se il profilo utente per l'utente specificato non è stato caricato. Quando si effettua l'accesso, il sistema carica automaticamente il profilo per l'utente interattivo. Per gli altri utenti, è necessario chiamare la funzione [**LoadUserProfile**](/windows/win32/api/userenv/nf-userenv-loaduserprofilea) per caricare in modo esplicito il profilo dell'utente.

Se un'applicazione viene eseguita con diritti di amministratore e il controllo dell'account utente è disabilitato, il runtime COM ignora la configurazione COM per singolo utente e accede solo alla configurazione COM per computer. Le applicazioni che richiedono diritti di amministratore devono registrare gli oggetti COM dipendenti durante l'installazione nell'archivio di configurazione COM per computer (**HKEY \_ \_ \\ \\ le classi software del computer locale**). Per altre informazioni, vedere [AC: UAC: COM Per-User Configuration](/previous-versions/bb756926(v=msdn.10)).

**Windows Server 2003 e Windows XP/2000:** Le applicazioni possono registrare oggetti COM dipendenti nell'archivio di configurazione COM per computer o per singolo utente (**HKEY le \_ \_ \\ \\ classi software del computer locale** o **HKEY \_ \_ \\ \\ le classi software dell'utente corrente**).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[HKEY \_ classi \_ radice (riferimento al registro di sistema Resource Kit)](/previous-versions/windows/it-pro/windows-server-2003/cc739822(v=ws.10))
</dt> </dl>

 

 
