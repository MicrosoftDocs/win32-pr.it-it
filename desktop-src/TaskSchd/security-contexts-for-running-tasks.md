---
title: Contesti di sicurezza per le attività
description: Le attività vengono registrate ed eseguite in un contesto di sicurezza specifico.
ms.assetid: be86eb9f-f6ec-4dce-afe8-e3314a74062a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb6f49ef07818b1fe729fa96a2b5e0712979a17f300e4f411f96cefd2f3917f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119738251"
---
# <a name="security-contexts-for-tasks"></a>Contesti di sicurezza per le attività

Le attività vengono registrate ed eseguite in un contesto di sicurezza specifico. Gli utenti possono creare applicazioni che registrano, aggiornano, eliminano o eseguono correttamente attività, ma l'utente deve fornire le credenziali corrette quando un'attività viene registrata e l'applicazione deve essere in esecuzione in un processo con i privilegi corretti.

## <a name="specifying-credentials"></a>Specifica delle credenziali

È possibile specificare il contesto di sicurezza per un'attività specificando le credenziali nei metodi [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) o [**ITaskFolder::RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) o [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) per lo scripting) o assegnando un'entità alla proprietà Principal di [**ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal) ([**TaskDefinition.Principal**](taskdefinition-principal.md) per lo scripting). Se viene creata un'entità per una definizione di attività e quindi la definizione dell'attività viene registrata usando il metodo **RegisterTaskDefinition** con credenziali diverse specificate nei parametri del metodo , le credenziali specificate nel metodo **RegisterTaskDefinition** sovrascriveranno le credenziali nell'entità. Se viene creata un'entità per una definizione di attività tramite XML e quindi il codice XML per l'attività viene registrato usando il **metodo RegisterTask** con credenziali diverse specificate nei parametri del metodo , le credenziali specificate nel **metodo RegisterTask** sovrascriveranno le credenziali nell'entità.

È possibile specificare un account utente o un gruppo quando si registra un'attività o si specifica il principio per un'attività. Il contesto di sicurezza dell'account utente o del gruppo viene usato per il contesto di sicurezza dell'attività. In questi metodi e proprietà si definisce anche il tipo di accesso. Il tipo di accesso è definito da una delle costanti [**nell'enumerazione TASK \_ LOGON \_ TYPE.**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type)

Le attività registrate con il flag TASK LOGON PASSWORD o TASK LOGON S4U verranno avviate solo se l'utente specificato ha il \_ \_ \_ \_ privilegio Logon as Batch abilitato. Gli utenti del gruppo Administrators e Backup Operators hanno questo privilegio abilitato per impostazione predefinita.

Quando si chiama il metodo [**ITaskService::Connessione**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-connect) [**(TaskService.Connessione**](taskservice-connect.md) per lo scripting), qualsiasi chiamata al metodo successiva al servizio Utilità di pianificazione userà le credenziali passate al **metodo Connessione.** Questo è importante da considerare quando si registrano attività con un tipo di accesso interattivo. Quando si registra un'attività con il tipo di accesso uguale a TASK LOGON INTERACTIVE TOKEN e l'attività non dispone di credenziali specificate nella proprietà Principal della definizione dell'attività, specificata nei parametri per \_ \_ \_ [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition)o [](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal)  specificata nel codice XML passato a [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask), l'attività verrà registrata con le credenziali dell'utente che ha chiamato il metodo Connessione.

## <a name="user-account-control-uac-security-for-tasks"></a>Sicurezza del controllo dell'account utente per le attività

[Controllo dell'account utente](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) consente agli utenti di eseguire funzionalità generali, ad esempio l'esecuzione di programmi e il salvataggio e la modifica dei dati senza esporre privilegi amministrativi. Per impostazione predefinita, un'attività viene eseguita con privilegi di basso livello quando il controllo dell'account utente è attivato. Le attività possono specificare che verranno eseguite con privilegi elevati o privilegi bassi impostando un livello di privilegio dall'enumerazione [**TASK \_ RUNLEVEL \_ TYPE**](/windows/win32/api/taskschd/ne-taskschd-task_runlevel_type) per la [**proprietà RunLevel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) di IPrincipal ([**Principal.RunLevel**](principal-runlevel.md) per lo scripting). Il valore della **proprietà RunLevel** determina il livello di privilegio al quale verranno eseguite le azioni di un'attività. Se le azioni di un'attività devono avere privilegi elevati per l'esecuzione, è necessario impostare la **proprietà RunLevel** su **TASK \_ RUNLEVEL \_ HIGHEST**. Se un'attività viene registrata usando il gruppo Administrators per il contesto di sicurezza dell'attività, è necessario impostare anche la **proprietà RunLevel** su **TASK \_ RUNLEVEL \_ HIGHEST** se si vuole eseguire l'attività. Se un'attività viene registrata usando l'account amministratore predefinito o gli account del sistema locale o del servizio locale, la \\ **proprietà RunLevel** verrà ignorata. Il valore della proprietà verrà ignorato anche se il controllo dell'account utente è disattivato. Il valore della **proprietà RunLevel** non influisce sulle autorizzazioni necessarie per eseguire o eliminare un'attività.

> [!Note]  
> Dopo l'aggiornamento di un sistema operativo da Windows XP a Windows Vista, le attività registrate usando l'account amministratore predefinito in Windows XP avranno la proprietà RunLevel impostata su \\ **TASK \_ RUNLEVEL \_ LUA.** [](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) Ciò potrebbe causare l'esito negativo di alcune attività. È possibile aggiornare questa proprietà manualmente per assicurarsi che tutte le attività verranno eseguite.

 

Da un processo con privilegi minimi non è possibile registrare un'attività con la proprietà [**RunLevel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) uguale a **TASK \_ RUNLEVEL \_ HIGHEST,** ma è possibile registrare un'attività con la **proprietà RunLevel** uguale a **TASK \_ RUNLEVEL \_ LUA.** Le azioni dell'attività verranno eseguite con privilegi minimi. Non è consentito registrare l'attività come Builtin/Administrator, Local System o per un gruppo.

Da un processo con privilegi elevati, è possibile registrare un'attività con la [**proprietà RunLevel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) uguale a **TASK \_ RUNLEVEL \_ HIGHEST** o **TASK \_ RUNLEVEL \_ LUA**. L'attività verrà eseguita con un livello di privilegio stabilito dalla proprietà **RunLevel,** a meno che non si utilizzi l'account Amministratore, nel qual caso l'attività viene eseguita con privilegi elevati.

Da un processo con privilegi elevati è possibile registrare un'Utilità di pianificazione 1.0. Il Utilità di pianificazione imposta il livello di esecuzione dell'attività su TASK RUNLEVEL HIGHEST e l'attività verrà eseguita \_ \_ con privilegi elevati.

Da un processo con privilegi bassi è anche possibile registrare un'Utilità di pianificazione 1.0. Il Utilità di pianificazione imposta il livello di esecuzione dell'attività su TASK RUNLEVEL LUA e l'attività verrà eseguita \_ \_ con privilegi minimi. Se questa attività viene aggiornata da un processo con privilegi elevati, il livello di esecuzione dell'attività rimarrà TASK \_ RUNLEVEL \_ LUA.

## <a name="security-for-registering-tasks"></a>Sicurezza per la registrazione di attività

Quando si registra un'attività da un account membro del gruppo Administrators, è necessario specificare solo una password durante la registrazione dell'attività nelle situazioni seguenti:

-   Se si registra l'attività per l'esecuzione nel contesto di sicurezza dell'account o di un account utente diverso e si usa il flag TASK LOGON PASSWORD nel \_ metodo \_ [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) o [**RegisterTaskDefinition.**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition)
-   Se si registra l'attività per l'esecuzione nel contesto di sicurezza di un account utente diverso e si usa il flag TASK LOGON S4U nel metodo RegisterTask o \_ \_ [**RegisterTaskDefinition.**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) [](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask)

Non è possibile usare un gruppo di utenti come contesto di sicurezza di un'attività quando si registra l'attività usando il flag TASK LOGON S4U o il flag TASK LOGON PASSWORD nel metodo RegisterTask o \_ \_ \_ \_ [**RegisterTaskDefinition.**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) [](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask)

Quando si registra un'attività da un account utente che non è membro del gruppo Administrators, non è necessario specificare una password durante la registrazione dell'attività se si registra l'attività per l'esecuzione nel contesto di sicurezza dell'account e si usa il tipo di accesso interattivo o S4U. In caso contrario, è necessario specificare una password durante la registrazione dell'attività. Inoltre, non è possibile registrare l'attività usando l'account del servizio locale o un gruppo per il contesto di sicurezza dell'attività.

## <a name="security-for-reading-updating-deleting-and-running-tasks"></a>Sicurezza per la lettura, l'aggiornamento, l'eliminazione e l'esecuzione di attività

Per impostazione predefinita, un utente che crea un'attività può leggere, aggiornare, eliminare ed eseguire l'attività. Un utente deve avere l'autorizzazione di scrittura file per un file di attività per aggiornare un'attività, l'autorizzazione di lettura file per un file di attività per leggere un'attività, eliminare l'autorizzazione per un file di attività per eliminare un'attività e l'autorizzazione di esecuzione file per un'attività per eseguire un'attività usando i metodi [**IRegisteredTask::Run**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-run) o [**RunEx**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-runex) ([**RegisteredTask.Run**](registeredtask-run.md) e [**RunEx**](registeredtask-runex.md) per lo scripting). I membri del gruppo Administrators o dell'account SYSTEM possono leggere, aggiornare, eliminare ed eseguire qualsiasi attività. I membri del gruppo Users, dell'account LocalService e dell'account NetworkService possono solo leggere, aggiornare, eliminare ed eseguire le attività create. Questo comportamento predefinito viene modificato quando viene modificato l'elenco DACL del file di attività, nel qual caso l'elenco DACL definisce quali utenti dispongono delle autorizzazioni di scrittura, lettura, esecuzione ed eliminazione di file. Per impostare le autorizzazioni per un file di attività, usare il metodo IRegisteredTask.SetSecurityDescriptor (RegisteredTask.SetSecurityDescriptor per lo scripting) o impostare il descrittore di sicurezza quando si registra l'attività usando i metodi [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) o [**RegisterTaskDefinition.**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition)

Un utente deve disporre dell'autorizzazione WriteDAC oltre alle autorizzazioni di lettura/scrittura per aggiornare un'attività se l'aggiornamento dell'attività richiede una modifica all'elenco DACL per l'attività.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di registrazione attività](task-registration-information.md)
</dt> <dt>

[Informazioni sul Utilità di pianificazione](about-the-task-scheduler.md)
</dt> <dt>

[Protezione avanzata della sicurezza delle attività](task-security-hardening.md)
</dt> <dt>

[**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md)
</dt> <dt>

[**ITaskFolder::RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition)
</dt> <dt>

[**Proprietà Principal di ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal)
</dt> <dt>

[**TIPO \_ DI ACCESSO \_ ALL'ATTIVITÀ**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type)
</dt> </dl>

 

 




