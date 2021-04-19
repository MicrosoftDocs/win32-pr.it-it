---
title: Utilizzo di Servizi Desktop remoto
description: Come programmare nell'ambiente Servizi Desktop remoto e come estendere la tecnologia di Servizi Desktop remoto (precedentemente nota come servizi Terminal) al Web utilizzando Connessione Web Desktop remoto.
ms.assetid: 17a8055c-3fde-4ba0-9ed9-af0ebe0a36b9
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto Servizi Desktop remoto utilizzando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac575a89d1ae8c7c065199aca136f2f0e5fc7459
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298337"
---
# <a name="using-remote-desktop-services"></a><span data-ttu-id="854cf-104">Utilizzo di Servizi Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="854cf-104">Using Remote Desktop Services</span></span>

<span data-ttu-id="854cf-105">Nelle sezioni seguenti viene descritto come programmare nell'ambiente Servizi Desktop remoto e come estendere la tecnologia di Servizi Desktop remoto (precedentemente nota come servizi Terminal) al Web utilizzando Connessione Web Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="854cf-105">The following sections describe how to program in the Remote Desktop Services environment and how to extend Remote Desktop Services (formerly known as Terminal Services) technology to the web by using Remote Desktop Web Connection.</span></span> <span data-ttu-id="854cf-106">Per informazioni sull'utente per le connessioni Desktop remoto, vedere [connettersi a un altro computer usando connessione Desktop remoto](https://windows.microsoft.com/windows/connect-using-remote-desktop-connection#connect-using-remote-desktop-connection=windows-7).</span><span class="sxs-lookup"><span data-stu-id="854cf-106">If you are looking for user information for Remote Desktop connections, See [Connect to another computer using Remote Desktop Connection](https://windows.microsoft.com/windows/connect-using-remote-desktop-connection#connect-using-remote-desktop-connection=windows-7).</span></span>

> [!Note]  
> <span data-ttu-id="854cf-107">Questo argomento è per gli sviluppatori di software.</span><span class="sxs-lookup"><span data-stu-id="854cf-107">This topic is for software developers.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="854cf-108">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="854cf-108">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="854cf-109">Rilevamento dell'installazione del ruolo Servizi Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="854cf-109">Detecting Whether the Remote Desktop Services Role Is Installed</span></span>](detecting-whether-terminal-services-is-installed.md)
</dt> <dd>

<span data-ttu-id="854cf-110">Esempio di codice C# che mostra un metodo che restituisce **true** se il ruolo del server Servizi Desktop remoto è installato e in esecuzione o **false** in caso contrario, a partire da Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="854cf-110">C# code example that shows a method that returns **True** if the Remote Desktop Services server role is installed and running or **false** otherwise, beginning with Windows Server 2008.</span></span>

</dd> <dt>

[<span data-ttu-id="854cf-111">Estensione di broker di sessione di Servizi terminal</span><span class="sxs-lookup"><span data-stu-id="854cf-111">Extending Terminal Services Session Broker</span></span>](extending-ts-session-broker.md)
</dt> <dd>

<span data-ttu-id="854cf-112">È possibile estendere broker di sessione di Servizi terminal tramite l'interfaccia com [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) .</span><span class="sxs-lookup"><span data-stu-id="854cf-112">You can extend TS Session Broker by using the [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) COM interface.</span></span>

</dd> <dt>

[<span data-ttu-id="854cf-113">Implementazione di un enumeratore di endpoint audio personalizzato</span><span class="sxs-lookup"><span data-stu-id="854cf-113">Implementing a Custom Audio Endpoint Enumerator</span></span>](implementing-an-audio-endpoint-enumerator.md)
</dt> <dd>

<span data-ttu-id="854cf-114">A partire da Windows Server 2008 R2, è possibile implementare un enumeratore endpoint audio remoto personalizzato come parte di un provider di protocollo Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="854cf-114">Beginning with Windows Server 2008 R2, you can implement a custom remote audio endpoint enumerator as part of a Remote Desktop protocol provider.</span></span>

</dd> <dt>

[<span data-ttu-id="854cf-115">Moniker della sessione</span><span class="sxs-lookup"><span data-stu-id="854cf-115">Session Monikers</span></span>](session-monikers.md)
</dt> <dd>

<span data-ttu-id="854cf-116">Distributed COM (DCOM) consente l'attivazione di oggetti in base a ogni sessione usando un moniker di sessione fornito dal sistema.</span><span class="sxs-lookup"><span data-stu-id="854cf-116">Distributed COM (DCOM) enables object activation on a per-session basis by using a system-supplied session moniker.</span></span>

</dd> <dt>

[<span data-ttu-id="854cf-117">Uso dell'estensione ADSI per la configurazione di Servizi Desktop remoto utente</span><span class="sxs-lookup"><span data-stu-id="854cf-117">Using the ADSI Extension for Remote Desktop Services User Configuration</span></span>](using-the-adsi-extension-for-terminal-services-user-configuration.md)
</dt> <dd>

<span data-ttu-id="854cf-118">L'amministrazione delle proprietà utente specifiche di Servizi Desktop remoto è possibile utilizzando i metodi implementati dall'estensione ADSI (Active Directory Service Interfaces), assemblata con la libreria a collegamento dinamico Tsuserex.dll.</span><span class="sxs-lookup"><span data-stu-id="854cf-118">Administration of Remote Desktop Services-specific user properties is possible by using the methods implemented by the Active Directory Service Interfaces (ADSI) extension, which is packaged with the dynamic-link library Tsuserex.dll.</span></span>

</dd> <dt>

[<span data-ttu-id="854cf-119">Uso dell'API Servizi Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="854cf-119">Using the Remote Desktop Services API</span></span>](using-the-terminal-services-api.md)
</dt> <dd>

<span data-ttu-id="854cf-120">Viene descritto come utilizzare l'API Servizi Desktop remoto per consentire alle applicazioni di eseguire attività in un ambiente Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="854cf-120">Describes how you can use the Remote Desktop Services API to enable applications to perform tasks in a Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="854cf-121">Uso dell'API di virtualizzazione Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="854cf-121">Using the Remote Desktop Virtualization API</span></span>](using-the-remote-desktop-virtualization-api.md)
</dt> <dd>

<span data-ttu-id="854cf-122">Gli sviluppatori possono utilizzare questa API per personalizzare la logica utilizzata da Connessione Desktop remoto broker di connessione Desktop remoto per determinare la destinazione migliore per una connessione client in ingresso.</span><span class="sxs-lookup"><span data-stu-id="854cf-122">Developers can use this API to customize the logic that Remote Desktop Connection Broker (RD Connection Broker) uses to determine the best destination for an incoming client connection.</span></span>

</dd> <dt>

[<span data-ttu-id="854cf-123">Interfaccia WSDL per soluzioni VDI personalizzate</span><span class="sxs-lookup"><span data-stu-id="854cf-123">WSDL Interface for Custom VDI Solutions</span></span>](wsdl-interface-for-custom-vdi-solutions.md)
</dt> <dd>

<span data-ttu-id="854cf-124">Gli sviluppatori possono creare servizi Web personalizzati che gestiscono soluzioni VDI (Virtual Desktop Infrastructure).</span><span class="sxs-lookup"><span data-stu-id="854cf-124">Developers can create custom web services that manage virtual desktop infrastructure (VDI) solutions.</span></span>

</dd> </dl>

<span data-ttu-id="854cf-125">Per ulteriori informazioni, vedere [Servizi Desktop remoto linee guida](terminal-services-programming-guidelines.md)per la programmazione.</span><span class="sxs-lookup"><span data-stu-id="854cf-125">For more information, see [Remote Desktop Services Programming Guidelines](terminal-services-programming-guidelines.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="854cf-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="854cf-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="854cf-127">Servizi terminal è ora Servizi Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="854cf-127">Terminal Services Is Now Remote Desktop Services</span></span>](terminal-services-is-now-remote-desktop-services.md)
</dt> <dt>

[<span data-ttu-id="854cf-128">Rilevamento dell'ambiente Servizi Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="854cf-128">Detecting the Remote Desktop Services Environment</span></span>](detecting-the-terminal-services-environment.md)
</dt> </dl>

 

 




