---
title: Implementazione di canali virtuali tramite script tramite Connessione Web Desktop remoto
description: Esempi di codice che illustrano i passaggi per l'implementazione di canali virtuali utilizzabili tramite script con Connessione Web Desktop remoto.
ms.assetid: a482b84d-96b6-4f42-8841-7039a1882789
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89a36f685de01312a93df67deb6be16ce031794c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712217"
---
# <a name="implementing-scriptable-virtual-channels-by-using-remote-desktop-web-connection"></a><span data-ttu-id="8b3e6-103">Implementazione di canali virtuali tramite script tramite Connessione Web Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="8b3e6-103">Implementing scriptable virtual channels by using Remote Desktop Web Connection</span></span>

<span data-ttu-id="8b3e6-104">Nella procedura e negli esempi di codice riportati di seguito vengono illustrati i passaggi per l'implementazione di canali virtuali tramite script con Connessione Web Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="8b3e6-104">The following procedure and code examples show the steps for implementing scriptable virtual channels with Remote Desktop Web Connection.</span></span> <span data-ttu-id="8b3e6-105">Gli esempi sono stati scritti in Visual Basic Scripting Edition e presuppongono che il controllo ActiveX Desktop remoto sia denominato "MsRdpClient".</span><span class="sxs-lookup"><span data-stu-id="8b3e6-105">The examples were written in Visual Basic Scripting Edition and assume that the Remote Desktop ActiveX control is named "MsRdpClient".</span></span>

<span data-ttu-id="8b3e6-106">**Per creare e distribuire canali virtuali tramite script**</span><span class="sxs-lookup"><span data-stu-id="8b3e6-106">**To create and deploy scriptable virtual channels**</span></span>

1.  <span data-ttu-id="8b3e6-107">Distribuire il lato server dell'applicazione e assicurarsi che sia in esecuzione nel server host sessione Desktop remoto (host sessione Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="8b3e6-107">Deploy the server side of the application and make sure it is running on the Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="8b3e6-108">Per informazioni sulla distribuzione di applicazioni di canali virtuali sul server, vedere [Virtual Channel Server Application](virtual-channel-server-application.md).</span><span class="sxs-lookup"><span data-stu-id="8b3e6-108">For information about deploying virtual channels applications on the server, see [Virtual Channel Server Application](virtual-channel-server-application.md).</span></span>
2.  <span data-ttu-id="8b3e6-109">Nello script client, chiamare [**IMsTscAx:: CreateVirtualChannels**](imstscax-createvirtualchannels.md), passando una stringa che contiene un elenco delimitato da virgole di nomi di canale virtuali.</span><span class="sxs-lookup"><span data-stu-id="8b3e6-109">In your client script, call [**IMsTscAx::CreateVirtualChannels**](imstscax-createvirtualchannels.md), passing a string that contains a comma-separated list of virtual channel names.</span></span>

    ```VB
    MsRdpClient.CreateVirtualChannels("mychan1,mychan2")
    ```

    

    <span data-ttu-id="8b3e6-110">Per informazioni sulle restrizioni di denominazione dei canali virtuali, vedere [registrazione client del canale virtuale](virtual-channel-client-registration.md).</span><span class="sxs-lookup"><span data-stu-id="8b3e6-110">For information about virtual channel naming restrictions, see [Virtual Channel Client Registration](virtual-channel-client-registration.md).</span></span>

3.  <span data-ttu-id="8b3e6-111">Chiamare [**IMsTscAx:: Connect**](imstscax-connect.md) per creare la connessione Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="8b3e6-111">Call [**IMsTscAx::Connect**](imstscax-connect.md) to create your Remote Desktop Services connection.</span></span>

    ```VB
    MsRdpClient.connect
    ```

    

4.  <span data-ttu-id="8b3e6-112">Usare il metodo [**IMsTscAx:: SendOnVirtualChannel**](imstscax-sendonvirtualchannel.md) per inviare dati al server, passando una stringa che contiene il nome del canale virtuale e una seconda stringa che contiene i dati da passare.</span><span class="sxs-lookup"><span data-stu-id="8b3e6-112">Use the [**IMsTscAx::SendOnVirtualChannel**](imstscax-sendonvirtualchannel.md) method to send data to the server, passing a string that contains the virtual channel name and a second string that contains the data to be passed.</span></span>

    ```VB
    MsRdpClient.SendOnVirtualChannel("mychan1","hello from the client")
    ```

    

5.  <span data-ttu-id="8b3e6-113">Ricevere i dati dal server nell'evento [**IMsTscAxEvents:: OnChannelReceivedData**](imstscaxevents-onchannelreceiveddata.md) .</span><span class="sxs-lookup"><span data-stu-id="8b3e6-113">Receive data from the server on the [**IMsTscAxEvents::OnChannelReceivedData**](imstscaxevents-onchannelreceiveddata.md) event.</span></span>

    ```VB
    Sub MsRdpClient.OnChannelReceivedData(chanName,data)
    Msgbox("received data:" &data& "on virtual channel:" &chanName)
    End sub
    ```

    

 

 




