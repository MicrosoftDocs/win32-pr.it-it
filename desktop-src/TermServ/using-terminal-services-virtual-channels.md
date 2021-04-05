---
title: Uso di Servizi Desktop remoto canali virtuali
description: Per implementare un canale virtuale, fornire i moduli server e client dell'applicazione di un canale virtuale.
ms.assetid: 3b378071-ebd6-47b0-8a9c-3e671505011a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 539eafca38c19855fdb057ceeb6e79cb4613773a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708752"
---
# <a name="using-remote-desktop-services-virtual-channels"></a><span data-ttu-id="5409d-103">Uso di Servizi Desktop remoto canali virtuali</span><span class="sxs-lookup"><span data-stu-id="5409d-103">Using Remote Desktop Services virtual channels</span></span>

<span data-ttu-id="5409d-104">Per implementare un canale virtuale, fornire i moduli server e client dell'applicazione di un canale virtuale.</span><span class="sxs-lookup"><span data-stu-id="5409d-104">To implement a virtual channel, you provide the server and client modules of a virtual channel's application.</span></span> <span data-ttu-id="5409d-105">Il modulo server può essere un'applicazione in modalità utente o un driver in modalità kernel.</span><span class="sxs-lookup"><span data-stu-id="5409d-105">The server module can be a user-mode application or a kernel-mode driver.</span></span> <span data-ttu-id="5409d-106">Il modulo client deve essere una DLL.</span><span class="sxs-lookup"><span data-stu-id="5409d-106">The client module must be a DLL.</span></span>

<span data-ttu-id="5409d-107">Per le descrizioni di questi moduli, vedere gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="5409d-107">For descriptions of these modules, see the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5409d-108">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="5409d-108">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="5409d-109">Applicazione Virtual Channel Server</span><span class="sxs-lookup"><span data-stu-id="5409d-109">Virtual Channel Server Application</span></span>](virtual-channel-server-application.md)
</dt> <dd>

<span data-ttu-id="5409d-110">Il modulo server di un'applicazione che usa canali virtuali deve essere un'applicazione in modalità utente in esecuzione in una sessione client nel server host sessione Desktop remoto (host sessione Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="5409d-110">The server module of an application that uses virtual channels must be a user-mode application running in a client session on the Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="5409d-111">Si noti che è necessario fornire un metodo per avviare l'applicazione server.</span><span class="sxs-lookup"><span data-stu-id="5409d-111">Note that you must provide a method to start the server application.</span></span>

</dd> <dt>

[<span data-ttu-id="5409d-112">DLL client canale virtuale</span><span class="sxs-lookup"><span data-stu-id="5409d-112">Virtual Channel Client DLL</span></span>](virtual-channel-client-dll.md)
</dt> <dd>

<span data-ttu-id="5409d-113">Il client di un'applicazione di canali virtuali è una DLL caricata durante l'inizializzazione del Servizi Desktop remoto nel computer client.</span><span class="sxs-lookup"><span data-stu-id="5409d-113">The client of a virtual channels application is a DLL that is loaded during the Remote Desktop Services initialization on the client computer.</span></span> <span data-ttu-id="5409d-114">La DLL deve essere registrata nel computer client.</span><span class="sxs-lookup"><span data-stu-id="5409d-114">The DLL must be registered on the client computer.</span></span>

</dd> <dt>

[<span data-ttu-id="5409d-115">Registrazione client del canale virtuale</span><span class="sxs-lookup"><span data-stu-id="5409d-115">Virtual Channel Client Registration</span></span>](virtual-channel-client-registration.md)
</dt> <dd>

<span data-ttu-id="5409d-116">È necessario archiviare il nome della DLL client nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="5409d-116">You must store the name of the client DLL in the registry.</span></span>

</dd> <dt>

[<span data-ttu-id="5409d-117">Canale virtuale persistente del controllo remoto</span><span class="sxs-lookup"><span data-stu-id="5409d-117">Remote Control Persistent Virtual Channels</span></span>](remote-control-persistent-virtual-channels.md)
</dt> <dd>

<span data-ttu-id="5409d-118">Un canale virtuale persistente del controllo remoto non viene chiuso quando un controllo remoto si connette o si disconnette per la sessione connessa al client.</span><span class="sxs-lookup"><span data-stu-id="5409d-118">A remote control persistent virtual channel is not closed when a remote control connects or disconnects for the session connected to the client.</span></span> <span data-ttu-id="5409d-119">I dati continueranno a essere trasmessi e ricevuti tramite questo canale.</span><span class="sxs-lookup"><span data-stu-id="5409d-119">Data will continue to be transmitted and received through this channel.</span></span>

</dd> <dt>

[<span data-ttu-id="5409d-120">Canali virtuali dinamici</span><span class="sxs-lookup"><span data-stu-id="5409d-120">Dynamic Virtual Channels</span></span>](dynamic-virtual-channels.md)
</dt> <dd>

<span data-ttu-id="5409d-121">Le API del canale virtuale dinamico (DVC) estendono le API del canale virtuale esistente per Servizi Desktop remoto, note come API del canale virtuale statico (SVC).</span><span class="sxs-lookup"><span data-stu-id="5409d-121">Dynamic virtual channel (DVC) APIs extend the existing virtual channel APIs for Remote Desktop Services, known as static virtual channel (SVC) APIs.</span></span>

</dd> </dl>

<span data-ttu-id="5409d-122">Se è stata abilitata l'applicazione di un canale virtuale nella distribuzione di Servizi Desktop remoto, è anche possibile rendere disponibile l'applicazione ai computer client che accedono al server Host sessione Desktop remoto tramite il controllo ActiveX Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="5409d-122">If you have enabled a virtual channel's application in your Remote Desktop Services deployment, you can also make the application available to client computers that access the RD Session Host server by means of the Remote Desktop ActiveX control.</span></span> <span data-ttu-id="5409d-123">Per ulteriori informazioni, vedere [utilizzo del controllo ActiveX Desktop remoto con i canali virtuali](using-the-remote-desktop-activex-control-with-virtual-channels.md).</span><span class="sxs-lookup"><span data-stu-id="5409d-123">For more information, see [Using the Remote Desktop ActiveX Control with Virtual Channels](using-the-remote-desktop-activex-control-with-virtual-channels.md).</span></span>

 

 




