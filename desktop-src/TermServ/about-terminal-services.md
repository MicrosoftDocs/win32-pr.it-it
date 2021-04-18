---
title: Informazioni su Servizi Desktop remoto
description: Servizi Desktop remoto (precedentemente noto come servizi Terminal) fornisce funzionalità simili a quelle di un ambiente basato su terminale, centralizzato o mainframe, in cui più terminali si connettono a un computer host.
ms.assetid: 5b5b0f97-f973-4f52-a965-c9c2390e6c8d
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto Servizi Desktop remoto, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4644170cfca3b4bacdd6db647e35549d56844e9b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298853"
---
# <a name="about-remote-desktop-services"></a><span data-ttu-id="2705c-104">Informazioni su Servizi Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="2705c-104">About Remote Desktop Services</span></span>

<span data-ttu-id="2705c-105">Servizi Desktop remoto (precedentemente noto come servizi Terminal) fornisce funzionalità simili a quelle di un ambiente basato su terminale, centralizzato o mainframe, in cui più terminali si connettono a un computer host.</span><span class="sxs-lookup"><span data-stu-id="2705c-105">Remote Desktop Services (formerly known as Terminal Services) provides functionality similar to a terminal-based, centralized host, or mainframe, environment in which multiple terminals connect to a host computer.</span></span> <span data-ttu-id="2705c-106">Ogni terminale fornisce un canale per l'input e l'output tra un utente e il computer host.</span><span class="sxs-lookup"><span data-stu-id="2705c-106">Each terminal provides a conduit for input and output between a user and the host computer.</span></span> <span data-ttu-id="2705c-107">Un utente può accedere a un terminale e quindi eseguire applicazioni nel computer host, accedere a file, database, risorse di rete e così via.</span><span class="sxs-lookup"><span data-stu-id="2705c-107">A user can log on at a terminal, and then run applications on the host computer, accessing files, databases, network resources, and so on.</span></span> <span data-ttu-id="2705c-108">Ogni sessione terminal è indipendente, con il sistema operativo host che gestisce i conflitti tra più utenti che tendono a condividere le risorse condivise.</span><span class="sxs-lookup"><span data-stu-id="2705c-108">Each terminal session is independent, with the host operating system managing conflicts between multiple users contending for shared resources.</span></span>

<span data-ttu-id="2705c-109">La differenza principale tra Servizi Desktop remoto e l'ambiente mainframe tradizionale è che i terminali muti in un ambiente mainframe forniscono solo input e output basati su caratteri.</span><span class="sxs-lookup"><span data-stu-id="2705c-109">The primary difference between Remote Desktop Services and the traditional mainframe environment is that the dumb terminals in a mainframe environment only provide character-based input and output.</span></span> <span data-ttu-id="2705c-110">Un client o un emulatore di Connessione Desktop remoto (RDC) fornisce un'interfaccia utente grafica completa che include un desktop del sistema operativo Windows e il supporto per un'ampia gamma di dispositivi di input, ad esempio una tastiera e un mouse.</span><span class="sxs-lookup"><span data-stu-id="2705c-110">A Remote Desktop Connection (RDC) client or emulator provides a complete graphical user interface including a Windows operating system desktop and support for a variety of input devices, such as a keyboard and mouse.</span></span>

<span data-ttu-id="2705c-111">Nell'ambiente Servizi Desktop remoto, un'applicazione viene eseguita interamente nel server di host sessione Desktop remoto (host sessione Desktop remoto), in precedenza noto come Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="2705c-111">In the Remote Desktop Services environment, an application runs entirely on the Remote Desktop Session Host (RD Session Host) server (formerly known as a terminal server).</span></span> <span data-ttu-id="2705c-112">Il client RDC non esegue alcuna elaborazione locale del software dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2705c-112">The RDC client performs no local processing of application software.</span></span> <span data-ttu-id="2705c-113">Il server trasmette l'interfaccia utente grafica al client.</span><span class="sxs-lookup"><span data-stu-id="2705c-113">The server transmits the graphical user interface to the client.</span></span> <span data-ttu-id="2705c-114">Il client trasmette di nuovo l'input dell'utente al server.</span><span class="sxs-lookup"><span data-stu-id="2705c-114">The client transmits the user's input back to the server.</span></span>

<span data-ttu-id="2705c-115">Per ulteriori informazioni, vedere gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="2705c-115">For more information, see the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2705c-116">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="2705c-116">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="2705c-117">Modificare il reindirizzamento dei dispositivi predefinito</span><span class="sxs-lookup"><span data-stu-id="2705c-117">Modify Device Redirection Default</span></span>](modify-device-redirection-default-.md)
</dt> <dd>

<span data-ttu-id="2705c-118">Poiché Desktop remoto server gateway tentano di applicare criteri di reindirizzamento dei dispositivi sicuri prima di passare la connessione client tramite a un server host sessione Desktop remoto, potrebbe essere necessario disabilitare questa impostazione predefinita in alcuni casi.</span><span class="sxs-lookup"><span data-stu-id="2705c-118">Because Remote Desktop Gateway servers attempt to enforce secure device redirection policies before passing the client connection through to a Remote Desktop Session Host server, you may need to disable this default in some cases.</span></span>

</dd> <dt>

[<span data-ttu-id="2705c-119">Remote Desktop Protocol</span><span class="sxs-lookup"><span data-stu-id="2705c-119">Remote Desktop Protocol</span></span>](remote-desktop-protocol.md)
</dt> <dd>

<span data-ttu-id="2705c-120">Il protocollo Desktop remoto Microsoft (RDP) fornisce funzionalità di visualizzazione e input Remote sulle connessioni di rete per le applicazioni basate su Windows in esecuzione in un server.</span><span class="sxs-lookup"><span data-stu-id="2705c-120">The Microsoft Remote Desktop Protocol (RDP) provides remote display and input capabilities over network connections for Windows-based applications running on a server.</span></span>

</dd> <dt>

[<span data-ttu-id="2705c-121">API Servizi Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="2705c-121">Remote Desktop Services API</span></span>](terminal-services-api.md)
</dt> <dd>

<span data-ttu-id="2705c-122">L'API Servizi Desktop remoto è particolarmente utile per le applicazioni client/server e le applicazioni per Servizi Desktop remoto l'amministrazione.</span><span class="sxs-lookup"><span data-stu-id="2705c-122">The Remote Desktop Services API is primarily useful to client/server applications and applications for Remote Desktop Services administration.</span></span>

</dd> <dt>

[<span data-ttu-id="2705c-123">Applicazioni di gestione Servizi Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="2705c-123">Remote Desktop Services management applications</span></span>](terminal-services-management-applications.md)
</dt> <dd>

<span data-ttu-id="2705c-124">Descrive le applicazioni di gestione supportate da Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="2705c-124">Describes the management applications that Remote Desktop Services supports.</span></span>

</dd> <dt>

[<span data-ttu-id="2705c-125">Linee guida per la programmazione Servizi Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="2705c-125">Remote Desktop Services programming guidelines</span></span>](terminal-services-programming-guidelines.md)
</dt> <dd>

<span data-ttu-id="2705c-126">Argomenti che forniscono linee guida per lo sviluppo di applicazioni in un ambiente Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="2705c-126">Topics that provide guidelines for developing applications in a Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="2705c-127">Sessioni di Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="2705c-127">Remote Desktop Sessions</span></span>](terminal-services-sessions.md)
</dt> <dd>

<span data-ttu-id="2705c-128">Poiché ogni accesso a un client di Connessione Desktop remoto (RDC) riceve un ID sessione separato, l'esperienza utente è simile a quella di essere connessi contemporaneamente a più computer; ad esempio, un computer Office e un computer di casa.</span><span class="sxs-lookup"><span data-stu-id="2705c-128">Because each logon to a Remote Desktop Connection (RDC) client receives a separate session ID, the user-experience is similar to being logged on to multiple computers at the same time; for example, an office computer and a home computer.</span></span>

</dd> <dt>

[<span data-ttu-id="2705c-129">Connessione Web Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="2705c-129">Remote Desktop Web Connection</span></span>](remote-desktop-web-connection.md)
</dt> <dd>

<span data-ttu-id="2705c-130">Viene descritto come installare un Connessione Web Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="2705c-130">Describes how to install a Remote Desktop Web Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="2705c-131">Risorse in un server di host sessione Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="2705c-131">Resources on a Remote Desktop Session Host Server</span></span>](resources-on-a-terminal-server.md)
</dt> <dd>

<span data-ttu-id="2705c-132">Più utenti possono accedere simultaneamente a un singolo server Host sessione Desktop remoto, condividendo le risorse hardware e software del server.</span><span class="sxs-lookup"><span data-stu-id="2705c-132">Multiple users can log on simultaneously to a single RD Session Host server, sharing the hardware and software resources of the server.</span></span>

</dd> <dt>

[<span data-ttu-id="2705c-133">Novità di Servizi Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="2705c-133">What's New in Remote Desktop Services</span></span>](what-s-new-in-terminal-services.md)
</dt> <dd>

<span data-ttu-id="2705c-134">Argomenti che descrivono le modifiche apportate a ogni versione dell'API Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="2705c-134">Topics that describe the changes in each release of the Remote Desktop Services API.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="2705c-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2705c-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2705c-136">Connettersi a un altro computer utilizzando Connessione Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="2705c-136">Connect to another computer using Remote Desktop Connection</span></span>](https://windows.microsoft.com/windows/connect-using-remote-desktop-connection#connect-using-remote-desktop-connection=windows-7)
</dt> </dl>

 

 




