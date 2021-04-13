---
title: Gestione delle dimensioni dei pacchetti
description: Gestione delle dimensioni dei pacchetti
ms.assetid: 75ccda39-255a-4213-824e-1ca778a741dc
keywords:
- Windows Media Format SDK, gestione delle dimensioni dei pacchetti
- Windows Media Format SDK, dimensioni dei pacchetti
- profili, dimensioni dei pacchetti
- profili, gestione delle dimensioni dei pacchetti
- pacchetti, dimensioni
- pacchetti, interfaccia IWMPacketSize
- IWMPacketSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22e5bb0720d54338a754838e3d44c4479e55af9d
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104398761"
---
# <a name="managing-packet-size"></a><span data-ttu-id="2bdcb-110">Gestione delle dimensioni dei pacchetti</span><span class="sxs-lookup"><span data-stu-id="2bdcb-110">Managing Packet Size</span></span>

<span data-ttu-id="2bdcb-111">Il writer è progettato per gestire le dimensioni dei pacchetti internamente.</span><span class="sxs-lookup"><span data-stu-id="2bdcb-111">The writer is designed to manage the size of packets internally.</span></span> <span data-ttu-id="2bdcb-112">Tuttavia, potrebbero essere presenti requisiti specifici per l'applicazione che richiedono un controllo manuale sulle dimensioni dei pacchetti nei file ASF scritti.</span><span class="sxs-lookup"><span data-stu-id="2bdcb-112">However, you may have specific requirements for your application that call for some manual control over the size of packets in the ASF files that you write.</span></span> <span data-ttu-id="2bdcb-113">Windows Media Format SDK fornisce due interfacce, [**IWMPacketSize**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize) e [**IWMPacketSize2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2) , che consentono di controllare le dimensioni massime e minime dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="2bdcb-113">The Windows Media Format SDK provides two interfaces, [**IWMPacketSize**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize) and [**IWMPacketSize2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2) that enable you to control the maximum and minimum size of packets.</span></span>

<span data-ttu-id="2bdcb-114">Entrambe le interfacce delle dimensioni del pacchetto sono esposte nell'oggetto profilo.</span><span class="sxs-lookup"><span data-stu-id="2bdcb-114">Both packet size interfaces are exposed in the profile object.</span></span> <span data-ttu-id="2bdcb-115">Sono disponibili anche per l'oggetto Reader.</span><span class="sxs-lookup"><span data-stu-id="2bdcb-115">They are also available to the reader object.</span></span> <span data-ttu-id="2bdcb-116">Come per le altre interfacce correlate al profilo, il lettore può accedere solo ai metodi di lettura.</span><span class="sxs-lookup"><span data-stu-id="2bdcb-116">As with other profile-related interfaces, the reader can access only the reading methods.</span></span>

<span data-ttu-id="2bdcb-117">Le dimensioni dei pacchetti hanno un effetto sulle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="2bdcb-117">The size of packets has some effect on performance.</span></span> <span data-ttu-id="2bdcb-118">In generale, minore è la dimensione del pacchetto, più frammenti sono i dati all'interno di un file.</span><span class="sxs-lookup"><span data-stu-id="2bdcb-118">In general, the smaller the packet size, the more fragmented the data is within a file.</span></span> <span data-ttu-id="2bdcb-119">Maggiore è la frammentazione di un file, minore sarà il modo più efficiente per ricostruirlo.</span><span class="sxs-lookup"><span data-stu-id="2bdcb-119">The more fragmented a file is, the less efficient it will be to reconstruct it.</span></span> <span data-ttu-id="2bdcb-120">In uno scenario di streaming, questo potrebbe non essere una considerazione importante, perché il processo di lettura di un file da un'origine Internet è in genere inefficiente.</span><span class="sxs-lookup"><span data-stu-id="2bdcb-120">In a streaming scenario, this may not be an important consideration, as the process of reading a file from an Internet source is generally inefficient.</span></span> <span data-ttu-id="2bdcb-121">Quando si tratta di un file localmente, questo potrebbe essere una considerazione.</span><span class="sxs-lookup"><span data-stu-id="2bdcb-121">When dealing with a file locally however, this might be a consideration.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2bdcb-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2bdcb-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2bdcb-123">**Interfaccia IWMPacketSize**</span><span class="sxs-lookup"><span data-stu-id="2bdcb-123">**IWMPacketSize Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize)
</dt> <dt>

[<span data-ttu-id="2bdcb-124">**Interfaccia IWMPacketSize2**</span><span class="sxs-lookup"><span data-stu-id="2bdcb-124">**IWMPacketSize2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2)
</dt> <dt>

[<span data-ttu-id="2bdcb-125">**Utilizzo dei profili**</span><span class="sxs-lookup"><span data-stu-id="2bdcb-125">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> </dl>

 

 




