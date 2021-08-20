---
description: La chiave HKEY CLASSES ROOT (HKCR) contiene associazioni di estensioni di file e informazioni di registrazione delle classi COM, ad esempio \_ \_ ProgID, CLSID e ID. È destinato principalmente alla compatibilità con il Registro di sistema in Windows a 16 bit.
ms.assetid: b404875f-11e1-48f2-98d2-0378a0646ed3
title: HKEY_CLASSES_ROOT chiave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca75fc0b736c156e2e0dbe8ad07ff84cbbaa0a9ee1484de74e4f670703b2d875
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885683"
---
# <a name="hkey_classes_root-key"></a>HKEY \_ CLASSES \_ ROOT Key

La **chiave HKEY \_ CLASSES \_ ROOT** (**HKCR**) contiene le associazioni di estensioni di file e le informazioni di registrazione delle classi COM, ad esempio [ProgID,](../com/-progid--key.md) [CLSID](../com/clsid-key-hklm.md)e [ID](../com/interface-key.md). È destinato principalmente alla compatibilità con il Registro di sistema in Windows a 16 bit.

Le informazioni sulla registrazione della classe e sull'estensione del nome file vengono archiviate nelle **chiavi HKEY \_ LOCAL \_ MACHINE** e **HKEY CURRENT \_ \_ USER.** La **chiave HKEY \_ LOCAL MACHINE \_ Software \\ \\ Classes** contiene le impostazioni predefinite che possono essere applicate a tutti gli utenti nel computer locale. La **chiave HKEY \_ CURRENT USER \_ Software \\ \\ Classes** contiene impostazioni che si applicano solo all'utente interattivo. La **chiave RADICE HKEY \_ CLASSES \_** fornisce una visualizzazione del Registro di sistema che unisce le informazioni provenienti da queste due origini. **HKEY \_ CLASSES \_ ROOT** fornisce anche questa visualizzazione unita per le applicazioni progettate per le versioni precedenti di Windows.

Le impostazioni specifiche dell'utente hanno la priorità rispetto alle impostazioni predefinite. Ad esempio, l'impostazione predefinita potrebbe specificare una particolare applicazione per gestire .doc file. Tuttavia, un utente può eseguire l'override di questa impostazione specificando un'applicazione diversa nel Registro di sistema.

Le funzioni del Registro di sistema, ad esempio [**RegOpenKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regopenkeyexa) o [**RegQueryValueEx,**](/windows/desktop/api/Winreg/nf-winreg-regqueryvalueexa) consentono di specificare la **chiave ROOT HKEY \_ CLASSES. \_** Quando si chiamano queste funzioni da un processo in esecuzione nell'account utente interattivo, il sistema unisce le impostazioni predefinite in **HKEY \_ LOCAL MACHINE Software \_ \\ \\ Classes** con le impostazioni dell'utente interattivo in **HKEY CURRENT USER Software \_ \_ \\ \\ Classes**. Per altre informazioni sul modo in cui queste impostazioni vengono unite, vedere Visualizzazione unita [di HKEY \_ CLASSES \_ ROOT](merged-view-of-hkey-classes-root.md).

Per modificare le impostazioni per l'utente interattivo, archiviare le modifiche in **HKEY \_ CURRENT USER Software \_ \\ \\ Classes** anziché **HKEY CLASSES \_ \_ ROOT**.

Per modificare le impostazioni predefinite, archiviare le modifiche in **HKEY \_ LOCAL MACHINE Software \_ \\ \\ Classes**. Se si scrivono chiavi in una chiave in **HKEY \_ CLASSES \_ ROOT**, il sistema archivia le informazioni in **HKEY \_ LOCAL MACHINE \_ \\ Software \\ Classes**. Se si scrivono valori in una chiave in **HKEY \_ CLASSES \_ ROOT** e la chiave esiste già in **HKEY \_ CURRENT USER \_ Software \\ \\ Classes**, il sistema archivierà le informazioni in questa chiave anziché in **HKEY LOCAL MACHINE Software \_ \_ \\ \\ Classes**.

I processi in esecuzione in un contesto di sicurezza diverso da quello dell'utente interattivo non devono usare la **chiave ROOT HKEY \_ CLASSES \_** con le funzioni del Registro di sistema. Tali processi possono invece aprire in modo esplicito la **chiave HKEY \_ LOCAL MACHINE \_ Software \\ \\ Classes** per accedere alle impostazioni predefinite. Per aprire una chiave del Registro di sistema che unisce il contenuto delle classi software **HKEY \_ LOCAL \_ MACHINE \\ \\** con le impostazioni per un utente specificato, questi processi possono chiamare la [**funzione RegOpenUserClassesRoot.**](/windows/desktop/api/Winreg/nf-winreg-regopenuserclassesroot) Ad esempio, un [](/windows/desktop/SecAuthZ/client-impersonation) thread che rappresenta un client può chiamare **RegOpenUserClassesRoot** se deve recuperare una visualizzazione unita per il client rappresentato. Si noti **che RegOpenUserClassesRoot** ha esito negativo se il profilo utente per l'utente specificato non è stato caricato. Il sistema carica automaticamente il profilo per l'utente interattivo durante l'accesso. Per altri utenti, è necessario chiamare la [**funzione LoadUserProfile**](/windows/win32/api/userenv/nf-userenv-loaduserprofilea) per caricare in modo esplicito il profilo dell'utente.

Se un'applicazione viene eseguita con diritti di amministratore e controllo dell'account utente è disabilitato, il runtime COM ignora la configurazione COM per utente e accede solo alla configurazione COM per computer. Le applicazioni che richiedono diritti di amministratore devono registrare gli oggetti COM dipendenti durante l'installazione nell'archivio di configurazione COM per computer (**HKEY \_ LOCAL MACHINE Software \_ \\ \\ Classes**). Per altre informazioni, vedere [AC: UAC: COM Per-User Configuration](/previous-versions/bb756926(v=msdn.10)).

**Windows Server 2003 e Windows XP/2000:** Le applicazioni possono registrare oggetti COM dipendenti nell'archivio di configurazione COM per computer o per utente (**HKEY \_ LOCAL MACHINE Software \_ \\ \\ Classes** o **HKEY CURRENT USER Software \_ \_ \\ \\ Classes**).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[HKEY \_ CLASSES \_ ROOT (Informazioni di riferimento sul Registro di sistema di Resource Kit)](/previous-versions/windows/it-pro/windows-server-2003/cc739822(v=ws.10))
</dt> </dl>

 

 
