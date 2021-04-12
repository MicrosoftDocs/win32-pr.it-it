---
title: Oggetto di rete
description: L'oggetto di rete fornisce le proprietà e i metodi usati per accedere alle statistiche relative alla qualità di una connessione di rete e per specificare e recuperare le impostazioni del proxy di rete.
ms.assetid: 5ae6137e-22f5-4a65-8793-b6f66adb4cba
keywords:
- Windows oggetto di rete Media Player
topic_type:
- apiref
api_name:
- Network Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d439679636bce773c43f5610060c4744ef4d5d7c
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/06/2019
ms.locfileid: "104398076"
---
# <a name="network-object"></a><span data-ttu-id="0e64c-104">Oggetto di rete</span><span class="sxs-lookup"><span data-stu-id="0e64c-104">Network Object</span></span>

<span data-ttu-id="0e64c-105">L'oggetto di **rete** fornisce le proprietà e i metodi usati per accedere alle statistiche relative alla qualità di una connessione di rete e per specificare e recuperare le impostazioni del proxy di rete.</span><span class="sxs-lookup"><span data-stu-id="0e64c-105">The **Network** object provides properties and methods used to access statistics relating to the quality of a network connection, and to specify and retrieve the network proxy settings.</span></span>

<span data-ttu-id="0e64c-106">L'oggetto di **rete** supporta le seguenti proprietà.</span><span class="sxs-lookup"><span data-stu-id="0e64c-106">The **Network** object supports the following properties.</span></span>



| <span data-ttu-id="0e64c-107">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0e64c-107">Property</span></span>                                           | <span data-ttu-id="0e64c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0e64c-108">Description</span></span>                                                                                 |
|----------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0e64c-109">Banda</span><span class="sxs-lookup"><span data-stu-id="0e64c-109">bandWidth</span></span>](network-bandwidth.md)                 | <span data-ttu-id="0e64c-110">Recupera la larghezza di banda corrente dell'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="0e64c-110">Retrieves the current bandwidth of the media item.</span></span>                                          |
| [<span data-ttu-id="0e64c-111">Velocità in bit</span><span class="sxs-lookup"><span data-stu-id="0e64c-111">bitRate</span></span>](network-bitrate.md)                     | <span data-ttu-id="0e64c-112">Recupera la velocità in bit corrente ricevuta.</span><span class="sxs-lookup"><span data-stu-id="0e64c-112">Retrieves the current bit rate being received.</span></span>                                              |
| [<span data-ttu-id="0e64c-113">bufferingCount</span><span class="sxs-lookup"><span data-stu-id="0e64c-113">bufferingCount</span></span>](network-bufferingcount.md)       | <span data-ttu-id="0e64c-114">Recupera il numero di volte in cui si è verificato il buffer durante la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="0e64c-114">Retrieves the number of times buffering occurred during playback.</span></span>                           |
| [<span data-ttu-id="0e64c-115">bufferingProgress</span><span class="sxs-lookup"><span data-stu-id="0e64c-115">bufferingProgress</span></span>](network-bufferingprogress.md) | <span data-ttu-id="0e64c-116">Recupera la percentuale di memorizzazione nel buffer completata.</span><span class="sxs-lookup"><span data-stu-id="0e64c-116">Retrieves the percentage of buffering completed.</span></span>                                            |
| [<span data-ttu-id="0e64c-117">bufferingTime</span><span class="sxs-lookup"><span data-stu-id="0e64c-117">bufferingTime</span></span>](network-bufferingtime.md)         | <span data-ttu-id="0e64c-118">Specifica o recupera la quantità di tempo di memorizzazione nel buffer in millisecondi prima che inizi la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="0e64c-118">Specifies or retrieves the amount of buffering time in milliseconds before playback begins.</span></span> |
| [<span data-ttu-id="0e64c-119">downloadProgress</span><span class="sxs-lookup"><span data-stu-id="0e64c-119">downloadProgress</span></span>](network-downloadprogress.md)   | <span data-ttu-id="0e64c-120">Recupera la percentuale di download completato.</span><span class="sxs-lookup"><span data-stu-id="0e64c-120">Retrieves the percentage of download completed.</span></span>                                             |
| [<span data-ttu-id="0e64c-121">encodedFrameRate</span><span class="sxs-lookup"><span data-stu-id="0e64c-121">encodedFrameRate</span></span>](network-encodedframerate.md)   | <span data-ttu-id="0e64c-122">Recupera la frequenza dei fotogrammi video specificata dall'autore del contenuto.</span><span class="sxs-lookup"><span data-stu-id="0e64c-122">Retrieves the video frame rate specified by the content author.</span></span>                             |
| [<span data-ttu-id="0e64c-123">frameRate</span><span class="sxs-lookup"><span data-stu-id="0e64c-123">frameRate</span></span>](network-framerate.md)                 | <span data-ttu-id="0e64c-124">Recupera la frequenza dei fotogrammi video corrente.</span><span class="sxs-lookup"><span data-stu-id="0e64c-124">Retrieves the current video frame rate.</span></span>                                                     |
| [<span data-ttu-id="0e64c-125">framesSkipped</span><span class="sxs-lookup"><span data-stu-id="0e64c-125">framesSkipped</span></span>](network-framesskipped.md)         | <span data-ttu-id="0e64c-126">Recupera il numero totale di frame ignorati durante la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="0e64c-126">Retrieves the total number of frames skipped during playback.</span></span>                               |
| [<span data-ttu-id="0e64c-127">lostPackets</span><span class="sxs-lookup"><span data-stu-id="0e64c-127">lostPackets</span></span>](network-lostpackets.md)             | <span data-ttu-id="0e64c-128">Recupera il numero di pacchetti persi.</span><span class="sxs-lookup"><span data-stu-id="0e64c-128">Retrieves the number of packets lost.</span></span>                                                       |
| [<span data-ttu-id="0e64c-129">maxBandwidth</span><span class="sxs-lookup"><span data-stu-id="0e64c-129">maxBandwidth</span></span>](network-maxbandwidth.md)           | <span data-ttu-id="0e64c-130">Specifica o recupera la larghezza di banda massima consentita.</span><span class="sxs-lookup"><span data-stu-id="0e64c-130">Specifies or retrieves the maximum allowed bandwidth.</span></span>                                       |
| [<span data-ttu-id="0e64c-131">maxBitRate</span><span class="sxs-lookup"><span data-stu-id="0e64c-131">maxBitRate</span></span>](network-maxbitrate.md)               | <span data-ttu-id="0e64c-132">Recupera la velocità in bit video massima possibile.</span><span class="sxs-lookup"><span data-stu-id="0e64c-132">Retrieves the maximum possible video bit rate.</span></span>                                              |
| [<span data-ttu-id="0e64c-133">receivedPackets</span><span class="sxs-lookup"><span data-stu-id="0e64c-133">receivedPackets</span></span>](network-receivedpackets.md)     | <span data-ttu-id="0e64c-134">Recupera il numero di pacchetti ricevuti.</span><span class="sxs-lookup"><span data-stu-id="0e64c-134">Retrieves the number of packets received.</span></span>                                                   |
| [<span data-ttu-id="0e64c-135">receptionQuality</span><span class="sxs-lookup"><span data-stu-id="0e64c-135">receptionQuality</span></span>](network-receptionquality.md)   | <span data-ttu-id="0e64c-136">Recupera la percentuale di pacchetti ricevuti negli ultimi 30 secondi.</span><span class="sxs-lookup"><span data-stu-id="0e64c-136">Retrieves the percentage of packets received in the last 30 seconds.</span></span>                        |
| [<span data-ttu-id="0e64c-137">recoveredPackets</span><span class="sxs-lookup"><span data-stu-id="0e64c-137">recoveredPackets</span></span>](network-recoveredpackets.md)   | <span data-ttu-id="0e64c-138">Recupera il numero di pacchetti ripristinati.</span><span class="sxs-lookup"><span data-stu-id="0e64c-138">Retrieves the number of recovered packets.</span></span>                                                  |
| [<span data-ttu-id="0e64c-139">sourceProtocol</span><span class="sxs-lookup"><span data-stu-id="0e64c-139">sourceProtocol</span></span>](network-sourceprotocol.md)       | <span data-ttu-id="0e64c-140">Recupera il protocollo di origine utilizzato per ricevere i dati.</span><span class="sxs-lookup"><span data-stu-id="0e64c-140">Retrieves the source protocol used to receive data.</span></span>                                         |



 

<span data-ttu-id="0e64c-141">L'oggetto di **rete** supporta i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="0e64c-141">The **Network** object supports the following methods.</span></span>



| <span data-ttu-id="0e64c-142">Metodo</span><span class="sxs-lookup"><span data-stu-id="0e64c-142">Method</span></span>                                                       | <span data-ttu-id="0e64c-143">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0e64c-143">Description</span></span>                                                                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0e64c-144">getProxyBypassForLocal</span><span class="sxs-lookup"><span data-stu-id="0e64c-144">getProxyBypassForLocal</span></span>](network-getproxybypassforlocal.md) | <span data-ttu-id="0e64c-145">Recupera un valore che indica se il server proxy deve essere ignorato se il server di origine si trova in una rete locale.</span><span class="sxs-lookup"><span data-stu-id="0e64c-145">Retrieves a value indicating whether the proxy server should by bypassed if the origin server is on a local network.</span></span> |
| [<span data-ttu-id="0e64c-146">getProxyExceptionList</span><span class="sxs-lookup"><span data-stu-id="0e64c-146">getProxyExceptionList</span></span>](network-getproxyexceptionlist.md)   | <span data-ttu-id="0e64c-147">Recupera l'elenco di eccezioni del proxy.</span><span class="sxs-lookup"><span data-stu-id="0e64c-147">Retrieves the proxy exception list.</span></span>                                                                                  |
| [<span data-ttu-id="0e64c-148">getProxyName</span><span class="sxs-lookup"><span data-stu-id="0e64c-148">getProxyName</span></span>](network-getproxyname.md)                     | <span data-ttu-id="0e64c-149">Recupera il nome di un server proxy da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="0e64c-149">Retrieves the name of a proxy server to use.</span></span>                                                                         |
| [<span data-ttu-id="0e64c-150">getProxyPort</span><span class="sxs-lookup"><span data-stu-id="0e64c-150">getProxyPort</span></span>](network-getproxyport.md)                     | <span data-ttu-id="0e64c-151">Recupera la porta del proxy da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="0e64c-151">Retrieves the proxy port to use.</span></span>                                                                                     |
| [<span data-ttu-id="0e64c-152">getProxySettings</span><span class="sxs-lookup"><span data-stu-id="0e64c-152">getProxySettings</span></span>](network-getproxysettings.md)             | <span data-ttu-id="0e64c-153">Recupera l'impostazione del proxy per un protocollo specificato.</span><span class="sxs-lookup"><span data-stu-id="0e64c-153">Retrieves the proxy setting for a given protocol.</span></span>                                                                    |
| [<span data-ttu-id="0e64c-154">setProxyBypassForLocal</span><span class="sxs-lookup"><span data-stu-id="0e64c-154">setProxyBypassForLocal</span></span>](network-setproxybypassforlocal.md) | <span data-ttu-id="0e64c-155">Specifica un valore che indica se il server proxy deve essere ignorato se il server di origine si trova in una rete locale.</span><span class="sxs-lookup"><span data-stu-id="0e64c-155">Specifies a value indicating whether the proxy server should by bypassed if the origin server is on a local network.</span></span> |
| [<span data-ttu-id="0e64c-156">setProxyExceptionList</span><span class="sxs-lookup"><span data-stu-id="0e64c-156">setProxyExceptionList</span></span>](network-setproxyexceptionlist.md)   | <span data-ttu-id="0e64c-157">Specifica l'elenco di eccezioni del proxy.</span><span class="sxs-lookup"><span data-stu-id="0e64c-157">Specifies the proxy exception list.</span></span>                                                                                  |
| [<span data-ttu-id="0e64c-158">seproxyname</span><span class="sxs-lookup"><span data-stu-id="0e64c-158">setProxyName</span></span>](network-setproxyname.md)                     | <span data-ttu-id="0e64c-159">Specifica il nome di un server proxy da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="0e64c-159">Specifies the name of a proxy server to use.</span></span>                                                                         |
| [<span data-ttu-id="0e64c-160">setProxyPort</span><span class="sxs-lookup"><span data-stu-id="0e64c-160">setProxyPort</span></span>](network-setproxyport.md)                     | <span data-ttu-id="0e64c-161">Specifica la porta del proxy da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="0e64c-161">Specifies the proxy port to use.</span></span>                                                                                     |
| [<span data-ttu-id="0e64c-162">setProxySettings</span><span class="sxs-lookup"><span data-stu-id="0e64c-162">setProxySettings</span></span>](network-setproxysettings.md)             | <span data-ttu-id="0e64c-163">Specifica l'impostazione del proxy per un protocollo specificato.</span><span class="sxs-lookup"><span data-stu-id="0e64c-163">Specifies the proxy setting for a given protocol.</span></span>                                                                    |



 

<span data-ttu-id="0e64c-164">È possibile accedere all'oggetto di **rete** tramite la proprietà seguente.</span><span class="sxs-lookup"><span data-stu-id="0e64c-164">The **Network** object is accessed through the following property.</span></span>



| <span data-ttu-id="0e64c-165">Oggetto</span><span class="sxs-lookup"><span data-stu-id="0e64c-165">Object</span></span>                      | <span data-ttu-id="0e64c-166">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0e64c-166">Property</span></span>                      |
|-----------------------------|-------------------------------|
| [<span data-ttu-id="0e64c-167">Player</span><span class="sxs-lookup"><span data-stu-id="0e64c-167">Player</span></span>](player-object.md) | [<span data-ttu-id="0e64c-168">network</span><span class="sxs-lookup"><span data-stu-id="0e64c-168">network</span></span>](player-network.md) |



 

## <a name="see-also"></a><span data-ttu-id="0e64c-169">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0e64c-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e64c-170">**Riferimento del modello a oggetti per lo scripting**</span><span class="sxs-lookup"><span data-stu-id="0e64c-170">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




