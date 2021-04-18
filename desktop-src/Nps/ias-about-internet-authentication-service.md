---
title: Informazioni sulle estensioni NPS
description: In questa sezione viene descritto come implementare le dll per estendere le funzionalità di NPS. Descrive l'interazione tra NPS e le dll e presenta alcune considerazioni di progettazione relative alle DLL.
ms.assetid: 3d4d8d22-4cd3-48e0-b4a4-dfa0a0b7b87f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05878a5243774046c1ca052052d59be9378483d6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300156"
---
# <a name="about-nps-extensions"></a><span data-ttu-id="f499b-104">Informazioni sulle estensioni NPS</span><span class="sxs-lookup"><span data-stu-id="f499b-104">About NPS Extensions</span></span>

> [!Note]  
> <span data-ttu-id="f499b-105">Il servizio di autenticazione Internet (IAS) è stato rinominato server dei criteri di rete (NPS) a partire da Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="f499b-105">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="f499b-106">Il contenuto di questo argomento si applica sia a IAS che a NPS.</span><span class="sxs-lookup"><span data-stu-id="f499b-106">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="f499b-107">In tutto il testo, NPS viene utilizzato per fare riferimento a tutte le versioni del servizio, incluse le versioni originariamente indicate come IAS.</span><span class="sxs-lookup"><span data-stu-id="f499b-107">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="f499b-108">In questa sezione viene descritto come implementare le dll per estendere le funzionalità di NPS.</span><span class="sxs-lookup"><span data-stu-id="f499b-108">This section describes how to implement DLLs to extend the functionality of NPS.</span></span> <span data-ttu-id="f499b-109">Descrive l'interazione tra NPS e le dll e presenta alcune considerazioni di progettazione relative alle DLL.</span><span class="sxs-lookup"><span data-stu-id="f499b-109">It describes the interaction between NPS and the DLLs, and presents some design considerations regarding the DLLs.</span></span>

<span data-ttu-id="f499b-110">NPS fornisce due punti di estensione, uno per l'autenticazione e l'altro per l'autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="f499b-110">NPS provides two extension points, one for authentication and the other for authorization.</span></span> <span data-ttu-id="f499b-111">Per autenticazione si intende la verifica dell'identità dell'utente.</span><span class="sxs-lookup"><span data-stu-id="f499b-111">Authentication refers to verifying the identity of the user.</span></span> <span data-ttu-id="f499b-112">L'autorizzazione si riferisce alla determinazione dei servizi che la rete deve fornire all'utente.</span><span class="sxs-lookup"><span data-stu-id="f499b-112">Authorization refers to determining what services the network should provide to the user.</span></span> <span data-ttu-id="f499b-113">I due punti di estensione corrispondono alle DLL dell'estensione di autenticazione e alle DLL dell'estensione di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="f499b-113">The two extension points correspond to Authentication Extension DLLs and Authorization Extension DLLs.</span></span> <span data-ttu-id="f499b-114">Ogni punto di estensione può supportare più dll.</span><span class="sxs-lookup"><span data-stu-id="f499b-114">Each extension point can support multiple DLLs.</span></span>

<span data-ttu-id="f499b-115">NPS fornisce servizi di autenticazione e autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="f499b-115">NPS provides both authentication and authorization services.</span></span> <span data-ttu-id="f499b-116">Le DLL dell'estensione di autenticazione vengono chiamate da NPS prima dell'autenticazione e dell'autorizzazione del server dei criteri di server.</span><span class="sxs-lookup"><span data-stu-id="f499b-116">Authentication Extension DLLs are called by NPS prior to the built-in NPS authentication and authorization.</span></span> <span data-ttu-id="f499b-117">Le DLL dell'estensione di autorizzazione vengono chiamate dopo l'autenticazione e l'autorizzazione NPS.</span><span class="sxs-lookup"><span data-stu-id="f499b-117">Authorization Extension DLLs are called after NPS authentication and authorization.</span></span>

<span data-ttu-id="f499b-118">Il diagramma seguente illustra il flusso di pacchetti tramite un server RADIUS NPS espanso mediante dll di estensione.</span><span class="sxs-lookup"><span data-stu-id="f499b-118">The following diagram illustrates the flow of packets through an NPS RADIUS server that is expanded using Extension DLLs.</span></span>

![processo di autenticazione e autorizzazione server dei criteri di server](images/ias03.png)

<span data-ttu-id="f499b-120">Se una DLL di estensione di autenticazione restituisce ACCEPT, il pacchetto ignora l'autenticazione NPS e passa direttamente all'autorizzazione NPS.</span><span class="sxs-lookup"><span data-stu-id="f499b-120">If an Authentication Extension DLL returns ACCEPT, the packet skips the NPS authentication and goes directly to NPS authorization.</span></span>

> [!Note]  
> <span data-ttu-id="f499b-121">Quando sono presenti più DLL dell'estensione di autenticazione, è possibile che vengano ignorate anche le altre DLL di estensione.</span><span class="sxs-lookup"><span data-stu-id="f499b-121">When multiple Authentication Extension DLLs are present, the rest of the Extension DLLs might be skipped as well.</span></span> <span data-ttu-id="f499b-122">Per ulteriori informazioni, vedere [configurazione delle DLL di estensione](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls) .</span><span class="sxs-lookup"><span data-stu-id="f499b-122">See [Setting Up the Extension DLLs](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls) for more information.</span></span>

 

<span data-ttu-id="f499b-123">Se una DLL di estensione di autenticazione restituisce CONTINUE, il pacchetto passa all'autenticazione NPS e quindi all'autorizzazione NPS.</span><span class="sxs-lookup"><span data-stu-id="f499b-123">If an Authentication Extension DLL returns CONTINUE, the packet goes to NPS authentication, and then to NPS authorization.</span></span>

> [!Note]  
> <span data-ttu-id="f499b-124">Quando sono presenti più DLL di estensione di autenticazione, le altre DLL dell'estensione di autenticazione vengono richiamate prima dell'autenticazione NPS.</span><span class="sxs-lookup"><span data-stu-id="f499b-124">When multiple Authentication Extension DLLs are present, the rest of the Authentication Extension DLLs are invoked before NPS authentication.</span></span>

 

<span data-ttu-id="f499b-125">Gli argomenti seguenti descrivono le DLL di estensione in modo più dettagliato:</span><span class="sxs-lookup"><span data-stu-id="f499b-125">The following topics describe the Extension DLLs in more detail:</span></span>

-   [<span data-ttu-id="f499b-126">Impostazione delle DLL di estensione</span><span class="sxs-lookup"><span data-stu-id="f499b-126">Setting Up the Extension DLLs</span></span>](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls)
-   [<span data-ttu-id="f499b-127">Richiamo delle DLL di estensione</span><span class="sxs-lookup"><span data-stu-id="f499b-127">Invoking the Extension DLLs</span></span>](/windows/desktop/Nps/ias-authentication-and-authorization-process)
-   [<span data-ttu-id="f499b-128">Attributi di identificazione utente</span><span class="sxs-lookup"><span data-stu-id="f499b-128">User Identification Attributes</span></span>](/windows/desktop/Nps/ias-user-identification-attributes)

 

 