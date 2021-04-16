---
title: Accettazione di una connessione (Servizi Desktop remoto)
description: A un certo punto nel tempo, il client dinamico del canale virtuale (DVC) richiederà una connessione al listener di DVC.
ms.assetid: eab17aa9-590c-4da2-a1a9-6e50a11d1de7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b13aa0b78e459c85e7ba07e043e3da313b3f6118
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104567730"
---
# <a name="accepting-a-connection-remote-desktop-services"></a><span data-ttu-id="0f389-103">Accettazione di una connessione (Servizi Desktop remoto)</span><span class="sxs-lookup"><span data-stu-id="0f389-103">Accepting a Connection (Remote Desktop Services)</span></span>

<span data-ttu-id="0f389-104">A un certo punto nel tempo, il client dinamico del canale virtuale (DVC) richiederà una connessione al listener di DVC.</span><span class="sxs-lookup"><span data-stu-id="0f389-104">At some point in time, the dynamic virtual channel (DVC) client will request a connection to the DVC listener.</span></span> <span data-ttu-id="0f389-105">Quando si verifica questo problema, il listener può generare un canale di comunicazione univoco per il client, gestito dal metodo [**OnNewChannelConnection**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtslistenercallback-onnewchannelconnection) di [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback).</span><span class="sxs-lookup"><span data-stu-id="0f389-105">When this occurs, the listener can spawn a unique communication channel to the client, which is handled by the [**OnNewChannelConnection**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtslistenercallback-onnewchannelconnection) method of [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback).</span></span> <span data-ttu-id="0f389-106">Per un esempio, vedere l'implementazione di **CDVCSamplePlugin:: OnNewChannelConnection** nel codice di esempio relativo al [plug-in del client DVC](dvc-client-plug-in-example.md) .</span><span class="sxs-lookup"><span data-stu-id="0f389-106">For an example, see the implementation of **CDVCSamplePlugin::OnNewChannelConnection** in the [DVC Client Plug-in Example](dvc-client-plug-in-example.md) sample code.</span></span>

<span data-ttu-id="0f389-107">Nella figura seguente viene illustrata la sequenza di eventi per stabilire una connessione DVC.</span><span class="sxs-lookup"><span data-stu-id="0f389-107">The following figure shows the sequence of events for establishing a DVC connection.</span></span> <span data-ttu-id="0f389-108">Gli oggetti ombreggiati sono forniti dall'utente (applicazione/servizio DVC e [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)), mentre gli oggetti non ombreggiati fanno parte di framework (host sessione Desktop remoto servizio host sessione Desktop remoto, listener e [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)).</span><span class="sxs-lookup"><span data-stu-id="0f389-108">The shaded objects are user-supplied (DVC application/service and [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)), while the un-shaded objects are part of the framework (Remote Desktop Session Host (RD Session Host) service, listener, and [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)).</span></span>

![sequenza di eventi per stabilire una connessione DVC](images/acceptingconnection.png)

> [!Note]  
> <span data-ttu-id="0f389-110">In questa figura si presuppone che sia stato creato un oggetto listener tramite una chiamata [**CreateListener**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannelmanager-createlistener) a [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager)e che il plug-in abbia specificato [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback) come parametro.</span><span class="sxs-lookup"><span data-stu-id="0f389-110">This figure assumes that a listener object has been created through a [**CreateListener**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannelmanager-createlistener) call to [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager), and that the plug-in has specified [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback) as a parameter.</span></span>

 

 

 




