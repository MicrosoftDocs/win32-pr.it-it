---
description: Per impostazione predefinita, il programma di installazione esegue azioni personalizzate con privilegi utente per limitare l'accesso alle azioni personalizzate al sistema.
ms.assetid: 62a3d103-a786-4727-b757-3a8229c8a53f
title: Sicurezza azione personalizzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e7d36e0e5c6cecc61730144fb7efdeed63ba0fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349761"
---
# <a name="custom-action-security"></a>Sicurezza azione personalizzata

Per impostazione predefinita, il programma di installazione esegue azioni personalizzate con privilegi utente per limitare l'accesso alle azioni personalizzate al sistema. Il programma di installazione può eseguire azioni personalizzate con privilegi elevati se è in corso l'installazione di un'applicazione gestita o se i criteri di sistema sono stati specificati per privilegi elevati.

È necessario utilizzare la proprietà [**MsiHiddenProperties**](msihiddenproperties.md) e **msidbCustomActionTypeHideTarget** per impedire la registrazione di informazioni riservate utilizzate dall'azione personalizzata. Per altre informazioni su **msidbCustomActionTypeHideTarget** , vedere [opzione di destinazione nascosta dell'azione personalizzata](custom-action-hidden-target-option.md).

Cancellare la proprietà CustomActionData dopo averla impostata per assicurarsi che i dati sensibili non siano più disponibili. Il codice di esempio seguente è un frammento usato da un'azione personalizzata DLL immediata che imposta i dati per l'uso da un'azione personalizzata posticipata denominata "MyDeferredCA":


```C++
#include <windows.h>
#include <Msiquery.h>
#pragma comment(lib, "msi.lib")

UINT __stdcall MyImmediateCA(MSIHANDLE hInstall)
{
    // set up information for deferred custom action called MyDeferredCA
    const TCHAR szValue[] = TEXT("data");
    UINT uiStat = ERROR_INSTALL_FAILURE;
    if (ERROR_SUCCESS == MsiSetProperty(hInstall, TEXT("MyDeferredCA"), szValue))
    {
        uiStat = MsiDoAction(hInstall, TEXT("MyDeferredCA"));

        // clear CustomActionData property
        if (ERROR_SUCCESS != MsiSetProperty(hInstall, TEXT("MyDeferredCA"), TEXT("")))
            return ERROR_INSTALL_FAILURE;
    }

    return (uiStat == ERROR_SUCCESS) ? uiStat : ERROR_INSTALL_FAILURE;    
}
```



Si noti che solo le [azioni personalizzate di esecuzione posticipata](deferred-execution-custom-actions.md) possono usare l'attributo **msidbCustomActionTypeNoImpersonate** . Per altre informazioni, vedere [azione personalizzata In-Script opzioni di esecuzione](custom-action-in-script-execution-options.md).

Se il bit **msidbCustomActionTypeNoImpersonate** non è impostato per un'azione personalizzata, il programma di installazione esegue l'azione personalizzata con privilegi a livello di utente. Per altre informazioni, vedere [azione personalizzata In-Script opzioni di esecuzione](custom-action-in-script-execution-options.md).

Se il bit **msidbCustomActionTypeNoImpersonate** è impostato ed è in corso l'installazione di un'applicazione gestita con autorizzazioni di amministratore, il programma di installazione può eseguire l'azione personalizzata con privilegi elevati. Tuttavia, se un utente tenta di installare l'applicazione gestita senza autorizzazione di amministratore, il programma di installazione esegue l'applicazione con privilegi a livello di utente indipendentemente dal fatto che sia impostato **msidbCustomActionTypeNoImpersonate** .

Si noti che un'azione personalizzata può essere eseguita con privilegi di sistema anche quando il bit **msidbCustomActionTypeNoImpersonate** non è impostato. Questo errore si verifica se un amministratore installa l'applicazione per tutti gli utenti in un server che esegue il servizio ruolo Terminal Server usando Windows 2000 e l'azione non è contrassegnata con **msidbCustomActionTypeTSAware**. Un'azione personalizzata può inoltre essere eseguita con i privilegi di sistema se l'installazione viene richiamata quando non è presente alcun contesto utente. Se, ad esempio, non è presente alcun utente attualmente connesso durante un'installazione richiamata dalla distribuzione di applicazioni Windows 2000.

Quando si creano azioni personalizzate, è sempre necessario creare l'azione personalizzata usando metodi protetti. Per ulteriori informazioni, vedere [linee guida per la protezione di azioni personalizzate](guidelines-for-securing-custom-actions.md).

 

 



