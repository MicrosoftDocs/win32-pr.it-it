---
description: Il programma di installazione esegue azioni personalizzate con privilegi utente per impostazione predefinita per limitare l'accesso delle azioni personalizzate al sistema.
ms.assetid: 62a3d103-a786-4727-b757-3a8229c8a53f
title: Sicurezza delle azioni personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0a8011640bea177ec253f555b6ff83302541b640a050ccf861eb345c58ca13f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118143311"
---
# <a name="custom-action-security"></a>Sicurezza delle azioni personalizzate

Il programma di installazione esegue azioni personalizzate con privilegi utente per impostazione predefinita per limitare l'accesso delle azioni personalizzate al sistema. Il programma di installazione può eseguire azioni personalizzate con privilegi elevati se è in corso l'installazione di un'applicazione gestita o se i criteri di sistema sono stati specificati per privilegi elevati.

È consigliabile usare la [**proprietà MsiHiddenProperties**](msihiddenproperties.md) e **msidbCustomActionTypeHideTarget** per impedire la registrazione delle informazioni riservate usate dall'azione personalizzata. Per altre informazioni su **msidbCustomActionTypeHideTarget,** vedere [Custom Action Hidden Target Option](custom-action-hidden-target-option.md).

Deselezionare la proprietà CustomActionData dopo l'impostazione per assicurarsi che i dati sensibili non siano più disponibili. Il codice di esempio seguente è un frammento di codice usato da un'azione personalizzata DLL immediata che configura i dati per l'uso da parte di un'azione personalizzata posticipata denominata "MyDeferredCA":


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



Si noti che solo [le azioni personalizzate di esecuzione posticipata](deferred-execution-custom-actions.md) possono usare **l'attributo msidbCustomActionTypeNoImpersonate.** Per altre informazioni, vedere [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).

Se il bit **msidbCustomActionTypeNoImpersonate** non è impostato per un'azione personalizzata, il programma di installazione esegue l'azione personalizzata con privilegi a livello di utente. Per altre informazioni, vedere [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).

Se il bit **msidbCustomActionTypeNoImpersonate** è impostato e un'applicazione gestita viene installata con autorizzazione di amministratore, il programma di installazione può eseguire l'azione personalizzata con privilegi elevati. Tuttavia, se un utente tenta di installare l'applicazione gestita senza autorizzazione di amministratore, il programma di installazione esegue l'applicazione con privilegi a livello di utente indipendentemente dall'impostazione di **msidbCustomActionTypeNoImpersonate.**

Si noti che un'azione personalizzata può essere eseguita con privilegi di sistema anche quando il bit **msidbCustomActionTypeNoImpersonate** non è impostato. Ciò si verifica se un amministratore installa l'applicazione per tutti gli utenti in un server che esegue il servizio ruolo Terminal Server usando Windows 2000 e l'azione non è contrassegnata con **msidbCustomActionTypeTSAware.** Un'azione personalizzata può essere eseguita anche con privilegi di sistema se l'installazione viene richiamata quando non è presente alcun contesto utente. Ad esempio, se non è presente alcun utente attualmente connesso durante un'installazione richiamata da Windows 2000 Application Deployment.

Quando si creano azioni personalizzate, è sempre consigliabile creare l'azione personalizzata usando metodi sicuri. Per altre informazioni, vedere [Linee guida per la protezione delle azioni personalizzate.](guidelines-for-securing-custom-actions.md)

 

 



