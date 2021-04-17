---
title: Oggetti dati del server
description: L'API SDO (Server Data Objects) consente di configurare e amministrare a livello di codice un sistema che esegue NPS.
ms.assetid: 9d159e15-f534-4ab1-9641-db70064beb51
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eebd0f837f9a8a36af1eb9118189015e677e2af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300076"
---
# <a name="server-data-objects"></a><span data-ttu-id="df3e0-103">Oggetti dati del server</span><span class="sxs-lookup"><span data-stu-id="df3e0-103">Server Data Objects</span></span>

> [!Note]  
> <span data-ttu-id="df3e0-104">Il servizio di autenticazione Internet (IAS) è stato rinominato server dei criteri di rete (NPS) a partire da Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="df3e0-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="df3e0-105">Il contenuto di questo argomento si applica sia a IAS che a NPS.</span><span class="sxs-lookup"><span data-stu-id="df3e0-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="df3e0-106">In tutto il testo, NPS viene utilizzato per fare riferimento a tutte le versioni del servizio, incluse le versioni originariamente indicate come IAS.</span><span class="sxs-lookup"><span data-stu-id="df3e0-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="df3e0-107">L'API SDO (Server Data Objects) consente di configurare e amministrare a livello di codice un sistema che esegue NPS.</span><span class="sxs-lookup"><span data-stu-id="df3e0-107">The Server Data Objects (SDO) API makes it possible to programmatically configure and administer a system running NPS.</span></span> <span data-ttu-id="df3e0-108">Usando SDO, uno sviluppatore può anche scrivere applicazioni che gestiscono profili e criteri di accesso remoto.</span><span class="sxs-lookup"><span data-stu-id="df3e0-108">Using SDO, a developer can also write applications that administer remote access policies and profiles.</span></span> <span data-ttu-id="df3e0-109">I criteri e i profili di accesso remoto vengono utilizzati dal servizio Routing e accesso remoto (RRAS), nonché da server dei criteri di rete per determinare se un client remoto è autorizzato a connettersi a un server di accesso alla rete (NAS).</span><span class="sxs-lookup"><span data-stu-id="df3e0-109">The remote access policies and profiles are used by the Routing and Remote Access Service (RRAS) as well as NPS to determine whether a remote client is allowed to connect to a network access server (NAS).</span></span>

<span data-ttu-id="df3e0-110">L'API SDO è applicabile in qualsiasi ambiente che utilizza criteri di accesso remoto o NPS.</span><span class="sxs-lookup"><span data-stu-id="df3e0-110">The SDO API is applicable in any environment that uses NPS or Remote Access Policies.</span></span>

<span data-ttu-id="df3e0-111">Con l'API SDO, uno sviluppatore può modificare qualsiasi elemento della configurazione NPS accessibile tramite l'interfaccia utente del server dei criteri di server.</span><span class="sxs-lookup"><span data-stu-id="df3e0-111">With the SDO API, a developer can manipulate any element of the NPS configuration that is accessible through the NPS user interface.</span></span>

<span data-ttu-id="df3e0-112">L'API SDO consente inoltre di impostare o recuperare i valori accessibili tramite la pagina delle proprietà impostazioni di connessione remota utente.</span><span class="sxs-lookup"><span data-stu-id="df3e0-112">The SDO API also makes it possible to set or retrieve any of the values accessible through the user dial-in settings property page.</span></span>

<span data-ttu-id="df3e0-113">L'API SDO è costituita da interfacce COM.</span><span class="sxs-lookup"><span data-stu-id="df3e0-113">The SDO API is composed of COM interfaces.</span></span> <span data-ttu-id="df3e0-114">Ognuna delle interfacce nell'API SDO eredita dall'interfaccia COM [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="df3e0-114">Each of the interfaces in the SDO API inherits from the COM [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="df3e0-115">L'interfaccia **IDispatch** consente agli sviluppatori di chiamare i metodi dell'interfaccia SDO da Visual Basic o da qualsiasi client di automazione, nonché da C/C++.</span><span class="sxs-lookup"><span data-stu-id="df3e0-115">The **IDispatch** interface enables developers to call the SDO interface methods from Visual Basic or any Automation client, as well as from C/C++.</span></span>

<span data-ttu-id="df3e0-116">Gli sviluppatori possono anche chiamare l'API SDO da linguaggi di scripting, ad esempio VBScript.</span><span class="sxs-lookup"><span data-stu-id="df3e0-116">Developers can also call the SDO API from scripting languages such as VBScript.</span></span> <span data-ttu-id="df3e0-117">Tuttavia, poiché VBScript è limitato all'uso dei soli parametri di tipo VARIANT, non tutte le funzionalità di SDO sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="df3e0-117">However, because VBScript is limited to using VARIANT-type parameters only, not all the functionality of SDO is available.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="df3e0-118">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="df3e0-118">In This Section</span></span>

[<span data-ttu-id="df3e0-119">Overview</span><span class="sxs-lookup"><span data-stu-id="df3e0-119">Overview</span></span>](/windows/desktop/Nps/sdo-about-server-data-objects)

<span data-ttu-id="df3e0-120">Informazioni generali sull'API oggetti dati server.</span><span class="sxs-lookup"><span data-stu-id="df3e0-120">General information about the Server Data Objects API.</span></span>

[<span data-ttu-id="df3e0-121">Usando</span><span class="sxs-lookup"><span data-stu-id="df3e0-121">Using</span></span>](/windows/desktop/Nps/sdo-using-server-data-objects)

<span data-ttu-id="df3e0-122">Codice di esempio che illustra come usare l'API di oggetti dati del server.</span><span class="sxs-lookup"><span data-stu-id="df3e0-122">Sample code that demonstrates how to use the Server Data Objects API.</span></span>

[<span data-ttu-id="df3e0-123">Riferimento</span><span class="sxs-lookup"><span data-stu-id="df3e0-123">Reference</span></span>](/windows/desktop/Nps/sdo-server-data-objects-reference)

<span data-ttu-id="df3e0-124">Documentazione dei tipi enumerati e delle interfacce che compongono l'API oggetti dati server.</span><span class="sxs-lookup"><span data-stu-id="df3e0-124">Documentation of the enumerated types and interfaces that compose the Server Data Objects API.</span></span>

## <a name="related-topics"></a><span data-ttu-id="df3e0-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="df3e0-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df3e0-126">Server dei criteri di rete (servizio di autenticazione Internet)</span><span class="sxs-lookup"><span data-stu-id="df3e0-126">Network Policy Server (Internet Authentication Service)</span></span>](portal.md)
</dt> <dt>

[<span data-ttu-id="df3e0-127">Servizio di accesso remoto</span><span class="sxs-lookup"><span data-stu-id="df3e0-127">Remote Access Service</span></span>](/windows/desktop/RRAS/portal)
</dt> </dl>

 

 