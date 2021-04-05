---
description: In genere, i servizi sono applicazioni console progettate per l'esecuzione automatica senza un'interfaccia utente grafica (GUI).
ms.assetid: 3d6e090a-00b1-47d8-a4fb-620f3db8ba9c
title: Servizi interattivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57dda3018b4b37e8c5ee56d67cd1db2c56da9b67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884254"
---
# <a name="interactive-services"></a>Servizi interattivi

In genere, i servizi sono applicazioni console progettate per l'esecuzione automatica senza un'interfaccia utente grafica (GUI). Tuttavia, alcuni servizi possono richiedere occasionali interazioni con un utente. In questa pagina vengono illustrati i modi migliori per interagire con l'utente da un servizio.

> [!IMPORTANT]
> I servizi non possono interagire direttamente con un utente a partire da Windows Vista. Pertanto, le tecniche descritte nella sezione intitolata utilizzo di un servizio interattivo non devono essere utilizzate in un nuovo codice.

 

## <a name="interacting-with-a-user-from-a-service-indirectly"></a>Interazione diretta con un utente da un servizio

Per interagire con l'utente da un servizio in tutte le versioni supportate di Windows, è possibile usare le tecniche seguenti:

-   Visualizza una finestra di dialogo nella sessione dell'utente tramite la funzione [**WTSSendMessage**](/windows/desktop/api/wtsapi32/nf-wtsapi32-wtssendmessagea) .
-   Creare un'applicazione GUI nascosta separata e usare la funzione [**CreateProcessAsUser ha**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) per eseguire l'applicazione nel contesto dell'utente interattivo. Progettare l'applicazione GUI per comunicare con il servizio tramite un metodo di comunicazione interprocesso (IPC), ad esempio Named Pipes. Il servizio comunica con l'applicazione GUI per indicare quando visualizzare l'interfaccia utente grafica. L'applicazione comunica nuovamente i risultati dell'interazione dell'utente con il servizio in modo che il servizio possa intraprendere l'azione appropriata. Si noti che IPC può esporre le interfacce del servizio in rete, a meno che non si usi un elenco di controllo di accesso (ACL) appropriato.

    Se il servizio viene eseguito in un sistema multiutente, aggiungere l'applicazione alla chiave seguente in modo che venga eseguita in ogni sessione: **HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run**. Se l'applicazione usa named pipe per IPC, il server può distinguere tra più processi utente assegnando a ogni pipe un nome univoco basato sull'ID di sessione.

La tecnica seguente è disponibile anche per Windows Server 2003 e Windows XP:

-   Consente di visualizzare una finestra di messaggio chiamando la funzione [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) con la **\_ \_ notifica del servizio MB**. Questa operazione è consigliata per la visualizzazione di messaggi di stato semplici. Non chiamare **MessageBox** durante l'inizializzazione del servizio o dalla routine [**HandlerEx**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex) , a meno che non lo si chiami da un thread separato, in modo da tornare al gestore SCM in modo tempestivo.

## <a name="using-an-interactive-service"></a>Uso di un servizio interattivo

Per impostazione predefinita, i servizi usano una [stazione di finestra](/windows/desktop/winstation/window-stations) non interattiva e non possono interagire con l'utente. Tuttavia, un *servizio interattivo* può visualizzare un'interfaccia utente e ricevere l'input dell'utente.

> [!Caution]  
> I servizi in esecuzione in un contesto di sicurezza con privilegi elevati, ad esempio l'account LocalSystem, non devono creare una finestra sul desktop interattivo perché qualsiasi altra applicazione in esecuzione sul desktop interattivo può interagire con questa finestra. In questo modo viene esposto il servizio a qualsiasi applicazione eseguita da un utente che ha eseguito l'accesso. Inoltre, i servizi in esecuzione come LocalSystem non devono accedere al desktop interattivo chiamando la funzione [**OpenWindowStation**](/windows/desktop/api/winuser/nf-winuser-openwindowstationa) o [**GetThreadDesktop**](/windows/desktop/api/winuser/nf-winuser-getthreaddesktop) .

 

Per creare un servizio interattivo, eseguire le operazioni seguenti quando si chiama la funzione [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) :

1.  Specificare NULL per il parametro *lpServiceStartName* per eseguire il servizio nel contesto dell' [account LocalSystem](localsystem-account.md).
2.  Specificare il flag del **\_ \_ processo interattivo del servizio** .

Per determinare se un servizio è in esecuzione come servizio interattivo, chiamare la funzione [**GetProcessWindowStation**](/windows/desktop/api/winuser/nf-winuser-getprocesswindowstation) per recuperare un handle per la stazione della finestra e la funzione [**GetUserObjectInformation**](/windows/desktop/api/winuser/nf-winuser-getuserobjectinformationa) per verificare se la stazione della finestra ha l'attributo **\_ visibile wsf** .

Si noti tuttavia che la chiave del registro di sistema seguente contiene un valore, **NoInteractiveServices**, che controlla l'effetto del \_ processo interattivo del servizio \_ :

**\_Finestre di \_ \\ \\ controllo CurrentControlSet di sistema del \\ computer \\ locale HKEY**

Il valore predefinito di **NoInteractiveServices** è 1, il che significa che nessun servizio può essere eseguito in modo interattivo, indipendentemente dal fatto che disponga di un **\_ \_ processo interattivo di servizio**. Quando **NoInteractiveServices** è impostato su 0, i servizi con **\_ \_ processo interattivo di servizio** possono essere eseguiti in modo interattivo.

**Windows 7, Windows server 2008 R2, Windows XP e Windows server 2003:** Il valore predefinito di **NoInteractiveServices** è 0, il che significa che i servizi con **\_ \_ processo interattivo di servizio** possono essere eseguiti in modo interattivo. Quando **NoInteractiveServices** è impostato su un valore diverso da zero, non è consentito eseguire il servizio in seguito in modo interattivo, indipendentemente dal fatto che disponga di un **\_ \_ processo interattivo di servizio**.

> [!IMPORTANT]
> Tutti i servizi vengono eseguiti nella sessione Servizi Terminal 0. Se pertanto un servizio interattivo Visualizza un'interfaccia utente, è visibile solo all'utente che si è connesso alla sessione 0. Poiché non esiste alcun modo per garantire che l'utente interattivo sia connesso alla sessione 0, non configurare un servizio per l'esecuzione come servizio interattivo in Servizi terminal o in un sistema che supporta il cambio rapido utente (il cambio rapido utente viene implementato tramite Servizi terminal).

 

 

 
