---
title: Canale virtuale persistente del controllo remoto
description: Un canale virtuale persistente del controllo remoto non viene chiuso quando un controllo remoto si connette o si disconnette per la sessione connessa al client. I dati continueranno a essere trasmessi e ricevuti tramite questo canale.
ms.assetid: 0c3d5429-250e-4272-8cdd-69097acfaff4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d87054a79863df5816b30fced648ab40251a80e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396754"
---
# <a name="remote-control-persistent-virtual-channels"></a><span data-ttu-id="f0c4b-104">Canale virtuale persistente del controllo remoto</span><span class="sxs-lookup"><span data-stu-id="f0c4b-104">Remote Control Persistent Virtual Channels</span></span>

<span data-ttu-id="f0c4b-105">In Windows XP, una DLL può specificare uno o più canali virtuali come *controllo remoto persistente*.</span><span class="sxs-lookup"><span data-stu-id="f0c4b-105">On Windows XP, a DLL can specify one or more virtual channels as *remote control persistent*.</span></span> <span data-ttu-id="f0c4b-106">Un canale virtuale persistente del controllo remoto non viene chiuso quando un controllo remoto si connette o si disconnette per la sessione connessa al client.</span><span class="sxs-lookup"><span data-stu-id="f0c4b-106">A remote control persistent virtual channel is not closed when a remote control connects or disconnects for the session connected to the client.</span></span> <span data-ttu-id="f0c4b-107">I dati continueranno a essere trasmessi e ricevuti tramite questo canale.</span><span class="sxs-lookup"><span data-stu-id="f0c4b-107">Data will continue to be transmitted and received through this channel.</span></span> <span data-ttu-id="f0c4b-108">In questo scenario, i canali virtuali che la DLL non specifica come controllo remoto persistente si chiuderà.</span><span class="sxs-lookup"><span data-stu-id="f0c4b-108">Virtual channels that the DLL does not specify as remote control persistent will close in this scenario.</span></span>

<span data-ttu-id="f0c4b-109">I canali virtuali permanenti di controllo remoto vengono specificati durante la chiamata a **VirtualChannelInit**.</span><span class="sxs-lookup"><span data-stu-id="f0c4b-109">Remote control persistent virtual channels are specified during the call to **VirtualChannelInit**.</span></span> <span data-ttu-id="f0c4b-110">Per informazioni specifiche su questa pagina, vedere la pagina di riferimento per [**VirtualChannelInit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit) .</span><span class="sxs-lookup"><span data-stu-id="f0c4b-110">Refer to the reference page for [**VirtualChannelInit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit) for specific information about this.</span></span>

 

 




