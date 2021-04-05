---
title: Applicazione Virtual Channel Server
description: Il modulo server di un'applicazione che usa canali virtuali deve essere un'applicazione in modalità utente in esecuzione in una sessione client nel server host sessione Desktop remoto (host sessione Desktop remoto). Si noti che è necessario fornire un metodo per avviare l'applicazione server.
ms.assetid: b593df5d-5e22-46c6-8f59-9e3fdfe765ad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 377732b91d6f93645e23b0f0b93cc203a65ef471
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711413"
---
# <a name="virtual-channel-server-application"></a><span data-ttu-id="c09d8-104">Applicazione Virtual Channel Server</span><span class="sxs-lookup"><span data-stu-id="c09d8-104">Virtual Channel Server Application</span></span>

<span data-ttu-id="c09d8-105">Il modulo server di un'applicazione che usa canali virtuali deve essere un'applicazione in modalità utente in esecuzione in una sessione client nel server host sessione Desktop remoto (host sessione Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="c09d8-105">The server module of an application that uses virtual channels must be a user-mode application running in a client session on the Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="c09d8-106">Si noti che è necessario fornire un metodo per avviare l'applicazione server.</span><span class="sxs-lookup"><span data-stu-id="c09d8-106">Note that you must provide a method to start the server application.</span></span> <span data-ttu-id="c09d8-107">Questa operazione può essere eseguita in diversi modi. ad esempio, è possibile usare uno script di accesso o un programma o uno script nella cartella di avvio.</span><span class="sxs-lookup"><span data-stu-id="c09d8-107">You can accomplish this in multiple ways; for example, you can use a logon script, or a program or script in the Startup folder.</span></span> <span data-ttu-id="c09d8-108">Gli utenti possono anche avviare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c09d8-108">Users could also launch the application.</span></span>

<span data-ttu-id="c09d8-109">È necessario archiviare il nome dell'applicazione Virtual Channel Server nel registro di sistema aggiungendo una sottochiave nel percorso seguente:</span><span class="sxs-lookup"><span data-stu-id="c09d8-109">You must store the name of the virtual channel server application in the registry by adding a subkey under the following location:</span></span>

<span data-ttu-id="c09d8-110">**HKEY \_ \_** \\  \\  \\  \\ **Terminal Server** \\ **componenti aggiuntivi** del controllo CurrentControlSet di sistema del computer locale</span><span class="sxs-lookup"><span data-stu-id="c09d8-110">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**Terminal Server**\\**Addins**</span></span>

<span data-ttu-id="c09d8-111">Per ulteriori informazioni sulla sottochiave, vedere [monitoraggio delle connessioni di sessione e disconnessione](monitoring-session-connections-and-disconnections.md).</span><span class="sxs-lookup"><span data-stu-id="c09d8-111">For more information about the subkey, see [Monitoring Session Connections and Disconnections](monitoring-session-connections-and-disconnections.md).</span></span>

<span data-ttu-id="c09d8-112">L'applicazione server può chiamare la funzione [**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen) per aprire un handle per un canale virtuale.</span><span class="sxs-lookup"><span data-stu-id="c09d8-112">The server application can call the [**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen) function to open a handle to a virtual channel.</span></span> <span data-ttu-id="c09d8-113">L'applicazione può quindi usare l'handle in una delle funzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="c09d8-113">The application can then use the handle in any of the following functions.</span></span>

<dl> <dt>

[<span data-ttu-id="c09d8-114">**WTSVirtualChannelClose**</span><span class="sxs-lookup"><span data-stu-id="c09d8-114">**WTSVirtualChannelClose**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelclose)
</dt> <dd>

<span data-ttu-id="c09d8-115">Chiude un handle di canale virtuale aperto.</span><span class="sxs-lookup"><span data-stu-id="c09d8-115">Closes an open virtual channel handle.</span></span>

</dd> <dt>

[<span data-ttu-id="c09d8-116">**WTSVirtualChannelPurgeInput**</span><span class="sxs-lookup"><span data-stu-id="c09d8-116">**WTSVirtualChannelPurgeInput**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeinput)
</dt> <dd>

<span data-ttu-id="c09d8-117">Elimina tutti i dati di input in coda inviati dal client al server su un canale virtuale specifico.</span><span class="sxs-lookup"><span data-stu-id="c09d8-117">Deletes all queued input data sent from the client to the server on a specific virtual channel.</span></span>

> [!Note]  
> <span data-ttu-id="c09d8-118">Questa funzione attualmente non viene utilizzata da Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="c09d8-118">This function currently is not used by Remote Desktop Services.</span></span>

 

</dd> <dt>

[<span data-ttu-id="c09d8-119">**WTSVirtualChannelPurgeOutput**</span><span class="sxs-lookup"><span data-stu-id="c09d8-119">**WTSVirtualChannelPurgeOutput**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeoutput)
</dt> <dd>

<span data-ttu-id="c09d8-120">Elimina tutti i dati di output in coda inviati dal server al client su un canale virtuale specifico.</span><span class="sxs-lookup"><span data-stu-id="c09d8-120">Deletes all queued output data sent from the server to the client on a specific virtual channel.</span></span>

> [!Note]  
> <span data-ttu-id="c09d8-121">Questa funzione attualmente non viene utilizzata da Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="c09d8-121">This function currently is not used by Remote Desktop Services.</span></span>

 

</dd> <dt>

[<span data-ttu-id="c09d8-122">**WTSVirtualChannelQuery**</span><span class="sxs-lookup"><span data-stu-id="c09d8-122">**WTSVirtualChannelQuery**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery)
</dt> <dd>

<span data-ttu-id="c09d8-123">Restituisce informazioni su un canale virtuale specificato.</span><span class="sxs-lookup"><span data-stu-id="c09d8-123">Returns information about a specified virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="c09d8-124">**WTSVirtualChannelRead**</span><span class="sxs-lookup"><span data-stu-id="c09d8-124">**WTSVirtualChannelRead**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread)
</dt> <dd>

<span data-ttu-id="c09d8-125">Legge i dati dall'estremità server di un canale virtuale.</span><span class="sxs-lookup"><span data-stu-id="c09d8-125">Reads data from the server end of a virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="c09d8-126">**WTSVirtualChannelWrite**</span><span class="sxs-lookup"><span data-stu-id="c09d8-126">**WTSVirtualChannelWrite**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelwrite)
</dt> <dd>

<span data-ttu-id="c09d8-127">Scrive i dati nell'entità finale del server di un canale virtuale.</span><span class="sxs-lookup"><span data-stu-id="c09d8-127">Writes data to the server end of a virtual channel.</span></span>

</dd> </dl>

 

 




