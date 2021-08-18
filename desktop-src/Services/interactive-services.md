---
description: In genere, i servizi sono applicazioni console progettate per l'esecuzione automatica senza un'interfaccia utente grafica (GUI).
ms.assetid: 3d6e090a-00b1-47d8-a4fb-620f3db8ba9c
title: Servizi interattivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee6b99eb41d26d6740a30a314654d92fdd4522f5597ea6e4cbb2a3d443de8120
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889469"
---
# <a name="interactive-services"></a>Servizi interattivi

In genere, i servizi sono applicazioni console progettate per l'esecuzione automatica senza un'interfaccia utente grafica (GUI). Tuttavia, alcuni servizi possono richiedere un'interazione occasionale con un utente. Questa pagina illustra i modi migliori per interagire con l'utente da un servizio.

> [!IMPORTANT]
> I servizi non possono interagire direttamente con un utente a Windows Vista. Di conseguenza, le tecniche indicate nella sezione Intitolata Uso di un servizio interattivo non devono essere usate nel nuovo codice.

 

## <a name="interacting-with-a-user-from-a-service-indirectly"></a>Interazione indiretta con un utente da un servizio

È possibile usare le tecniche seguenti per interagire con l'utente da un servizio in tutte le versioni supportate di Windows:

-   Visualizzare una finestra di dialogo nella sessione dell'utente usando la [**funzione WTSSendMessage.**](/windows/desktop/api/wtsapi32/nf-wtsapi32-wtssendmessagea)
-   Creare un'applicazione GUI nascosta separata e usare [**la funzione CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) per eseguire l'applicazione nel contesto dell'utente interattivo. Progettare l'applicazione GUI per comunicare con il servizio tramite un metodo di comunicazione interprocesso (IPC), ad esempio named pipe. Il servizio comunica con l'applicazione GUI per indicare quando visualizzare l'interfaccia utente grafica. L'applicazione comunica i risultati dell'interazione dell'utente al servizio in modo che il servizio possa eseguire l'azione appropriata. Si noti che IPC può esporre le interfacce del servizio in rete a meno che non si usi un elenco di controllo di accesso (ACL) appropriato.

    Se il servizio viene eseguito in un sistema multiutente, aggiungere l'applicazione alla chiave seguente in modo che venga eseguita in ogni sessione: **HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion \\ Run**. Se l'applicazione usa named pipe per IPC, il server può distinguere tra più processi utente, fornendo a ogni pipe un nome univoco in base all'ID sessione.

La tecnica seguente è disponibile anche per Windows Server 2003 e Windows XP:

-   Visualizzare una finestra di messaggio chiamando la [**funzione MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) con **MB SERVICE \_ \_ NOTIFICATION**. Questa opzione è consigliata per la visualizzazione di messaggi di stato semplici. Non chiamare **MessageBox durante** l'inizializzazione del servizio o dalla routine [**HandlerEx,**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex) a meno che non venga chiamato da un thread separato, in modo da tornare a Gestione controllo servizi in modo appropriato.

## <a name="using-an-interactive-service"></a>Uso di un servizio interattivo

Per impostazione predefinita, i servizi usano una stazione finestra non [interattiva e](/windows/desktop/winstation/window-stations) non possono interagire con l'utente. Tuttavia, un *servizio interattivo può* visualizzare un'interfaccia utente e ricevere l'input dell'utente.

> [!Caution]  
> I servizi in esecuzione in un contesto di sicurezza con privilegi elevati, ad esempio l'account LocalSystem, non devono creare una finestra sul desktop interattivo perché qualsiasi altra applicazione in esecuzione sul desktop interattivo può interagire con questa finestra. In questo modo il servizio viene esposto a qualsiasi applicazione eseguita da un utente connesso. Inoltre, i servizi in esecuzione come LocalSystem non devono accedere al desktop interattivo chiamando la [**funzione OpenWindowStation**](/windows/desktop/api/winuser/nf-winuser-openwindowstationa) o [**GetThreadDesktop.**](/windows/desktop/api/winuser/nf-winuser-getthreaddesktop)

 

Per creare un servizio interattivo, eseguire le operazioni seguenti quando si chiama la [**funzione CreateService:**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)

1.  Specificare NULL per il *parametro lpServiceStartName* per eseguire il servizio nel contesto dell'account [LocalSystem](localsystem-account.md).
2.  Specificare il flag **SERVICE \_ INTERACTIVE \_ PROCESS.**

Per determinare se un servizio è in esecuzione come servizio interattivo, chiamare la funzione [**GetProcessWindowStation**](/windows/desktop/api/winuser/nf-winuser-getprocesswindowstation) per recuperare un handle per la stazione della finestra e la funzione [**GetUserObjectInformation**](/windows/desktop/api/winuser/nf-winuser-getuserobjectinformationa) per verificare se la stazione finestra ha l'attributo **\_ WSF VISIBLE.**

Si noti tuttavia che la chiave del Registro di sistema seguente contiene un valore, **NoInteractiveServices**, che controlla l'effetto di SERVICE \_ INTERACTIVE \_ PROCESS:

**Controllo \_ \_ \\ \\ CurrentControlSet HKEY \\ LOCAL MACHINE SYSTEM \\ Windows**

Il **valore predefinito di NoInteractiveServices** è 1, il che significa che nessun servizio può essere eseguito in modo interattivo, indipendentemente dal fatto che abbia SERVICE INTERACTIVE **\_ \_ PROCESS**. Quando **NoInteractiveServices è** impostato su 0, i servizi con PROCESSO INTERATTIVO DEL SERVIZIO possono essere eseguiti in modo interattivo. **\_ \_**

**Windows 7, Windows Server 2008 R2, Windows XP e Windows Server 2003:** Il **valore predefinito di NoInteractiveServices** è 0, il che significa che i servizi con SERVICE INTERACTIVE **\_ \_ PROCESS** possono essere eseguiti in modo interattivo. Quando **NoInteractiveServices** è impostato su un valore diverso da zero, nessun servizio avviato successivamente può essere eseguito in modo interattivo, indipendentemente dal fatto che abbia **SERVICE INTERACTIVE \_ \_ PROCESS**.

> [!IMPORTANT]
> Tutti i servizi vengono eseguiti nella sessione 0 di Servizi terminal. Pertanto, se un servizio interattivo visualizza un'interfaccia utente, è visibile solo all'utente che si è connesso alla sessione 0. Poiché non è possibile garantire che l'utente interattivo sia connesso alla sessione 0, non configurare un servizio per l'esecuzione come servizio interattivo in Servizi terminal o in un sistema che supporta il cambio utente rapido (il cambio utente rapido viene implementato tramite Servizi Terminal).

 

 

 
