---
title: Estensioni del dispositivo per il trasferimento di metadati accelerati
description: Estensioni del dispositivo per il trasferimento di metadati accelerati
ms.assetid: a79b54d4-dad5-411b-aaff-b58bb549d4d1
keywords:
- Windows Media Player, estensioni del dispositivo
- Windows Media Player, estensioni
- Windows Media Player, trasferimento di metadati accelerato
- Windows Media Player, trasferimento accelerato dei metadati
- trasferimento di metadati accelerato
- metadati, trasferimento accelerato
- estensioni del dispositivo, trasferimento di metadati accelerato
- estensioni, trasferimento di metadati accelerato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbe661dff0750f2ad46bef96e537b0852d480db8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044965"
---
# <a name="device-extensions-for-accelerated-metadata-transfer"></a><span data-ttu-id="7cf18-111">Estensioni del dispositivo per il trasferimento di metadati accelerati</span><span class="sxs-lookup"><span data-stu-id="7cf18-111">Device Extensions for Accelerated Metadata Transfer</span></span>

<span data-ttu-id="7cf18-112">Windows Media Player 10 ha introdotto funzionalità nuove ed estese per la sincronizzazione di file multimediali digitali con dispositivi portatili.</span><span class="sxs-lookup"><span data-stu-id="7cf18-112">Windows Media Player 10 introduced new and extended functionality for synchronizing digital media files with portable devices.</span></span> <span data-ttu-id="7cf18-113">Gli utenti possono connettere un dispositivo a un computer, trasferire il contenuto al dispositivo, quindi disconnettere il dispositivo per sfruttare i contenuti del computer.</span><span class="sxs-lookup"><span data-stu-id="7cf18-113">Users can connect a device to a computer, transfer content to the device, and then disconnect the device to enjoy content away from the computer.</span></span>

<span data-ttu-id="7cf18-114">Quando l'utente riconnette il dispositivo al computer, è possibile che il contenuto archiviato nel dispositivo sia stato modificato dopo la connessione precedente.</span><span class="sxs-lookup"><span data-stu-id="7cf18-114">When the user reconnects the device to the computer, it is possible that the content stored on the device changed since the previous connection.</span></span> <span data-ttu-id="7cf18-115">Ad esempio, la semplice riproduzione di un file multimediale digitale particolare causa la modifica del numero di riscontri per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="7cf18-115">For example, simply playing a particular digital media file causes the play count for that item to change.</span></span> <span data-ttu-id="7cf18-116">Poiché i dispositivi portatili correnti possono archiviare grandi quantità di contenuti multimediali digitali, il processo di individuazione delle modifiche richiederebbe troppo tempo se Windows Media Player fosse necessario per enumerare e ispezionare ogni elemento multimediale digitale.</span><span class="sxs-lookup"><span data-stu-id="7cf18-116">Because current portable devices can store large quantities of digital media content, the process of discovering changes would be too time consuming if Windows Media Player were required to enumerate and inspect each digital media item.</span></span> <span data-ttu-id="7cf18-117">I produttori di dispositivi portatili possono invece implementare funzionalità speciali per consentire a Windows Media Player 10 o versioni successive di recuperare in modo efficiente le informazioni sulle modifiche apportate al contenuto archiviato in un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7cf18-117">Instead, portable device manufacturers can implement special functionality to enable Windows Media Player 10 or later to efficiently retrieve information about changes made to the content stored on a device.</span></span>

<span data-ttu-id="7cf18-118">Nelle sezioni seguenti vengono descritte le convenzioni utilizzate per implementare questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="7cf18-118">The following sections describe the conventions used to implement this functionality.</span></span>

-   [<span data-ttu-id="7cf18-119">Informazioni sui metadati</span><span class="sxs-lookup"><span data-stu-id="7cf18-119">About the Metadata</span></span>](about-the-metadata.md)
-   [<span data-ttu-id="7cf18-120">Estensioni del dispositivo MTP per il trasferimento dei metadati</span><span class="sxs-lookup"><span data-stu-id="7cf18-120">MTP Device Extensions for Metadata Transfer</span></span>](mtp-device-extensions-for-metadata-transfer.md)
-   [<span data-ttu-id="7cf18-121">Estensioni del dispositivo Windows Media Gestione dispositivi per il trasferimento dei metadati</span><span class="sxs-lookup"><span data-stu-id="7cf18-121">Windows Media Device Manager Device Extensions for Metadata Transfer</span></span>](windows-media-device-manager-device-extensions-for-metadata-transfer.md)

## <a name="related-topics"></a><span data-ttu-id="7cf18-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7cf18-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7cf18-123">**Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="7cf18-123">**Windows Media Player**</span></span>](windows-media-player.md)
</dt> </dl>

 

 




