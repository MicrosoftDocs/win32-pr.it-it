---
title: Servizi Desktop remoto canali virtuali
description: I canali virtuali sono estensioni software che possono essere usate per aggiungere miglioramenti funzionali a un'applicazione Servizi Desktop remoto.
ms.assetid: f7bdebec-ecc3-4f28-9327-f0d2f169c142
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce78331841a41502aa337de19e9879d42d85fe1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329700"
---
# <a name="remote-desktop-services-virtual-channels"></a><span data-ttu-id="e90e4-103">Servizi Desktop remoto canali virtuali</span><span class="sxs-lookup"><span data-stu-id="e90e4-103">Remote Desktop Services virtual channels</span></span>

<span data-ttu-id="e90e4-104">I *canali virtuali* sono estensioni software che possono essere usate per aggiungere miglioramenti funzionali a un'applicazione Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="e90e4-104">*Virtual channels* are software extensions that can be used to add functional enhancements to a Remote Desktop Services application.</span></span> <span data-ttu-id="e90e4-105">Esempi di miglioramenti funzionali possono includere: supporto per tipi speciali di hardware, audio o altre aggiunte alle funzionalità di base fornite dalla Servizi Desktop remoto [Remote Desktop Protocol](remote-desktop-protocol.md) (RDP).</span><span class="sxs-lookup"><span data-stu-id="e90e4-105">Examples of functional enhancements might include: support for special types of hardware, audio, or other additions to the core functionality provided by the Remote Desktop Services [Remote Desktop Protocol](remote-desktop-protocol.md) (RDP).</span></span> <span data-ttu-id="e90e4-106">Il protocollo RDP fornisce la gestione multiplexata di più canali virtuali.</span><span class="sxs-lookup"><span data-stu-id="e90e4-106">The RDP protocol provides multiplexed management of multiple virtual channels.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e90e4-107">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="e90e4-107">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="e90e4-108">Uso di Servizi Desktop remoto canali virtuali</span><span class="sxs-lookup"><span data-stu-id="e90e4-108">Using Remote Desktop Services virtual channels</span></span>](using-terminal-services-virtual-channels.md)
</dt> <dd>

<span data-ttu-id="e90e4-109">Per implementare un canale virtuale, fornire i moduli server e client dell'applicazione di un canale virtuale.</span><span class="sxs-lookup"><span data-stu-id="e90e4-109">To implement a virtual channel, you provide the server and client modules of a virtual channel's application.</span></span>

</dd> <dt>

[<span data-ttu-id="e90e4-110">Guida di riferimento ai canali virtuali dinamici</span><span class="sxs-lookup"><span data-stu-id="e90e4-110">Dynamic virtual channels reference</span></span>](dynamic-virtual-channels-reference.md)
</dt> <dd>

<span data-ttu-id="e90e4-111">Le interfacce client dinamiche del canale virtuale (DVC) sono supportate da Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="e90e4-111">Dynamic virtual channel (DVC) client interfaces are supported by Remote Desktop Services.</span></span>

</dd> <dt>

[<span data-ttu-id="e90e4-112">Informazioni di riferimento sui canali virtuali grafici</span><span class="sxs-lookup"><span data-stu-id="e90e4-112">Graphics virtual channels reference</span></span>](graphics-virtual-channels-reference.md)
</dt> <dd>

<span data-ttu-id="e90e4-113">La Guida di riferimento ai canali virtuali grafici contiene elementi di programmazione che consentono di creare un canale di grafica virtuale.</span><span class="sxs-lookup"><span data-stu-id="e90e4-113">The graphics virtual channels reference contains programming elements that enable you to create a virtual graphics channel.</span></span>

</dd> </dl>

<span data-ttu-id="e90e4-114">Un'applicazione di canale virtuale è costituita da due parti, un modulo client e un modulo server.</span><span class="sxs-lookup"><span data-stu-id="e90e4-114">A virtual channel application has two parts, a client module and a server module.</span></span> <span data-ttu-id="e90e4-115">Il modulo server è un programma eseguibile in esecuzione nel server host sessione Desktop remoto (host sessione Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="e90e4-115">The server module is an executable program running on the Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="e90e4-116">Il modulo client è una DLL che deve essere caricata in memoria sul computer client durante l'esecuzione del programma client di Connessione Desktop remoto (RDC).</span><span class="sxs-lookup"><span data-stu-id="e90e4-116">The client module is a DLL that must be loaded into memory on the client computer when the Remote Desktop Connection (RDC) client program runs.</span></span>

<span data-ttu-id="e90e4-117">I canali virtuali possono aggiungere miglioramenti funzionali a un client Connessione Desktop remoto (RDC), indipendentemente dal protocollo RDP.</span><span class="sxs-lookup"><span data-stu-id="e90e4-117">Virtual channels can add functional enhancements to a Remote Desktop Connection (RDC) client, independent of the RDP protocol.</span></span> <span data-ttu-id="e90e4-118">Con il supporto dei canali virtuali, è possibile aggiungere nuove funzionalità senza dover aggiornare il software client o server o il protocollo RDP.</span><span class="sxs-lookup"><span data-stu-id="e90e4-118">With virtual channel support, new features can be added without having to update the client or server software, or the RDP protocol.</span></span>

<span data-ttu-id="e90e4-119">Sono state identificate quattro classi principali di utenti di canali virtuali:</span><span class="sxs-lookup"><span data-stu-id="e90e4-119">Four major classes of users of virtual channels have been identified:</span></span>

-   <span data-ttu-id="e90e4-120">Driver in modalità kernel generale, ad esempio driver seriale o stampanti.</span><span class="sxs-lookup"><span data-stu-id="e90e4-120">General kernel-mode drivers, such as serial or printer drivers.</span></span>
-   <span data-ttu-id="e90e4-121">Reindirizzamento del file System (questo è solo un caso speciale di un driver in modalità kernel generale).</span><span class="sxs-lookup"><span data-stu-id="e90e4-121">File system redirection (this is just a special case of a general kernel-mode driver).</span></span>
-   <span data-ttu-id="e90e4-122">Applicazioni in modalità utente, ad esempio Cut-and-paste remote.</span><span class="sxs-lookup"><span data-stu-id="e90e4-122">User mode applications, for example remote cut-and-paste.</span></span>
-   <span data-ttu-id="e90e4-123">Dispositivi audio.</span><span class="sxs-lookup"><span data-stu-id="e90e4-123">Audio devices.</span></span>

<span data-ttu-id="e90e4-124">Per ulteriori informazioni, vedere [utilizzo di Servizi Desktop remoto canali virtuali](using-terminal-services-virtual-channels.md).</span><span class="sxs-lookup"><span data-stu-id="e90e4-124">For more information, see [Using Remote Desktop Services Virtual Channels](using-terminal-services-virtual-channels.md).</span></span>

<span data-ttu-id="e90e4-125">Se è stata abilitata un'applicazione per i canali virtuali nella distribuzione di Servizi Desktop remoto, è possibile rendere disponibile l'applicazione ai computer client che accedono al server Host sessione Desktop remoto tramite il Desktop remoto controllo ActiveX Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e90e4-125">If you have enabled a virtual channels application in your Remote Desktop Services deployment, you can make the application available to client computers that access the RD Session Host server by means of the Remote Desktop Microsoft ActiveX control.</span></span> <span data-ttu-id="e90e4-126">Per altre informazioni, vedere [canali virtuali con script](scriptable-virtual-channels.md) e [uso del controllo ActiveX Desktop remoto con i canali virtuali](using-the-remote-desktop-activex-control-with-virtual-channels.md).</span><span class="sxs-lookup"><span data-stu-id="e90e4-126">For more information, see [Scriptable Virtual Channels](scriptable-virtual-channels.md) and [Using the Remote Desktop ActiveX Control with Virtual Channels](using-the-remote-desktop-activex-control-with-virtual-channels.md).</span></span>

 

 




