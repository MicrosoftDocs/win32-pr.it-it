---
title: Attivazione da sessione a sessione con un moniker di sessione
description: L'attivazione da sessione a sessione (detta anche attivazione tra sessioni) consente a un processo client di avviare (attivare) un processo del server locale in una sessione specificata.
ms.assetid: d405c276-040b-4cde-aeb2-482a25e2867f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2714f3dbe7b23c8b7f04d4271018891960b87f76
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729618"
---
# <a name="session-to-session-activation-with-a-session-moniker"></a><span data-ttu-id="46108-103">Attivazione da sessione a sessione con un moniker di sessione</span><span class="sxs-lookup"><span data-stu-id="46108-103">Session-to-Session Activation with a Session Moniker</span></span>

<span data-ttu-id="46108-104">L'attivazione da sessione a sessione (detta anche attivazione tra sessioni) consente a un processo client di avviare (attivare) un processo del server locale in una sessione specificata.</span><span class="sxs-lookup"><span data-stu-id="46108-104">Session-to-session activation (also called cross-session activation) allows a client process to start (activate) a local server process on a specified session.</span></span> <span data-ttu-id="46108-105">Questa funzionalità è disponibile per le applicazioni configurate per l'esecuzione nel contesto di sicurezza dell'utente interattivo, nota anche come modalità di attivazione degli oggetti "RunAs Interactive".</span><span class="sxs-lookup"><span data-stu-id="46108-105">This feature is available for applications that are configured to run in the security context of the interactive user, also known as the "RunAs Interactive User" object activation mode.</span></span> <span data-ttu-id="46108-106">Per ulteriori informazioni sui contesti di sicurezza, vedere [il contesto di sicurezza del client](/windows/desktop/SecAuthZ/the-client-security-context).</span><span class="sxs-lookup"><span data-stu-id="46108-106">For more information about security contexts, see [The Client's Security Context](/windows/desktop/SecAuthZ/the-client-security-context).</span></span>

<span data-ttu-id="46108-107">Distributed COM (DCOM) consente l'attivazione di oggetti in base a ogni sessione usando un moniker di [sessione](session-monikers.md)fornito dal sistema.</span><span class="sxs-lookup"><span data-stu-id="46108-107">Distributed COM (DCOM) enables object activation on a per-session basis by using a system-supplied [Session Moniker](session-monikers.md).</span></span> <span data-ttu-id="46108-108">Altri moniker forniti dal sistema includono [moniker di file](../com/file-monikers.md), moniker di [elementi](../com/item-monikers.md), [moniker compositi](../com/composite-monikers.md)generici, [anti-moniker](../com/anti-monikers.md), [moniker di puntatore](../com/pointer-monikers.md)e [moniker URL](../com/url-monikers.md).</span><span class="sxs-lookup"><span data-stu-id="46108-108">Other system-supplied monikers include [file monikers](../com/file-monikers.md), [item monikers](../com/item-monikers.md), generic [composite monikers](../com/composite-monikers.md), [anti-monikers](../com/anti-monikers.md), [pointer monikers](../com/pointer-monikers.md), and [URL monikers](../com/url-monikers.md).</span></span>

<span data-ttu-id="46108-109">Per poter utilizzare il moniker della sessione, è necessario che l'applicazione DCOM sia impostata per l'esecuzione come utente interattivo.</span><span class="sxs-lookup"><span data-stu-id="46108-109">To be able to use the session moniker, the DCOM application must be set to run as the interactive user.</span></span> <span data-ttu-id="46108-110">Questa impostazione può essere configurata utilizzando lo strumento di amministrazione Servizi componenti, visualizzando le proprietà dell'applicazione DCOM e selezionando **l'utente interattivo** nella scheda **identità** . Per ulteriori informazioni sui possibili rischi per la sicurezza associati all'impostazione di un'applicazione DCOM per l'esecuzione come utente interattivo in un ambiente di Servizi Desktop remoto, vedere la sezione relativa all'identità dell'applicazione (COM) nella documentazione COM della piattaforma Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="46108-110">This can be set by using the Component Services Administrative tool, viewing the Properties of the DCOM application, and selecting **The interactive user** on the **Identity** tab. For more information about the possible security risks associated with setting a DCOM application to run as the interactive user in a Remote Desktop Services environment, see the "Application Identity (COM)" section of the COM documentation in the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="46108-111">Se si seleziona un altro tipo di utente per eseguire l'applicazione, il moniker della sessione verrà ignorato dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="46108-111">If any other type of user is selected to run the application, the session moniker will be ignored by the application.</span></span> <span data-ttu-id="46108-112">Il moniker della sessione viene ignorato anche dalle applicazioni server COM+.</span><span class="sxs-lookup"><span data-stu-id="46108-112">The session moniker is also ignored by COM+ server applications.</span></span> <span data-ttu-id="46108-113">Per ulteriori informazioni sugli altri metodi per la selezione del tipo di utente per l'esecuzione dell'applicazione, vedere la documentazione COM in Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="46108-113">For more information about other methods for selecting the type of user to run the application, see the COM documentation in the Platform SDK.</span></span>

<span data-ttu-id="46108-114">Per creare un moniker di sessione, è necessario comporre l'ID di sessione della sessione di Servizi Desktop remoto con un moniker della classe che specifica l'ID di classe del server di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="46108-114">To create a session moniker, you must compose the session ID of the Remote Desktop Services session with a class moniker that specifies the process server's class ID.</span></span>

<span data-ttu-id="46108-115">**Per creare un moniker di sessione**</span><span class="sxs-lookup"><span data-stu-id="46108-115">**To create a session moniker**</span></span>

1.  <span data-ttu-id="46108-116">Impostare come prefisso il nome visualizzato del moniker della classe con il nome visualizzato del moniker della sessione utilizzando la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="46108-116">Prefix the display name of the class moniker with the display name of the session moniker by using the following syntax:</span></span>

    ``` syntax
    "Session:[digits]!clsid:[class id]"
    ```

    <span data-ttu-id="46108-117">dove *cifre* rappresenta l'ID di sessione della sessione in cui verrà avviato il processo server e dove *ID classe* rappresenta l'ID di classe del server.</span><span class="sxs-lookup"><span data-stu-id="46108-117">where *digits* represents the session ID of the session on which the server process will be started, and where *class id* represents the class ID of the server.</span></span> <span data-ttu-id="46108-118">Si noti che l'ID sessione è un numero in base 10.</span><span class="sxs-lookup"><span data-stu-id="46108-118">Note that the session ID is a base-10 number.</span></span>

    <span data-ttu-id="46108-119">Per i computer che eseguono Windows XP o versioni successive, l'utilizzo della sintassi seguente comporterà l'invio dell'attivazione da parte di COM alla sessione della console fisica attualmente attiva, indipendentemente dal relativo ID di sessione:</span><span class="sxs-lookup"><span data-stu-id="46108-119">For computers that are running Windows XP or later, using the following syntax will result in COM sending the activation to the currently active physical console session, whatever its session ID is:</span></span>

    ``` syntax
    "Session:Console!clsid:[class id]"
    ```

2.  <span data-ttu-id="46108-120">Dopo aver creato il moniker della sessione, è possibile passare il risultato alla funzione [**MkParseDisplayName**](/windows/desktop/api/objbase/nf-objbase-mkparsedisplayname) o [MkParseDisplayNameEx](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="46108-120">After you have created the session moniker, you can pass the result to either the [**MkParseDisplayName**](/windows/desktop/api/objbase/nf-objbase-mkparsedisplayname) function or the [MkParseDisplayNameEx](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) function.</span></span>

<span data-ttu-id="46108-121">È possibile usare un moniker di sessione in modo analogo a qualsiasi altro moniker.</span><span class="sxs-lookup"><span data-stu-id="46108-121">You can use a session moniker in the same way as you would use any other moniker.</span></span>

<span data-ttu-id="46108-122">Per un esempio di codice che illustra come attivare un processo del server locale in una sessione specificata, vedere [using a Session moniker](using-a-session-moniker.md).</span><span class="sxs-lookup"><span data-stu-id="46108-122">For a code sample that demonstrates how to activate a local server process on a specified session, see [Using a Session Moniker](using-a-session-moniker.md).</span></span>

<span data-ttu-id="46108-123">Per ulteriori informazioni sull'attivazione di oggetti, sui moniker forniti dal sistema e sui moniker della classe, vedere la documentazione COM in Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="46108-123">For more information about object activation, system-supplied monikers and class monikers, see the COM documentation in the Platform SDK.</span></span>

> [!Note]  
> <span data-ttu-id="46108-124">I processi creati tra sessioni hanno un limite superiore per le dimensioni del blocco dell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="46108-124">Processes that are created across sessions have an upper limit on the size of the environment block.</span></span> <span data-ttu-id="46108-125">Questo limite è di circa 4 KB, ma può essere maggiore o minore a seconda delle altre informazioni necessarie per creare il processo, ad esempio i nomi file, le directory e i parametri per il nuovo processo.</span><span class="sxs-lookup"><span data-stu-id="46108-125">This limit is around 4 KB, but it can be larger or smaller depending on what other information is needed to create the process (for example file names, directories, and parameters for the new process).</span></span>

 

 

 