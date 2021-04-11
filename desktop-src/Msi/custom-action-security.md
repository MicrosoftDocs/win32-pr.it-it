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
# <a name="custom-action-security"></a><span data-ttu-id="0c908-103">Sicurezza azione personalizzata</span><span class="sxs-lookup"><span data-stu-id="0c908-103">Custom Action Security</span></span>

<span data-ttu-id="0c908-104">Per impostazione predefinita, il programma di installazione esegue azioni personalizzate con privilegi utente per limitare l'accesso alle azioni personalizzate al sistema.</span><span class="sxs-lookup"><span data-stu-id="0c908-104">The installer runs custom actions with user privileges by default in order to limit the access of custom actions to the system.</span></span> <span data-ttu-id="0c908-105">Il programma di installazione può eseguire azioni personalizzate con privilegi elevati se è in corso l'installazione di un'applicazione gestita o se i criteri di sistema sono stati specificati per privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="0c908-105">The installer may run custom actions with elevated privileges if a managed application is being installed or if the system policy has been specified for elevated privileges.</span></span>

<span data-ttu-id="0c908-106">È necessario utilizzare la proprietà [**MsiHiddenProperties**](msihiddenproperties.md) e **msidbCustomActionTypeHideTarget** per impedire la registrazione di informazioni riservate utilizzate dall'azione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="0c908-106">You should use the [**MsiHiddenProperties**](msihiddenproperties.md) property and **msidbCustomActionTypeHideTarget** to prevent logging of sensitive information used by the custom action.</span></span> <span data-ttu-id="0c908-107">Per altre informazioni su **msidbCustomActionTypeHideTarget** , vedere [opzione di destinazione nascosta dell'azione personalizzata](custom-action-hidden-target-option.md).</span><span class="sxs-lookup"><span data-stu-id="0c908-107">For more information about **msidbCustomActionTypeHideTarget** see [Custom Action Hidden Target Option](custom-action-hidden-target-option.md).</span></span>

<span data-ttu-id="0c908-108">Cancellare la proprietà CustomActionData dopo averla impostata per assicurarsi che i dati sensibili non siano più disponibili.</span><span class="sxs-lookup"><span data-stu-id="0c908-108">Clear the CustomActionData property after setting it to ensure that sensitive data is no longer available.</span></span> <span data-ttu-id="0c908-109">Il codice di esempio seguente è un frammento usato da un'azione personalizzata DLL immediata che imposta i dati per l'uso da un'azione personalizzata posticipata denominata "MyDeferredCA":</span><span class="sxs-lookup"><span data-stu-id="0c908-109">Example code below is a snippet used by an immediate DLL custom action that is setting up data for use by a deferred custom action called "MyDeferredCA":</span></span>


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



<span data-ttu-id="0c908-110">Si noti che solo le [azioni personalizzate di esecuzione posticipata](deferred-execution-custom-actions.md) possono usare l'attributo **msidbCustomActionTypeNoImpersonate** .</span><span class="sxs-lookup"><span data-stu-id="0c908-110">Note that only [deferred execution custom actions](deferred-execution-custom-actions.md) can use the **msidbCustomActionTypeNoImpersonate** attribute.</span></span> <span data-ttu-id="0c908-111">Per altre informazioni, vedere [azione personalizzata In-Script opzioni di esecuzione](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="0c908-111">For more information see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

<span data-ttu-id="0c908-112">Se il bit **msidbCustomActionTypeNoImpersonate** non è impostato per un'azione personalizzata, il programma di installazione esegue l'azione personalizzata con privilegi a livello di utente.</span><span class="sxs-lookup"><span data-stu-id="0c908-112">If the **msidbCustomActionTypeNoImpersonate** bit is not set for a custom action, the installer runs the custom action with user-level privileges.</span></span> <span data-ttu-id="0c908-113">Per altre informazioni, vedere [azione personalizzata In-Script opzioni di esecuzione](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="0c908-113">For more information, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

<span data-ttu-id="0c908-114">Se il bit **msidbCustomActionTypeNoImpersonate** è impostato ed è in corso l'installazione di un'applicazione gestita con autorizzazioni di amministratore, il programma di installazione può eseguire l'azione personalizzata con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="0c908-114">If the **msidbCustomActionTypeNoImpersonate** bit is set and a managed application is being installed with administrator permission, the installer may run the custom action with elevated privileges.</span></span> <span data-ttu-id="0c908-115">Tuttavia, se un utente tenta di installare l'applicazione gestita senza autorizzazione di amministratore, il programma di installazione esegue l'applicazione con privilegi a livello di utente indipendentemente dal fatto che sia impostato **msidbCustomActionTypeNoImpersonate** .</span><span class="sxs-lookup"><span data-stu-id="0c908-115">However, if a user attempts to install the managed application without administrator permission, the installer runs the application with user level privileges regardless of whether **msidbCustomActionTypeNoImpersonate** is set.</span></span>

<span data-ttu-id="0c908-116">Si noti che un'azione personalizzata può essere eseguita con privilegi di sistema anche quando il bit **msidbCustomActionTypeNoImpersonate** non è impostato.</span><span class="sxs-lookup"><span data-stu-id="0c908-116">Note that a custom action may run with system privileges even when the **msidbCustomActionTypeNoImpersonate** bit is not set.</span></span> <span data-ttu-id="0c908-117">Questo errore si verifica se un amministratore installa l'applicazione per tutti gli utenti in un server che esegue il servizio ruolo Terminal Server usando Windows 2000 e l'azione non è contrassegnata con **msidbCustomActionTypeTSAware**.</span><span class="sxs-lookup"><span data-stu-id="0c908-117">This occurs if an administrator installs the application for all users on a server running the Terminal Server role service using Windows 2000 and the action is not marked with **msidbCustomActionTypeTSAware**.</span></span> <span data-ttu-id="0c908-118">Un'azione personalizzata può inoltre essere eseguita con i privilegi di sistema se l'installazione viene richiamata quando non è presente alcun contesto utente.</span><span class="sxs-lookup"><span data-stu-id="0c908-118">A custom action may also run with system privileges if the installation is invoked when there is no user context.</span></span> <span data-ttu-id="0c908-119">Se, ad esempio, non è presente alcun utente attualmente connesso durante un'installazione richiamata dalla distribuzione di applicazioni Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="0c908-119">For example, if there is no currently logged-on user during an installation invoked by Windows 2000 Application Deployment.</span></span>

<span data-ttu-id="0c908-120">Quando si creano azioni personalizzate, è sempre necessario creare l'azione personalizzata usando metodi protetti.</span><span class="sxs-lookup"><span data-stu-id="0c908-120">When creating your own custom actions, you should always author the custom action using secure methods.</span></span> <span data-ttu-id="0c908-121">Per ulteriori informazioni, vedere [linee guida per la protezione di azioni personalizzate](guidelines-for-securing-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="0c908-121">For more information, see [Guidelines for Securing Custom Actions](guidelines-for-securing-custom-actions.md).</span></span>

 

 



