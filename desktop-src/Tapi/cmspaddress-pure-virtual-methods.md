---
description: Questi metodi devono essere sottoposti a override dalle classi derivate.
ms.assetid: 68402cff-effd-4a2b-b9f9-f13f233b1555
title: Metodi virtuali puri CMSPAddress
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a93c9b2a995554dd2f7412c8fa5bf153ea8871e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312728"
---
# <a name="cmspaddress-pure-virtual-methods"></a><span data-ttu-id="16b16-103">Metodi virtuali puri CMSPAddress</span><span class="sxs-lookup"><span data-stu-id="16b16-103">CMSPAddress Pure Virtual Methods</span></span>

<span data-ttu-id="16b16-104">Questi metodi devono essere sottoposti a override dalle classi derivate.</span><span class="sxs-lookup"><span data-stu-id="16b16-104">These methods must be overridden by derived classes.</span></span>



| <span data-ttu-id="16b16-105">Metodi virtuali puri CMSPAddress</span><span class="sxs-lookup"><span data-stu-id="16b16-105">CMSPAddress pure virtual methods</span></span>                           | <span data-ttu-id="16b16-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16b16-106">Description</span></span>                                                                                                                                                                            |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="16b16-107">**MSPAddressAddRef**</span><span class="sxs-lookup"><span data-stu-id="16b16-107">**MSPAddressAddRef**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressaddref)   | <span data-ttu-id="16b16-108">Metodo AddRef privato per l'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="16b16-108">Private AddRef method for the address.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="16b16-109">**MSPAddressRelease**</span><span class="sxs-lookup"><span data-stu-id="16b16-109">**MSPAddressRelease**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressrelease) | <span data-ttu-id="16b16-110">Metodo di rilascio privato per l'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="16b16-110">Private Release method for the address.</span></span>                                                                                                                                                |
| [<span data-ttu-id="16b16-111">**CreateMSPCall**</span><span class="sxs-lookup"><span data-stu-id="16b16-111">**CreateMSPCall**</span></span>](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)        | <span data-ttu-id="16b16-112">Chiamato da TAPI per creare un oggetto chiamata.</span><span class="sxs-lookup"><span data-stu-id="16b16-112">Called by TAPI to create a call object.</span></span> <span data-ttu-id="16b16-113">L'implementazione nella classe derivata deve semplicemente chiamare la funzione [**CreateMSPCallHelper**](/windows/desktop/api/Mspaddr/nf-mspaddr-createmspcallhelper) .</span><span class="sxs-lookup"><span data-stu-id="16b16-113">The implementation in the derived class should simply call the [**CreateMSPCallHelper**](/windows/desktop/api/Mspaddr/nf-mspaddr-createmspcallhelper) function.</span></span>        |
| [<span data-ttu-id="16b16-114">**ShutdownMSPCall**</span><span class="sxs-lookup"><span data-stu-id="16b16-114">**ShutdownMSPCall**</span></span>](/windows/desktop/api/msp/nf-msp-itmspaddress-shutdownmspcall)    | <span data-ttu-id="16b16-115">Chiamato da TAPI per arrestare un oggetto chiamata.</span><span class="sxs-lookup"><span data-stu-id="16b16-115">Called by TAPI to shut down a call object.</span></span> <span data-ttu-id="16b16-116">L'implementazione nella classe derivata deve semplicemente chiamare la funzione [**ShutdownMSPCallHelper**](/windows/desktop/api/Mspaddr/nf-mspaddr-shutdownmspcallhelper) .</span><span class="sxs-lookup"><span data-stu-id="16b16-116">The implementation in the derived class should simply call the [**ShutdownMSPCallHelper**](/windows/desktop/api/Mspaddr/nf-mspaddr-shutdownmspcallhelper) function.</span></span> |
| [<span data-ttu-id="16b16-117">**GetCallMediaTypes**</span><span class="sxs-lookup"><span data-stu-id="16b16-117">**GetCallMediaTypes**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getcallmediatypes) | <span data-ttu-id="16b16-118">Ottiene i tipi di supporto supportati dall'MSP.</span><span class="sxs-lookup"><span data-stu-id="16b16-118">Gets media types supported by the MSP.</span></span>                                                                                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="16b16-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="16b16-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16b16-120">**CMSPAddress**</span><span class="sxs-lookup"><span data-stu-id="16b16-120">**CMSPAddress**</span></span>](/windows/desktop/api/Mspaddr/nl-mspaddr-cmspaddress)
</dt> </dl>

 

 



