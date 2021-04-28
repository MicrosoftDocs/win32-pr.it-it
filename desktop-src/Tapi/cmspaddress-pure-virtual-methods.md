---
description: 'Metodi virtuali puri CMSPAddress: questi metodi devono essere sottoposti a override dalle classi derivate.'
ms.assetid: 68402cff-effd-4a2b-b9f9-f13f233b1555
title: Metodi virtuali puri CMSPAddress
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c9d9b9494e4ee42972d97433927fd587034af81
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084209"
---
# <a name="cmspaddress-pure-virtual-methods"></a><span data-ttu-id="ad375-103">Metodi virtuali puri CMSPAddress</span><span class="sxs-lookup"><span data-stu-id="ad375-103">CMSPAddress Pure Virtual Methods</span></span>

<span data-ttu-id="ad375-104">Questi metodi devono essere sottoposti a override dalle classi derivate.</span><span class="sxs-lookup"><span data-stu-id="ad375-104">These methods must be overridden by derived classes.</span></span>



| <span data-ttu-id="ad375-105">Metodi virtuali puri CMSPAddress</span><span class="sxs-lookup"><span data-stu-id="ad375-105">CMSPAddress pure virtual methods</span></span>                           | <span data-ttu-id="ad375-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad375-106">Description</span></span>                                                                                                                                                                            |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ad375-107">**MSPAddressAddRef**</span><span class="sxs-lookup"><span data-stu-id="ad375-107">**MSPAddressAddRef**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressaddref)   | <span data-ttu-id="ad375-108">Metodo AddRef privato per l'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="ad375-108">Private AddRef method for the address.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="ad375-109">**MSPAddressRelease**</span><span class="sxs-lookup"><span data-stu-id="ad375-109">**MSPAddressRelease**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressrelease) | <span data-ttu-id="ad375-110">Metodo Release privato per l'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="ad375-110">Private Release method for the address.</span></span>                                                                                                                                                |
| [<span data-ttu-id="ad375-111">**CreateMSPCall**</span><span class="sxs-lookup"><span data-stu-id="ad375-111">**CreateMSPCall**</span></span>](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)        | <span data-ttu-id="ad375-112">Chiamato da TAPI per creare un oggetto chiamata.</span><span class="sxs-lookup"><span data-stu-id="ad375-112">Called by TAPI to create a call object.</span></span> <span data-ttu-id="ad375-113">L'implementazione nella classe derivata deve semplicemente chiamare [**la funzione CreateMSPCallHelper.**](/windows/desktop/api/Mspaddr/nf-mspaddr-createmspcallhelper)</span><span class="sxs-lookup"><span data-stu-id="ad375-113">The implementation in the derived class should simply call the [**CreateMSPCallHelper**](/windows/desktop/api/Mspaddr/nf-mspaddr-createmspcallhelper) function.</span></span>        |
| [<span data-ttu-id="ad375-114">**ShutdownMSPCall**</span><span class="sxs-lookup"><span data-stu-id="ad375-114">**ShutdownMSPCall**</span></span>](/windows/desktop/api/msp/nf-msp-itmspaddress-shutdownmspcall)    | <span data-ttu-id="ad375-115">Chiamato da TAPI per arrestare un oggetto chiamata.</span><span class="sxs-lookup"><span data-stu-id="ad375-115">Called by TAPI to shut down a call object.</span></span> <span data-ttu-id="ad375-116">L'implementazione nella classe derivata deve chiamare semplicemente la [**funzione ShutdownMSPCallHelper.**](/windows/desktop/api/Mspaddr/nf-mspaddr-shutdownmspcallhelper)</span><span class="sxs-lookup"><span data-stu-id="ad375-116">The implementation in the derived class should simply call the [**ShutdownMSPCallHelper**](/windows/desktop/api/Mspaddr/nf-mspaddr-shutdownmspcallhelper) function.</span></span> |
| [<span data-ttu-id="ad375-117">**GetCallMediaTypes**</span><span class="sxs-lookup"><span data-stu-id="ad375-117">**GetCallMediaTypes**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getcallmediatypes) | <span data-ttu-id="ad375-118">Ottiene i tipi di supporti supportati dal msp.</span><span class="sxs-lookup"><span data-stu-id="ad375-118">Gets media types supported by the MSP.</span></span>                                                                                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="ad375-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ad375-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad375-120">**CMSPAddress**</span><span class="sxs-lookup"><span data-stu-id="ad375-120">**CMSPAddress**</span></span>](/windows/desktop/api/Mspaddr/nl-mspaddr-cmspaddress)
</dt> </dl>

 

 



