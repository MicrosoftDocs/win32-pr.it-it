---
title: Monitoraggio di connessioni e disconnessioni di sessione
description: Per registrare un'applicazione con Servizi Desktop remoto, archiviare il nome dell'applicazione Virtual Channel Server nel registro di sistema aggiungendo una sottochiave.
ms.assetid: 8524cb7a-a930-431a-bc5f-b0793781de15
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e819b13594ecec14a2b425560152cadedd4e9122
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046848"
---
# <a name="monitoring-session-connections-and-disconnections"></a><span data-ttu-id="872e1-103">Monitoraggio di connessioni e disconnessioni di sessione</span><span class="sxs-lookup"><span data-stu-id="872e1-103">Monitoring session connections and disconnections</span></span>

<span data-ttu-id="872e1-104">Per un'applicazione di servizio, ad esempio un'applicazione server di canale virtuale, per monitorare le connessioni e le disconnessioni della sessione, è necessario registrarla con Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="872e1-104">For a service application, such as a virtual channel server application, to monitor session connections and disconnections, you must register it with Remote Desktop Services.</span></span> <span data-ttu-id="872e1-105">Per registrare l'applicazione con Servizi Desktop remoto, archiviare il nome dell'applicazione Virtual Channel Server nel registro di sistema aggiungendo una sottochiave nel percorso seguente:</span><span class="sxs-lookup"><span data-stu-id="872e1-105">To register the application with Remote Desktop Services, store the name of the virtual channel server application in the registry by adding a subkey under the following location:</span></span>

<span data-ttu-id="872e1-106">**HKEY \_ \_** \\  \\  \\  \\  \\ **Componenti aggiuntivi** TerminalServer del controllo CurrentControlSet di sistema del computer locale</span><span class="sxs-lookup"><span data-stu-id="872e1-106">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**TerminalServer**\\**Addins**</span></span>

<span data-ttu-id="872e1-107">La sottochiave può avere qualsiasi nome.</span><span class="sxs-lookup"><span data-stu-id="872e1-107">The subkey can have any name.</span></span> <span data-ttu-id="872e1-108">Deve avere un valore **reg \_ SZ** , **Name**, che contiene il nome simbolico dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="872e1-108">It must have a **REG\_SZ** value, **Name**, that contains the symbolic name of the application.</span></span>

``` syntax
Name = AddinName
```

<span data-ttu-id="872e1-109">La lunghezza massima della sottochiave e del valore di **Name** è 99 caratteri.</span><span class="sxs-lookup"><span data-stu-id="872e1-109">The maximum length of both the subkey and the value of **Name** is 99 characters.</span></span>

<span data-ttu-id="872e1-110">La sottochiave deve avere anche un valore **reg \_ DWORD** che indica il tipo di applicazione server.</span><span class="sxs-lookup"><span data-stu-id="872e1-110">The subkey must also have a **REG\_DWORD** value that indicates the type of server application.</span></span>

``` syntax
Type = AddinType
```

<span data-ttu-id="872e1-111">*AddinType* deve essere il valore seguente.</span><span class="sxs-lookup"><span data-stu-id="872e1-111">*AddinType* must be the following value.</span></span>



| <span data-ttu-id="872e1-112">Valore</span><span class="sxs-lookup"><span data-stu-id="872e1-112">Value</span></span> | <span data-ttu-id="872e1-113">Significato</span><span class="sxs-lookup"><span data-stu-id="872e1-113">Meaning</span></span>                               |
|-------|---------------------------------------|
| <span data-ttu-id="872e1-114">3</span><span class="sxs-lookup"><span data-stu-id="872e1-114">3</span></span>     | <span data-ttu-id="872e1-115">Applicazione in modalità utente, spazio sessione.</span><span class="sxs-lookup"><span data-stu-id="872e1-115">User-mode application, session space.</span></span> |



 

<span data-ttu-id="872e1-116">La registrazione dell'applicazione di servizio ha effetto solo nelle sessioni create dopo l'esecuzione della registrazione.</span><span class="sxs-lookup"><span data-stu-id="872e1-116">Registration of the service application takes effect only in sessions created after the registration was performed.</span></span>

<span data-ttu-id="872e1-117">Per ogni applicazione di servizio registrato, Servizi Desktop remoto segnalerà un set di oggetti evento quando un client si connette o si disconnette dalla sessione.</span><span class="sxs-lookup"><span data-stu-id="872e1-117">For each registered service application, Remote Desktop Services will signal a set of event objects when a client connects or disconnects from the session.</span></span> <span data-ttu-id="872e1-118">Ogni plug-in di canale virtuale deve registrarsi e creare gli eventi di notifica chiamando [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa).</span><span class="sxs-lookup"><span data-stu-id="872e1-118">Each virtual channel plug-in must register itself and create the notification events by calling [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa).</span></span> <span data-ttu-id="872e1-119">I nomi di questi oggetti evento rispettano il formato seguente.</span><span class="sxs-lookup"><span data-stu-id="872e1-119">The names of these event objects adhere to the following format.</span></span>

``` syntax
AddinName-Reconnect

AddinName-Disconnect
```

<span data-ttu-id="872e1-120">*AddInName* è la stringa specificata nel valore **nome** della sottochiave del registro di sistema in cui è registrata l'applicazione server.</span><span class="sxs-lookup"><span data-stu-id="872e1-120">*AddinName* is the string specified in the **Name** value of the registry subkey under which the server application is registered.</span></span> <span data-ttu-id="872e1-121">La creazione di questi eventi in una sessione ne comporta la creazione in una speciale directory di eventi per sessione.</span><span class="sxs-lookup"><span data-stu-id="872e1-121">Creating these events under a session causes them to be created in a special per-session event directory.</span></span> <span data-ttu-id="872e1-122">La directory degli eventi offre una maggiore sicurezza impedendo alle applicazioni in altre sessioni di modificare lo stato di questi eventi.</span><span class="sxs-lookup"><span data-stu-id="872e1-122">The event directory provides added security by preventing applications in other sessions from modifying the state of these events.</span></span>

<span data-ttu-id="872e1-123">Per controllare se gli eventi di riconnessione e disconnessione vengono ricevuti sul server, è possibile inserire il flag **RemoteControlPersistent** nel registro di sistema nella chiave seguente:</span><span class="sxs-lookup"><span data-stu-id="872e1-123">To control whether RECONNECT and DISCONNECT events are received on the server, you can place the **RemoteControlPersistent** flag in the registry under the following key:</span></span>

<span data-ttu-id="872e1-124">**HKEY \_ \_Computer locale** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **TerminalServer** \\ **AddIns** \\ *AddInName*</span><span class="sxs-lookup"><span data-stu-id="872e1-124">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**TerminalServer**\\**Addins**\\*addinname*</span></span>

<span data-ttu-id="872e1-125">Il flag Abilita o Disabilita la riconnessione e la disconnessione degli eventi quando una sessione client viene avviata o arrestata.</span><span class="sxs-lookup"><span data-stu-id="872e1-125">The flag enables or disables RECONNECT and DISCONNECT events from being signaled when a client session starts or stops.</span></span> <span data-ttu-id="872e1-126">La sintassi del valore **reg \_ DWORD** è la seguente.</span><span class="sxs-lookup"><span data-stu-id="872e1-126">The syntax of the **REG\_DWORD** value is the following.</span></span>

``` syntax
RemoteControlPersistent = flag
```

<span data-ttu-id="872e1-127">Il valore di *flag* può essere uno o zero.</span><span class="sxs-lookup"><span data-stu-id="872e1-127">The value of *flag* can be one or zero.</span></span> <span data-ttu-id="872e1-128">Il valore predefinito è zero.</span><span class="sxs-lookup"><span data-stu-id="872e1-128">Zero is the default value.</span></span> <span data-ttu-id="872e1-129">Se impostato su uno, l'applicazione del servizio non riceverà una notifica se la sessione client viene avviata o arrestata.</span><span class="sxs-lookup"><span data-stu-id="872e1-129">If set to one, the service application will not be notified if the client session is started or stopped.</span></span> <span data-ttu-id="872e1-130">Se è impostato su zero, un evento di riconnessione viene segnalato all'avvio della sessione client e viene segnalato un evento di disconnessione quando la sessione client viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="872e1-130">If set to zero, a RECONNECT event is signaled when the client session starts, and a DISCONNECT event is signaled when the client session stops.</span></span>

<span data-ttu-id="872e1-131">Il formato del nome dell'oggetto evento precedente è ancora supportato in Windows Server 2008 per compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="872e1-131">The previous event-object name format is still supported in Windows Server 2008 for backward compatibility.</span></span> <span data-ttu-id="872e1-132">Si consiglia di usare il formato più recente di Windows Server 2008 perché è più sicuro.</span><span class="sxs-lookup"><span data-stu-id="872e1-132">It is recommended that you use the newer Windows Server 2008 format because it is more secure.</span></span>

<span data-ttu-id="872e1-133">Il formato di evento precedente è il seguente.</span><span class="sxs-lookup"><span data-stu-id="872e1-133">The previous event format is as follows.</span></span>

``` syntax
Global\AddinName-SessionId-Reconnect
 
Global\AddinName-SessionId-Disconnect
```

<span data-ttu-id="872e1-134">*AddInName* è la stringa specificata nel valore **nome** della sottochiave del registro di sistema in cui è registrata l'applicazione server.</span><span class="sxs-lookup"><span data-stu-id="872e1-134">*AddinName* is the string specified in the **Name** value of the registry subkey under which the server application is registered.</span></span> <span data-ttu-id="872e1-135">*SessionID* è l'identificatore di sessione di una sessione client.</span><span class="sxs-lookup"><span data-stu-id="872e1-135">*SessionId* is the session identifier of a client session.</span></span>

 

 