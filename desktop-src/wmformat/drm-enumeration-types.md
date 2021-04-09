---
title: Tipi di enumerazione client DRM di Microsoft Windows Media
description: Tipi di enumerazione
ms.assetid: 940f66e1-1dc1-414f-bba9-b91f4f0dfc45
keywords:
- Windows Media Format SDK, tipi di enumerazione
- Digital Rights Management (DRM), tipi di enumerazione
- DRM (Digital Rights Management), tipi di enumerazione
- API estese del client DRM, tipi di enumerazione
- API estese client, tipi di enumerazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c159342367035767d213d57987d93d23eb321a6c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104047725"
---
# <a name="microsoft-windows-media-drm-client-enumeration-types"></a><span data-ttu-id="6f16d-108">Tipi di enumerazione client DRM di Microsoft Windows Media</span><span class="sxs-lookup"><span data-stu-id="6f16d-108">Microsoft Windows Media DRM Client Enumeration Types</span></span>

<span data-ttu-id="6f16d-109">Nella tabella seguente vengono descritte le enumerazioni supportate dalle API estese del client DRM di Microsoft Windows Media.</span><span class="sxs-lookup"><span data-stu-id="6f16d-109">The following table describes the enumerations that are supported by the Microsoft Windows Media DRM Client Extended APIs.</span></span>



| <span data-ttu-id="6f16d-110">Enumerazione</span><span class="sxs-lookup"><span data-stu-id="6f16d-110">Enumeration</span></span>                                                                      | <span data-ttu-id="6f16d-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6f16d-111">Description</span></span>                                                                                                                                                   |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6f16d-112">**azione DRM- \_ \_ Risultati della query consentiti \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6f16d-112">**DRM\_ACTION\_ALLOWED\_QUERY\_RESULTS**</span></span>](drm-action-allowed-query-results.md) | <span data-ttu-id="6f16d-113">Usato dall'interfaccia [**IWMDRMLicenseQuery:: QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) per specificare il motivo per cui non è consentita un'azione.</span><span class="sxs-lookup"><span data-stu-id="6f16d-113">Used by the [**IWMDRMLicenseQuery::QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) interface to specify the reason an action is not allowed.</span></span> |
| [<span data-ttu-id="6f16d-114">**tipo di dati attr di DRM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6f16d-114">**DRM\_ATTR\_DATATYPE**</span></span>](drm-attr-datatype.md)                                 | <span data-ttu-id="6f16d-115">Definisce i tipi di dati utilizzati per le proprietà e gli attributi DRM.</span><span class="sxs-lookup"><span data-stu-id="6f16d-115">Defines the data types used for DRM attributes and properties.</span></span>                                                                                                |
| [<span data-ttu-id="6f16d-116">**\_tipo di crittografia DRM \_**</span><span class="sxs-lookup"><span data-stu-id="6f16d-116">**DRM\_CRYPTO\_TYPE**</span></span>](drm-crypto-type.md)                                     | <span data-ttu-id="6f16d-117">Definisce i tipi di algoritmi di crittografia che possono essere usati per crittografare il contenuto.</span><span class="sxs-lookup"><span data-stu-id="6f16d-117">Defines the cryptographic algorithm types that can be used to encrypt content.</span></span>                                                                                |
| [<span data-ttu-id="6f16d-118">**\_stato http \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="6f16d-118">**DRM\_HTTP\_STATUS**</span></span>](drmdrm-http-status.md)                                  | <span data-ttu-id="6f16d-119">Definisce un intervallo di stati HTTP per una richiesta DRM.</span><span class="sxs-lookup"><span data-stu-id="6f16d-119">Defines a range of HTTP states for a DRM request.</span></span>                                                                                                             |
| [<span data-ttu-id="6f16d-120">**\_stato di individualizzazione DRM \_**</span><span class="sxs-lookup"><span data-stu-id="6f16d-120">**DRM\_INDIVIDUALIZATION\_STATUS**</span></span>](drmdrm-individualization-status.md)        | <span data-ttu-id="6f16d-121">Definisce gli stati validi per l'individualizzazione DRM.</span><span class="sxs-lookup"><span data-stu-id="6f16d-121">Defines the valid states for DRM individualization.</span></span>                                                                                                           |
| [<span data-ttu-id="6f16d-122">**\_ \_ Categoria stato della licenza DRM \_**</span><span class="sxs-lookup"><span data-stu-id="6f16d-122">**DRM\_LICENSE\_STATE\_CATEGORY**</span></span>](drmdrm-license-state-category.md)           | <span data-ttu-id="6f16d-123">Specifica il tipo di restrizione della licenza descritta dalla struttura [**\_ \_ \_ dei dati dello stato delle licenze DRM**](drmdrm-license-state-data.md) .</span><span class="sxs-lookup"><span data-stu-id="6f16d-123">Specifies the type of license restriction that is described by a [**DRM\_LICENSE\_STATE\_DATA**](drmdrm-license-state-data.md) structure.</span></span>                    |
| [<span data-ttu-id="6f16d-124">**\_stato msdrm**</span><span class="sxs-lookup"><span data-stu-id="6f16d-124">**MSDRM\_STATUS**</span></span>](msdrm-status.md)                                            | <span data-ttu-id="6f16d-125">Definisce le condizioni di stato per il sottosistema DRM.</span><span class="sxs-lookup"><span data-stu-id="6f16d-125">Defines status conditions for the DRM subsystem.</span></span>                                                                                                              |
| [<span data-ttu-id="6f16d-126">**\_tipo di criteri WMDRMNET \_**</span><span class="sxs-lookup"><span data-stu-id="6f16d-126">**WMDRMNET\_POLICY\_TYPE**</span></span>](wmdrmnet-policy-type.md)                           | <span data-ttu-id="6f16d-127">Elenca i tipi di criteri disponibili per le operazioni di Windows Media DRM per i dispositivi di rete.</span><span class="sxs-lookup"><span data-stu-id="6f16d-127">Lists the types of policies that are available for Windows Media DRM for Network Devices operations.</span></span>                                                          |
| [<span data-ttu-id="6f16d-128">**\_diritti WMT**</span><span class="sxs-lookup"><span data-stu-id="6f16d-128">**WMT\_RIGHTS**</span></span>](drm-wmt-rights.md)                                            | <span data-ttu-id="6f16d-129">Definisce i diritti che possono essere specificati in una licenza DRM.</span><span class="sxs-lookup"><span data-stu-id="6f16d-129">Defines the rights that may be specified in a DRM license.</span></span>                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="6f16d-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6f16d-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f16d-131">**Guida di riferimento alla programmazione**</span><span class="sxs-lookup"><span data-stu-id="6f16d-131">**Programming Reference**</span></span>](drm-programming-reference.md)
</dt> </dl>

 

 




