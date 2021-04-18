---
title: Codici di controllo di I/O del dispositivo
description: Codici di controllo di I/O del dispositivo
ms.assetid: 46a5d166-ca8d-42df-9455-145332437153
keywords:
- Media Player di Windows, codici di controllo di I/O del dispositivo
- Media Player di Windows, codici di controllo
- Gestione dispositivi Windows Media
- codici di controllo di I/O del dispositivo
- codici di controllo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69c00e235ce0f0e68e98f4f0e37221eac0903682
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298570"
---
# <a name="device-io-control-codes"></a><span data-ttu-id="092f1-108">Codici di controllo di I/O del dispositivo</span><span class="sxs-lookup"><span data-stu-id="092f1-108">Device I/O Control Codes</span></span>

<span data-ttu-id="092f1-109">Windows Media Player 10 o versioni successive definisce Windows Media Gestione dispositivi I codici di controllo di I/O del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="092f1-109">Windows Media Player 10 or later defines Windows Media Device Manager device I/O control codes.</span></span> <span data-ttu-id="092f1-110">La tabella seguente contiene i codici di controllo e le relative descrizioni.</span><span class="sxs-lookup"><span data-stu-id="092f1-110">The following table contains the control codes and their descriptions.</span></span>



| <span data-ttu-id="092f1-111">Codice di controllo di I/O</span><span class="sxs-lookup"><span data-stu-id="092f1-111">I/O control code</span></span>                      | <span data-ttu-id="092f1-112">Valore</span><span class="sxs-lookup"><span data-stu-id="092f1-112">Value</span></span>      | <span data-ttu-id="092f1-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="092f1-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="092f1-114">**\_ \_ \_ round trip dei metadati IOCTL WMP \_**</span><span class="sxs-lookup"><span data-stu-id="092f1-114">**IOCTL\_WMP\_METADATA\_ROUND\_TRIP**</span></span> | <span data-ttu-id="092f1-115">0x31504d57</span><span class="sxs-lookup"><span data-stu-id="092f1-115">0x31504d57</span></span> | <span data-ttu-id="092f1-116">Gestisce il trasferimento delle informazioni sulle modifiche apportate ai valori dei metadati.</span><span class="sxs-lookup"><span data-stu-id="092f1-116">Manages transfer of information about changes that occurred to metadata values.</span></span> <span data-ttu-id="092f1-117">Vedere [estensioni del dispositivo per il trasferimento di metadati accelerati](device-extensions-for-accelerated-metadata-transfer.md).</span><span class="sxs-lookup"><span data-stu-id="092f1-117">See [Device Extensions for Accelerated Metadata Transfer](device-extensions-for-accelerated-metadata-transfer.md).</span></span>                                                                                                                                                                          |
| <span data-ttu-id="092f1-118">**il \_ dispositivo IOCTL WMP \_ \_ può \_ sincronizzare**</span><span class="sxs-lookup"><span data-stu-id="092f1-118">**IOCTL\_WMP\_DEVICE\_CAN\_SYNC**</span></span>     | <span data-ttu-id="092f1-119">0x32504d57</span><span class="sxs-lookup"><span data-stu-id="092f1-119">0x32504d57</span></span> | <span data-ttu-id="092f1-120">Indica se un dispositivo portatile supporta la sincronizzazione automatica.</span><span class="sxs-lookup"><span data-stu-id="092f1-120">Indicates whether a portable device supports automatic synchronization.</span></span> <span data-ttu-id="092f1-121">Windows Media Player 10 o versioni successive non fornisce buffer di input. Il buffer di output deve restituire un valore **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="092f1-121">Windows Media Player 10 or later provides no input buffer.The output buffer must return a **DWORD** value.</span></span> <span data-ttu-id="092f1-122">Il valore 1 indica che il dispositivo supporta la sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="092f1-122">A value of 1 means the device supports synchronization.</span></span> <span data-ttu-id="092f1-123">Il valore 0 indica che il dispositivo non supporta la sincronizzazione automatica.</span><span class="sxs-lookup"><span data-stu-id="092f1-123">A value of 0 means the device does not support automatic synchronization.</span></span><br/> <span data-ttu-id="092f1-124">Per ulteriori informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="092f1-124">See Remarks for more information.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="092f1-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="092f1-125">Remarks</span></span>

<span data-ttu-id="092f1-126">Questi codici di controllo sono definiti in wmpdevices. h.</span><span class="sxs-lookup"><span data-stu-id="092f1-126">These control codes are defined in wmpdevices.h.</span></span>

<span data-ttu-id="092f1-127">Se il dispositivo non supporta il **dispositivo \_ IOCTL \_ WMP \_ può \_ sincronizzare**, Windows Media Player 10 o versioni successive presuppone che il dispositivo supporti la sincronizzazione automatica.</span><span class="sxs-lookup"><span data-stu-id="092f1-127">If the device does not support **IOCTL\_WMP\_DEVICE\_CAN\_SYNC**, Windows Media Player 10 or later assumes the device supports automatic synchronization.</span></span> <span data-ttu-id="092f1-128">Si noti che, anche se questo valore può impedire la sincronizzazione automatica, sono disponibili criteri aggiuntivi per determinare se il dispositivo supporta la sincronizzazione automatica.</span><span class="sxs-lookup"><span data-stu-id="092f1-128">Note that while this value can disallow automatic synchronization, there are additional criteria used to determine whether the device supports automatic synchronization.</span></span>

## <a name="related-topics"></a><span data-ttu-id="092f1-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="092f1-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="092f1-130">**Estensioni del dispositivo per il trasferimento di metadati accelerati**</span><span class="sxs-lookup"><span data-stu-id="092f1-130">**Device Extensions for Accelerated Metadata Transfer**</span></span>](device-extensions-for-accelerated-metadata-transfer.md)
</dt> <dt>

[<span data-ttu-id="092f1-131">**Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="092f1-131">**Windows Media Player**</span></span>](windows-media-player.md)
</dt> </dl>

 

 





