---
title: Avvio di un listener DVC
description: Per stabilire una connessione corretta tra due moduli DVC (Dynamic Virtual Channel) in esecuzione nel client e nel server Connessione Desktop remoto (RDC), è necessario che un listener DVC sia in esecuzione e in stato di ascolto.
ms.assetid: c9130375-eb60-4996-84f5-a1081144e130
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b625d5547facd0487af170af9d59eddd6bfed87
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332388"
---
# <a name="starting-a-dvc-listener"></a><span data-ttu-id="58167-103">Avvio di un listener DVC</span><span class="sxs-lookup"><span data-stu-id="58167-103">Starting a DVC Listener</span></span>

<span data-ttu-id="58167-104">Per stabilire una connessione corretta tra due moduli DVC (Dynamic Virtual Channel) in esecuzione nel client e nel server Connessione Desktop remoto (RDC), è necessario che un listener DVC sia in esecuzione e in stato di ascolto.</span><span class="sxs-lookup"><span data-stu-id="58167-104">To establish a successful connection between two dynamic virtual channel (DVC) modules that are running on the Remote Desktop Connection (RDC) client and server, a DVC listener must be running and in a listening state.</span></span>

<span data-ttu-id="58167-105">La creazione di istanze di un listener si verifica in genere nel metodo [**Initialize**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-initialize) del plug-in DVC.</span><span class="sxs-lookup"><span data-stu-id="58167-105">The instantiation of a listener typically occurs in the [**Initialize**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-initialize) method of the DVC plug-in.</span></span> <span data-ttu-id="58167-106">Tuttavia, la creazione di istanze non è limitata al metodo **Initialize** e può essere avviata in qualsiasi punto dell'esecuzione del plug-in.</span><span class="sxs-lookup"><span data-stu-id="58167-106">However, instantiation is not limited to the **Initialize** method, and can be started at any point of the plug-in execution.</span></span> <span data-ttu-id="58167-107">Il listener viene descritto dall'interfaccia [**IWTSListener**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener) di cui viene creata un'istanza da [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager).</span><span class="sxs-lookup"><span data-stu-id="58167-107">The listener is described by the [**IWTSListener**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener) interface which is instantiated by the [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager).</span></span> <span data-ttu-id="58167-108">Un'istanza di al gestore del canale viene passata al plug-in nel punto di inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="58167-108">An instance to the channel manager is passed to the plug-in at the initialization point.</span></span> <span data-ttu-id="58167-109">Il plug-in è in grado di mantenere un riferimento interno all'istanza a condizione che sia necessario.</span><span class="sxs-lookup"><span data-stu-id="58167-109">The plug-in can maintain an internal reference to the instance as long as it needs to.</span></span>

<span data-ttu-id="58167-110">Un plug-in può creare un'istanza di un numero di listener sufficiente.</span><span class="sxs-lookup"><span data-stu-id="58167-110">A plug-in can instantiate as many listeners as it needs to.</span></span> <span data-ttu-id="58167-111">Tutte le connessioni in ingresso verranno gestite da [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback), fornito nel metodo [**CreateListener**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannelmanager-createlistener) di [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager).</span><span class="sxs-lookup"><span data-stu-id="58167-111">Any incoming connection will be handled by [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback), which is supplied in the [**CreateListener**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannelmanager-createlistener) method of [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager).</span></span> <span data-ttu-id="58167-112">Per un esempio, vedere l'implementazione di **CDVCSamplePlugin:: Initialize** nell'esempio di codice del [plug-in del client DVC](dvc-client-plug-in-example.md) .</span><span class="sxs-lookup"><span data-stu-id="58167-112">For an example, see the implementation of **CDVCSamplePlugin::Initialize** in the [DVC Client Plug-in Example](dvc-client-plug-in-example.md) sample code.</span></span>

 

 




