---
title: Scrittura di dati tramite un canale DVC
description: La scrittura di dati del canale tramite un canale virtuale dinamico (DVC) è simmetrica sia per il server host sessione Desktop remoto (host sessione Desktop remoto) che per il client.
ms.assetid: 33bacbf0-c558-497a-a08a-95eb398fad97
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd6f26e926958ceba5418a72849b75a66b11d2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298413"
---
# <a name="writing-data-by-using-a-dvc-channel"></a><span data-ttu-id="8fda9-103">Scrittura di dati tramite un canale DVC</span><span class="sxs-lookup"><span data-stu-id="8fda9-103">Writing Data by Using a DVC Channel</span></span>

<span data-ttu-id="8fda9-104">La scrittura di dati del canale tramite un canale virtuale dinamico (DVC) è simmetrica sia per il server host sessione Desktop remoto (host sessione Desktop remoto) che per il client.</span><span class="sxs-lookup"><span data-stu-id="8fda9-104">Writing channel data by using a dynamic virtual channel (DVC) is symmetric for both the Remote Desktop Session Host (RD Session Host) server and the client.</span></span> <span data-ttu-id="8fda9-105">La scrittura dei dati del canale viene implementata dal metodo [**Write**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannel-write) dell'interfaccia [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel) .</span><span class="sxs-lookup"><span data-stu-id="8fda9-105">The writing of channel data is implemented by the [**Write**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannel-write) method of the [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel) interface.</span></span>

<span data-ttu-id="8fda9-106">La figura seguente mostra l'invio e la ricezione del pacchetto di dati tra il client e il server DVC (plug-in DVC).</span><span class="sxs-lookup"><span data-stu-id="8fda9-106">The following illustration shows the sending and receiving of the data packet between the DVC client and server (DVC plug-in).</span></span>

![invio e ricezione di un pacchetto di dati tra il client e il server DVC](images/writedvcchannel.png)

 

 




