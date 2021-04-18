---
title: Servizi Desktop remoto (Servizi Desktop remoto)
description: Desktop remoto Microsoft Services è un software di accesso remoto al PC che supporta l'accesso desktop remoto. Servizi Desktop remoto connette più client a un server di host sessione Desktop remoto (host sessione Desktop remoto).
ms.assetid: 90c40b7a-e324-43fc-a1e6-f29997ed9436
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto Servizi Desktop remoto
- Servizi Desktop remoto Servizi Desktop remoto, home page
- Servizi Terminal vedere Servizi Desktop remoto Servizi Desktop remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f39e176473c98f1e240d58592463df749a95f939
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300894"
---
# <a name="remote-desktop-services-remote-desktop-services"></a><span data-ttu-id="76d6b-107">Servizi Desktop remoto (Servizi Desktop remoto)</span><span class="sxs-lookup"><span data-stu-id="76d6b-107">Remote Desktop Services (Remote Desktop Services)</span></span>

## <a name="purpose"></a><span data-ttu-id="76d6b-108">Scopo</span><span class="sxs-lookup"><span data-stu-id="76d6b-108">Purpose</span></span>

<span data-ttu-id="76d6b-109">Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 o Windows Server 2008 con Servizi Desktop remoto (precedentemente noto come servizi Terminal) consentono a un server di ospitare più sessioni client simultanee.</span><span class="sxs-lookup"><span data-stu-id="76d6b-109">Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2, or Windows Server 2008 with Remote Desktop Services (formerly known as Terminal Services) allow a server to host multiple, simultaneous client sessions.</span></span> <span data-ttu-id="76d6b-110">Desktop remoto usa la tecnologia Servizi Desktop remoto per consentire l'esecuzione remota di una singola sessione.</span><span class="sxs-lookup"><span data-stu-id="76d6b-110">Remote Desktop uses Remote Desktop Services technology to allow a single session to run remotely.</span></span> <span data-ttu-id="76d6b-111">Un utente può connettersi a un server di host sessione Desktop remoto (host sessione Desktop remoto) (in precedenza noto come Terminal Server) utilizzando il software client Connessione Desktop remoto (RDC).</span><span class="sxs-lookup"><span data-stu-id="76d6b-111">A user can connect to a Remote Desktop Session Host (RD Session Host) server (formerly known as a terminal server) by using Remote Desktop Connection (RDC) client software.</span></span> <span data-ttu-id="76d6b-112">Il Connessione Web Desktop remoto estende la tecnologia Servizi Desktop remoto al Web.</span><span class="sxs-lookup"><span data-stu-id="76d6b-112">The Remote Desktop Web Connection extends Remote Desktop Services technology to the web.</span></span>

> [!Note]  
> <span data-ttu-id="76d6b-113">Questo argomento è per gli sviluppatori di software.</span><span class="sxs-lookup"><span data-stu-id="76d6b-113">This topic is for software developers.</span></span> <span data-ttu-id="76d6b-114">Per informazioni sull'utente per le connessioni Desktop remoto, vedere [Connessione desktop remoto: domande frequenti](https://windows.microsoft.com/windows/remote-desktop-connection-faq#1TC=windows-8).</span><span class="sxs-lookup"><span data-stu-id="76d6b-114">If you are looking for user information for Remote Desktop connections, See [Remote Desktop Connection: frequently asked questions](https://windows.microsoft.com/windows/remote-desktop-connection-faq#1TC=windows-8).</span></span>

 

## <a name="where-applicable"></a><span data-ttu-id="76d6b-115">Se applicabile</span><span class="sxs-lookup"><span data-stu-id="76d6b-115">Where applicable</span></span>

<span data-ttu-id="76d6b-116">Un client Connessione Desktop remoto (RDC) può esistere in un'ampia gamma di moduli.</span><span class="sxs-lookup"><span data-stu-id="76d6b-116">A Remote Desktop Connection (RDC) client can exist in a variety of forms.</span></span> <span data-ttu-id="76d6b-117">I dispositivi hardware thin client che eseguono un sistema operativo basato su Windows incorporato possono eseguire il software client RDC per connettersi a un server Host sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="76d6b-117">Thin-client hardware devices that run an embedded Windows-based operating system can run the RDC client software to connect to an RD Session Host server.</span></span> <span data-ttu-id="76d6b-118">I computer basati su Windows, Macintosh o UNIX possono eseguire il software client RDC per connettersi a un server Host sessione Desktop remoto per visualizzare le applicazioni basate su Windows.</span><span class="sxs-lookup"><span data-stu-id="76d6b-118">Windows-, Macintosh-, or UNIX-based computers can run RDC client software to connect to an RD Session Host server to display Windows-based applications.</span></span> <span data-ttu-id="76d6b-119">Questa combinazione di client RDC consente di accedere alle applicazioni basate su Windows praticamente da qualsiasi sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="76d6b-119">This combination of RDC clients provides access to Windows-based applications from virtually any operating system.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="76d6b-120">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="76d6b-120">Developer audience</span></span>

<span data-ttu-id="76d6b-121">Gli sviluppatori che utilizzano Servizi Desktop remoto devono acquisire familiarità con i linguaggi di programmazione C e C++ e con l'ambiente di programmazione basato su Windows.</span><span class="sxs-lookup"><span data-stu-id="76d6b-121">Developers who use Remote Desktop Services should be familiar with the C and C++ programming languages and the Windows-based programming environment.</span></span> <span data-ttu-id="76d6b-122">È necessaria una certa familiarità con l'architettura client/server.</span><span class="sxs-lookup"><span data-stu-id="76d6b-122">Familiarity with client/server architecture is required.</span></span> <span data-ttu-id="76d6b-123">Il Connessione Web Desktop remoto include interfacce di script per la creazione e la distribuzione di canali virtuali tramite script all'interno di Servizi Desktop remoto applicazioni Web.</span><span class="sxs-lookup"><span data-stu-id="76d6b-123">The Remote Desktop Web Connection includes scriptable interfaces to create and deploy scriptable virtual channels within Remote Desktop Services web applications.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="76d6b-124">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="76d6b-124">Run-time requirements</span></span>

<span data-ttu-id="76d6b-125">Le applicazioni che usano Servizi Desktop remoto richiedono Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="76d6b-125">Applications that use Remote Desktop Services require Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008, or Windows Vista.</span></span> <span data-ttu-id="76d6b-126">Per utilizzare Connessione Web Desktop remoto funzionalità, l'applicazione client Servizi Desktop remoto richiede Internet Explorer e una connessione al World Wide Web.</span><span class="sxs-lookup"><span data-stu-id="76d6b-126">To use Remote Desktop Web Connection functionality, the Remote Desktop Services client application requires Internet Explorer and a connection to the World Wide Web.</span></span> <span data-ttu-id="76d6b-127">Per informazioni sui requisiti della fase di esecuzione per un particolare elemento di programmazione, vedere la sezione requisiti della pagina di riferimento per tale elemento.</span><span class="sxs-lookup"><span data-stu-id="76d6b-127">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="76d6b-128">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="76d6b-128">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="76d6b-129">Controllo ActiveX Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="76d6b-129">Remote Desktop ActiveX control</span></span>](remote-desktop-activex-control.md)
</dt> <dd>

<span data-ttu-id="76d6b-130">Viene descritto come utilizzare il controllo ActiveX Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="76d6b-130">Describes how to use the Remote Desktop ActiveX control.</span></span>

</dd> <dt>

[<span data-ttu-id="76d6b-131">API del provider Remote Desktop Protocol</span><span class="sxs-lookup"><span data-stu-id="76d6b-131">Remote Desktop Protocol Provider API</span></span>](custom-remote-desktop-protocols.md)
</dt> <dd>

<span data-ttu-id="76d6b-132">Usare l'API del provider Remote Desktop Protocol per creare un protocollo per fornire la comunicazione tra il servizio Servizi Desktop remoto e più client.</span><span class="sxs-lookup"><span data-stu-id="76d6b-132">You use the Remote Desktop Protocol Provider API to create a protocol to provide communication between the Remote Desktop Services service and multiple clients.</span></span>

</dd> <dt>

[<span data-ttu-id="76d6b-133">Servizi Desktop remoto canali virtuali</span><span class="sxs-lookup"><span data-stu-id="76d6b-133">Remote Desktop Services virtual channels</span></span>](terminal-services-virtual-channels.md)
</dt> <dd>

<span data-ttu-id="76d6b-134">I *canali virtuali* sono estensioni software che possono essere usate per aggiungere miglioramenti funzionali a un'applicazione Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="76d6b-134">*Virtual channels* are software extensions that can be used to add functional enhancements to a Remote Desktop Services application.</span></span>

</dd> <dt>

[<span data-ttu-id="76d6b-135">API di reindirizzamento dei supporti RemoteFX</span><span class="sxs-lookup"><span data-stu-id="76d6b-135">RemoteFX Media Redirection API</span></span>](remotefx-api.md)
</dt> <dd>

<span data-ttu-id="76d6b-136">L'API di reindirizzamento dei supporti RemoteFX viene utilizzata in una sessione di Desktop remoto per identificare le aree del server in cui viene visualizzato il contenuto a modifica rapida, ad esempio il video.</span><span class="sxs-lookup"><span data-stu-id="76d6b-136">The RemoteFX Media Redirection API is used in a Remote Desktop session to identify areas of the server that are displaying fast changing content, such as video.</span></span> <span data-ttu-id="76d6b-137">Questo contenuto può quindi essere codificato come video e inviato al client in formato codificato.</span><span class="sxs-lookup"><span data-stu-id="76d6b-137">This content can then be video encoded and sent to the client in encoded format.</span></span>

</dd> <dt>

[<span data-ttu-id="76d6b-138">API client di Connessione Desktop remoto broker</span><span class="sxs-lookup"><span data-stu-id="76d6b-138">Remote Desktop Connection Broker client API</span></span>](connection-broker-client-api.md)
</dt> <dd>

<span data-ttu-id="76d6b-139">Viene descritto come utilizzare l'API client di Connessione Desktop remoto broker.</span><span class="sxs-lookup"><span data-stu-id="76d6b-139">Describes how to use the Remote Desktop Connection Broker client API.</span></span>

</dd> <dt>

[<span data-ttu-id="76d6b-140">Informazioni di riferimento sull'API personal desktop Task Agent</span><span class="sxs-lookup"><span data-stu-id="76d6b-140">Personal desktop task agent API reference</span></span>](task-agent-api-reference.md)
</dt> <dd>

<span data-ttu-id="76d6b-141">L'API personal desktop Task Agent viene utilizzata per gestire gli aggiornamenti pianificati a un desktop virtuale personale.</span><span class="sxs-lookup"><span data-stu-id="76d6b-141">The personal desktop task agent API is used to handle scheduled updates to a personal virtual desktop.</span></span>

</dd> <dt>

[<span data-ttu-id="76d6b-142">Informazioni su Servizi Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="76d6b-142">About Remote Desktop Services</span></span>](about-terminal-services.md)
</dt> <dd>

<span data-ttu-id="76d6b-143">Servizi Desktop remoto (precedentemente noto come servizi Terminal) fornisce funzionalità simili a quelle di un ambiente basato su terminale, centralizzato o mainframe, in cui più terminali si connettono a un computer host.</span><span class="sxs-lookup"><span data-stu-id="76d6b-143">Remote Desktop Services (formerly known as Terminal Services) provides functionality similar to a terminal-based, centralized host, or mainframe, environment in which multiple terminals connect to a host computer.</span></span>

</dd> <dt>

[<span data-ttu-id="76d6b-144">Provider di Desktop remoto Management Services</span><span class="sxs-lookup"><span data-stu-id="76d6b-144">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> <dd>

<span data-ttu-id="76d6b-145">Il provider Desktop remoto Management Services (RDBMS) gestisce gli ambienti VDI (Virtual Desktop Infrastructure).</span><span class="sxs-lookup"><span data-stu-id="76d6b-145">The Remote Desktop Management Services (RDMS) Provider manages virtual desktop infrastructure (VDI) environments.</span></span>

</dd> <dt>

[<span data-ttu-id="76d6b-146">Riferimento Servizi Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="76d6b-146">Remote Desktop Services reference</span></span>](terminal-services-reference.md)
</dt> <dd>

<span data-ttu-id="76d6b-147">Documentazione dei metodi di proprietà che è possibile utilizzare per esaminare e configurare Servizi Desktop remoto proprietà utente.</span><span class="sxs-lookup"><span data-stu-id="76d6b-147">Documentation of property methods that you can use to examine and configure Remote Desktop Services user properties.</span></span> <span data-ttu-id="76d6b-148">Sono inoltre documentate le funzioni di Servizi Desktop remoto, le strutture e le interfacce Connessione Web Desktop remoto con script.</span><span class="sxs-lookup"><span data-stu-id="76d6b-148">Remote Desktop Services functions, structures, and Remote Desktop Web Connection scriptable interfaces are also documented.</span></span>

</dd> <dt>

[<span data-ttu-id="76d6b-149">Tasti di scelta rapida Servizi Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="76d6b-149">Remote Desktop Services Shortcut Keys</span></span>](terminal-services-shortcut-keys.md)
</dt> <dd>

<span data-ttu-id="76d6b-150">Elenco di tasti di scelta rapida Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="76d6b-150">A list of the Remote Desktop Services shortcut keys.</span></span>

</dd> <dt>

[<span data-ttu-id="76d6b-151">Provider WMI Servizi Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="76d6b-151">Remote Desktop Services WMI provider</span></span>](terminal-services-wmi-provider.md)
</dt> <dd>

<span data-ttu-id="76d6b-152">Il provider WMI Servizi Desktop remoto fornisce accesso a livello di codice alle informazioni e alle impostazioni esposte dallo snap-in Microsoft Management Console (MMC) Servizi Desktop remoto Configuration/Connections.</span><span class="sxs-lookup"><span data-stu-id="76d6b-152">The Remote Desktop Services WMI provider provides programmatic access to the information and settings that are exposed by the Remote Desktop Services Configuration/Connections Microsoft Management Console (MMC) snap-in.</span></span>

</dd> <dt>

[<span data-ttu-id="76d6b-153">Utilizzo di Servizi Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="76d6b-153">Using Remote Desktop Services</span></span>](using-terminal-services.md)
</dt> <dd>

<span data-ttu-id="76d6b-154">Come programmare nell'ambiente Servizi Desktop remoto e come estendere la tecnologia di Servizi Desktop remoto (precedentemente nota come servizi Terminal) al Web utilizzando Connessione Web Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="76d6b-154">How to program in the Remote Desktop Services environment and how to extend Remote Desktop Services (formerly known as Terminal Services) technology to the web by using Remote Desktop Web Connection.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="76d6b-155">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="76d6b-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76d6b-156">Servizi terminal è ora Servizi Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="76d6b-156">Terminal Services Is Now Remote Desktop Services</span></span>](terminal-services-is-now-remote-desktop-services.md)
</dt> </dl>

 

 




