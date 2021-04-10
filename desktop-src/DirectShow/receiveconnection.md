---
description: ReceiveConnection
ms.assetid: 90a6a09a-95e1-4adf-8e0b-269f971aaa67
title: ReceiveConnection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80fd9fe31f87a34dc3bfdfc4ecfb532255138b9c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124671"
---
# <a name="receiveconnection"></a><span data-ttu-id="41157-103">ReceiveConnection</span><span class="sxs-lookup"><span data-stu-id="41157-103">ReceiveConnection</span></span>

<span data-ttu-id="41157-104">Questo meccanismo consente a un pin di output di proporre una modifica di formato al peer downstream, quando il nuovo formato richiede un buffer più grande.</span><span class="sxs-lookup"><span data-stu-id="41157-104">This mechanism enables an output pin to propose a format change to its downstream peer, when the new format requires a larger buffer.</span></span> <span data-ttu-id="41157-105">Il pin di output esegue le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="41157-105">The output pin does the following:</span></span>

1.  <span data-ttu-id="41157-106">Chiama [**Ipin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) sul pin di input downstream.</span><span class="sxs-lookup"><span data-stu-id="41157-106">Calls [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) on the downstream input pin.</span></span>
2.  <span data-ttu-id="41157-107">Se ha `ReceiveConnection` esito positivo, chiama [**IMemInputPin:: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) sul pin di input.</span><span class="sxs-lookup"><span data-stu-id="41157-107">If `ReceiveConnection` succeeds, calls [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) on the input pin.</span></span>

<span data-ttu-id="41157-108">Inoltre, per modificare le dimensioni del buffer, potrebbe essere necessario chiamare [**IMemAllocator:: seproperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) , quindi eseguire il commit e il commit dell'allocatore.</span><span class="sxs-lookup"><span data-stu-id="41157-108">In addition, the output pin may need to call [**IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) and then decommit and recommit the allocator in order to change buffer sizes.</span></span> <span data-ttu-id="41157-109">Assicurarsi di recapitare tutti gli esempi in sospeso nel formato precedente prima di modificare le dimensioni del buffer.</span><span class="sxs-lookup"><span data-stu-id="41157-109">Make sure to deliver all pending samples in the old format before changing the buffer size.</span></span>

<span data-ttu-id="41157-110">Alcuni decodificatori MPEG-2 usano questo meccanismo per passare tra l'output MPEG-1 e MPEG-2 o se le dimensioni del video cambiano.</span><span class="sxs-lookup"><span data-stu-id="41157-110">Some MPEG-2 decoders use this mechanism to switch between MPEG-1 and MPEG-2 output or if the video size changes.</span></span>

 

 



