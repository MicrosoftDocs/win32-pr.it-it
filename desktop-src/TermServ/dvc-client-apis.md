---
title: API client DVC
description: Le API client dinamiche del canale virtuale (DVC) sono implementate in modo specifico per il client Connessione Desktop remoto (RDC) della connessione.
ms.assetid: 976a6cc2-7bbe-4ecc-91b4-b7c659eca5ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25c29d360fb0ad4d6e31e828f9c62f42f64fb311
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329484"
---
# <a name="dvc-client-apis"></a><span data-ttu-id="e961d-103">API client DVC</span><span class="sxs-lookup"><span data-stu-id="e961d-103">DVC Client APIs</span></span>

<span data-ttu-id="e961d-104">Le API client dinamiche del canale virtuale (DVC) sono implementate in modo specifico per il client Connessione Desktop remoto (RDC) della connessione.</span><span class="sxs-lookup"><span data-stu-id="e961d-104">The dynamic virtual channel (DVC) client APIs are implemented specifically for the Remote Desktop Connection (RDC) client of the connection.</span></span> <span data-ttu-id="e961d-105">Alcune API sono implementate dal Framework DVC e alcune sono implementate dallo sviluppatore di plug-in.</span><span class="sxs-lookup"><span data-stu-id="e961d-105">Some of the APIs are implemented by the DVC framework, and some are implemented by the plug-in developer.</span></span> <span data-ttu-id="e961d-106">Alcune API vengono utilizzate per supportare il plug-in client di Connessione Desktop remoto (RDC) e non sono direttamente correlate al trasporto dati.</span><span class="sxs-lookup"><span data-stu-id="e961d-106">Some of the APIs are used to support the Remote Desktop Connection (RDC) client plug-in, and are not directly related to data transport.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e961d-107">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="e961d-107">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="e961d-108">**IWTSPlugin**</span><span class="sxs-lookup"><span data-stu-id="e961d-108">**IWTSPlugin**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin)
</dt> <dd>

<span data-ttu-id="e961d-109">Consente il caricamento del plug-in del client Connessione Desktop remoto (RDC) dal client di Connessione Desktop remoto (RDC).</span><span class="sxs-lookup"><span data-stu-id="e961d-109">Allows for the Remote Desktop Connection (RDC) client plug-in to be loaded by the Remote Desktop Connection (RDC) client.</span></span>

</dd> <dt>

[<span data-ttu-id="e961d-110">**IWTSListener**</span><span class="sxs-lookup"><span data-stu-id="e961d-110">**IWTSListener**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener)
</dt> <dd>

<span data-ttu-id="e961d-111">Gestisce le impostazioni di configurazione per ogni listener per la connessione del canale virtuale dinamico (DVC).</span><span class="sxs-lookup"><span data-stu-id="e961d-111">Manages configuration settings for each listener for the dynamic virtual channel (DVC) connection.</span></span>

</dd> <dt>

[<span data-ttu-id="e961d-112">**IWTSListenerCallback**</span><span class="sxs-lookup"><span data-stu-id="e961d-112">**IWTSListenerCallback**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)
</dt> <dd>

<span data-ttu-id="e961d-113">Utilizzato per notificare al plug-in del client Connessione Desktop remoto (RDC) informazioni sulle richieste in ingresso su un listener specifico.</span><span class="sxs-lookup"><span data-stu-id="e961d-113">Used to notify the Remote Desktop Connection (RDC) client plug-in about incoming requests on a particular listener.</span></span>

</dd> <dt>

[<span data-ttu-id="e961d-114">**IWTSVirtualChannelManager**</span><span class="sxs-lookup"><span data-stu-id="e961d-114">**IWTSVirtualChannelManager**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager)
</dt> <dd>

<span data-ttu-id="e961d-115">Gestisce tutti i plug-in del client Connessione Desktop remoto (RDC) e i listener del canale virtuale dinamico (DVC).</span><span class="sxs-lookup"><span data-stu-id="e961d-115">Manages all Remote Desktop Connection (RDC) client plug-ins and dynamic virtual channel (DVC) listeners.</span></span>

</dd> <dt>

[<span data-ttu-id="e961d-116">**IWTSVirtualChannel**</span><span class="sxs-lookup"><span data-stu-id="e961d-116">**IWTSVirtualChannel**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)
</dt> <dd>

<span data-ttu-id="e961d-117">Utilizzato per controllare lo stato del canale e scrivere sul canale.</span><span class="sxs-lookup"><span data-stu-id="e961d-117">Used to control the channel state, and writes on the channel.</span></span>

</dd> <dt>

[<span data-ttu-id="e961d-118">**IWTSVirtualChannelCallback**</span><span class="sxs-lookup"><span data-stu-id="e961d-118">**IWTSVirtualChannelCallback**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback)
</dt> <dd>

<span data-ttu-id="e961d-119">Riceve le notifiche relative alle modifiche dello stato del canale o ai dati ricevuti.</span><span class="sxs-lookup"><span data-stu-id="e961d-119">Receives notifications about channel state changes or data received.</span></span>

</dd> <dt>

[<span data-ttu-id="e961d-120">**IWTSVirtualChannelCallback2**</span><span class="sxs-lookup"><span data-stu-id="e961d-120">**IWTSVirtualChannelCallback2**</span></span>](iwtsvirtualchannelcallback2.md)
</dt> <dd>

<span data-ttu-id="e961d-121">Questa interfaccia non è supportata.</span><span class="sxs-lookup"><span data-stu-id="e961d-121">This interface is not supported.</span></span>

</dd> <dt>

[<span data-ttu-id="e961d-122">**VirtualChannelGetInstance**</span><span class="sxs-lookup"><span data-stu-id="e961d-122">**VirtualChannelGetInstance**</span></span>](virtualchannelgetinstance.md)
</dt> <dd>

<span data-ttu-id="e961d-123">Chiamato per fare in modo che il plug-in crei un'istanza dell'interfaccia [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) per tutti i plug-in implementati dalla dll.</span><span class="sxs-lookup"><span data-stu-id="e961d-123">Called to have the plug-in create an instance of the [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) interface for all plug-ins implemented by the DLL.</span></span>

</dd> </dl>

 

 




