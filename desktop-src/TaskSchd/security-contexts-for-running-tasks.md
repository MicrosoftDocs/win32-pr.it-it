---
title: Contesti di sicurezza per le attività
description: Le attività vengono registrate ed eseguite in un contesto di sicurezza specifico.
ms.assetid: be86eb9f-f6ec-4dce-afe8-e3314a74062a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 329f354518daeb11a5f330ae3fdc2c332b66d5c3
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104398652"
---
# <a name="security-contexts-for-tasks"></a>Contesti di sicurezza per le attività

Le attività vengono registrate ed eseguite in un contesto di sicurezza specifico. Gli utenti possono creare applicazioni che registrano, aggiornano, eliminano o eseguono correttamente le attività, ma l'utente deve fornire le credenziali corrette quando un'attività viene registrata e l'applicazione deve essere in esecuzione in un processo con i privilegi corretti.

## <a name="specifying-credentials"></a>Specifica di credenziali

È possibile specificare il contesto di sicurezza per un'attività specificando le credenziali nei metodi [**ITaskFolder:: l'RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) o [**ITaskFolder:: RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) ([**TaskFolder. l'RegisterTask**](taskfolder-registertask.md) o [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) per gli script) oppure assegnando un'entità alla [**Proprietà Principal di ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal) ([**TaskDefinition. Principal**](taskdefinition-principal.md) per lo scripting). Se viene creata un'entità per una definizione di attività e la definizione di attività viene registrata usando il metodo **RegisterTaskDefinition** con credenziali diverse specificate nei parametri del metodo, le credenziali specificate nel metodo **RegisterTaskDefinition** sovrascriveranno le credenziali nell'entità. Se un'entità viene creata per una definizione di attività usando XML e quindi il codice XML per l'attività viene registrato usando il metodo **l'RegisterTask** con credenziali diverse specificate nei parametri del metodo, le credenziali specificate nel metodo **l'RegisterTask** sovrascriveranno le credenziali nell'entità.

È possibile specificare un account utente o un gruppo quando si registra un'attività o si specifica il principio per un'attività. Il contesto di sicurezza dell'account utente o del gruppo viene utilizzato per il contesto di sicurezza dell'attività. In questi metodi e proprietà viene definito anche il tipo di accesso. Il tipo di accesso è definito da una delle costanti nell'enumerazione del [**\_ \_ tipo di accesso dell'attività**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type) .

Le attività registrate con la \_ password di accesso dell'attività \_ o il \_ \_ flag S4U di accesso alle attività verranno avviate solo se per l'utente specificato è abilitato il privilegio accesso come batch. Gli utenti del gruppo Administrators e Backup Operators hanno questo privilegio abilitato per impostazione predefinita.

Quando si chiama il metodo [**ITaskService:: Connect**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-connect) ([**TaskService. Connect**](taskservice-connect.md) per gli script), tutte le chiamate al metodo successive al servizio Utilità di pianificazione utilizzeranno le credenziali passate al metodo **Connect** . Questo aspetto è importante da considerare quando si registrano le attività con un tipo di accesso interattivo. Quando si registra un'attività con il tipo di accesso uguale a \_ \_ token interattivo accesso attività \_ e l'attività non ha le credenziali specificate nella proprietà [**principale**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal) della definizione di attività, specificata nei parametri per [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition)o specificata nel codice XML passato a [**l'RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask), l'attività verrà registrata con le credenziali dell'utente che ha chiamato il metodo **Connect** .

## <a name="user-account-control-uac-security-for-tasks"></a>Sicurezza del controllo dell'account utente (UAC) per le attività

Il [controllo dell'account utente](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) consente agli utenti di esercitare le funzionalità generali, ad esempio l'esecuzione di programmi e il salvataggio e la modifica dei dati senza esporre i privilegi amministrativi. Per impostazione predefinita, un'attività viene eseguita con privilegi di basso livello quando UAC è attivato. Le attività possono specificare che verranno eseguite con privilegi elevati o con privilegi limitati impostando un livello di privilegio dall'enumerazione del [**\_ \_ tipo di attività runlevel**](/windows/win32/api/taskschd/ne-taskschd-task_runlevel_type) per la [**Proprietà runlevel di IPrincipal**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) ([**Principal. runlevel**](principal-runlevel.md) per lo scripting). Il valore della proprietà **runlevel** determina il livello di privilegio in corrispondenza del quale verranno eseguite le azioni di un'attività. Se le azioni di un'attività devono disporre di privilegi elevati per l'esecuzione, è necessario impostare la proprietà **runlevel** su **attività \_ runlevel \_ più alta**. Se un'attività viene registrata usando il gruppo Administrators per il contesto di sicurezza dell'attività, è necessario impostare anche la proprietà **runlevel** su **attività \_ runlevel \_ più alta** se si vuole eseguire l'attività. Se un'attività viene registrata utilizzando l' \\ account Administrator predefinito o gli account del sistema locale o del servizio locale, la proprietà **runlevel** verrà ignorata. Il valore della proprietà verrà ignorato anche se il controllo dell'account utente è disattivato. Il valore della proprietà **runlevel** non influisce sulle autorizzazioni necessarie per eseguire o eliminare un'attività.

> [!Note]  
> Dopo l'aggiornamento di un sistema operativo da Windows XP a Windows Vista, le attività registrate con l' \\ account Administrator predefinito in Windows XP avranno la proprietà [**runlevel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) impostata su **Task \_ runlevel \_ LUA**. Questo potrebbe causare l'esito negativo di alcune attività. È possibile aggiornare manualmente questa proprietà per assicurarsi che tutte le attività vengano eseguite.

 

Da un processo con privilegi limitati non è possibile registrare un'attività con la proprietà [**runlevel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) uguale **a \_ runlevel attività \_ più elevata**, ma è possibile registrare un'attività con la proprietà **runlevel** uguale a **Task \_ runlevel \_ LUA**. Le azioni dell'attività verranno eseguite con privilegi limitati. Non è possibile registrare l'attività come predefinita/amministratore, sistema locale o per un gruppo.

Da un processo con privilegi elevati, è possibile registrare un'attività con la proprietà [**runlevel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) uguale a **attività runlevel \_ \_ più alta** o **attività di \_ runlevel \_**. L'attività verrà eseguita con un livello di privilegio stabilito dalla proprietà **runlevel** , a meno che non si stia usando l'account Administrator, nel qual caso l'attività viene eseguita con privilegi elevati.

Da un processo con privilegi elevati è possibile registrare un'attività Utilità di pianificazione 1,0. Il servizio Utilità di pianificazione imposta il livello di esecuzione dell'attività su runlevel attività \_ \_ più alto e l'attività viene eseguita con privilegi elevati.

Da un processo con privilegi limitati è anche possibile registrare un'attività Utilità di pianificazione 1,0. Il servizio Utilità di pianificazione imposta il livello di esecuzione dell'attività su TASK \_ runlevel \_ LUA e l'attività viene eseguita con privilegi limitati. Se questa attività viene aggiornata da un processo con privilegi elevati, il livello di esecuzione dell'attività rimarrà il valore LUA per l'attività \_ \_ .

## <a name="security-for-registering-tasks"></a>Sicurezza per la registrazione delle attività

Quando si registra un'attività da un account membro del gruppo Administrators, è sufficiente specificare una password durante la registrazione dell'attività nelle situazioni seguenti:

-   Se si registra l'attività per l'esecuzione nel contesto di sicurezza dell'account o in un account utente diverso e si usa il flag di accesso alle attività \_ \_ nel metodo [**l'RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) o [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) .
-   Se si registra l'attività per l'esecuzione nel contesto di sicurezza di un account utente diverso e si usa il \_ \_ flag S4U di accesso alle attività nel metodo [**l'RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) o [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) .

Non è possibile utilizzare un gruppo di utenti come contesto di sicurezza di un'attività quando si registra l'attività utilizzando \_ il \_ flag S4U di accesso attività o il \_ flag di accesso all'attività \_ nel metodo [**l'RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) o [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) .

Quando si registra un'attività da un account utente che non è un membro del gruppo Administrators, non è necessario specificare una password per la registrazione dell'attività se si registra l'attività per l'esecuzione nel contesto di sicurezza dell'account e si usa il tipo di accesso S4U o interattivo. In caso contrario, è necessario specificare una password per la registrazione dell'attività. Inoltre, non è possibile registrare l'attività utilizzando l'account del servizio locale o utilizzando un gruppo per il contesto di sicurezza dell'attività.

## <a name="security-for-reading-updating-deleting-and-running-tasks"></a>Sicurezza per la lettura, l'aggiornamento, l'eliminazione e l'esecuzione di attività

Per impostazione predefinita, un utente che crea un'attività può leggere, aggiornare, eliminare ed eseguire l'attività. Un utente deve disporre dell'autorizzazione di scrittura file per un file di attività per aggiornare un'attività, l'autorizzazione di lettura file per un file di attività per leggere un'attività, l'autorizzazione di eliminazione per un file di attività per eliminare un'attività e l'autorizzazione di esecuzione file per un'attività per eseguire un'attività usando i metodi [**IRegisteredTask:: Run**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-run) o [**RunEx**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-runex) ([**RegisteredTask. Run**](registeredtask-run.md) e [**RunEx**](registeredtask-runex.md) per gli script) I membri del gruppo Administrators o dell'account di sistema possono leggere, aggiornare, eliminare ed eseguire tutte le attività. I membri del gruppo Users, l'account LocalService e l'account NetworkService possono solo leggere, aggiornare, eliminare ed eseguire le attività create. Questo comportamento predefinito viene modificato quando viene modificato l'elenco DACL del file delle attività, nel qual caso il DACL definisce quali utenti dispongono dell'autorizzazione di scrittura, lettura, esecuzione ed eliminazione del file. Per impostare le autorizzazioni per un file di attività, usare il metodo IRegisteredTask. SetSecurityDescriptor (RegisteredTask. SetSecurityDescriptor per lo scripting) o impostare il descrittore di sicurezza quando si registra l'attività usando i metodi [**l'RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) o [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) .

Un utente deve disporre dell'autorizzazione WriteDAC oltre alle autorizzazioni di lettura/scrittura per aggiornare un'attività se l'aggiornamento dell'attività richiede una modifica all'elenco DACL per l'attività.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di registrazione delle attività](task-registration-information.md)
</dt> <dt>

[Informazioni sul Utilità di pianificazione](about-the-task-scheduler.md)
</dt> <dt>

[Protezione avanzata delle attività](task-security-hardening.md)
</dt> <dt>

[**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md)
</dt> <dt>

[**ITaskFolder:: RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition)
</dt> <dt>

[**Proprietà Principal di ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal)
</dt> <dt>

[**\_tipo di accesso attività \_**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type)
</dt> </dl>

 

 




