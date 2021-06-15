---
title: Tipi di enumerazione client DRM di Microsoft Windows Media
description: Informazioni sulle enumerazioni supportate dalle API estese del client DRM di Microsoft Windows Media.
ms.assetid: 940f66e1-1dc1-414f-bba9-b91f4f0dfc45
keywords:
- Windows Media Format SDK, tipi di enumerazione
- digital rights management (DRM), tipi di enumerazione
- DRM (digital rights management),tipi di enumerazione
- API estese del client DRM, tipi di enumerazione
- API estese del client, tipi di enumerazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 574136f8016161f4d2c208865a72ad2a86d98f68
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068428"
---
# <a name="microsoft-windows-media-drm-client-enumeration-types"></a><span data-ttu-id="415a8-108">Tipi di enumerazione client DRM di Microsoft Windows Media</span><span class="sxs-lookup"><span data-stu-id="415a8-108">Microsoft Windows Media DRM Client Enumeration Types</span></span>

<span data-ttu-id="415a8-109">Nella tabella seguente vengono descritte le enumerazioni supportate dalle API estese del client DRM di Microsoft Windows Media.</span><span class="sxs-lookup"><span data-stu-id="415a8-109">The following table describes the enumerations that are supported by the Microsoft Windows Media DRM Client Extended APIs.</span></span>



| <span data-ttu-id="415a8-110">Enumerazione</span><span class="sxs-lookup"><span data-stu-id="415a8-110">Enumeration</span></span>                                                                      | <span data-ttu-id="415a8-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="415a8-111">Description</span></span>                                                                                                                                                   |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="415a8-112">**AZIONE DRM \_ \_ CONSENTITA RISULTATI \_ QUERY \_**</span><span class="sxs-lookup"><span data-stu-id="415a8-112">**DRM\_ACTION\_ALLOWED\_QUERY\_RESULTS**</span></span>](drm-action-allowed-query-results.md) | <span data-ttu-id="415a8-113">Usata [**dall'interfaccia IWMDRMLicenseQuery::QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) per specificare il motivo per cui un'azione non è consentita.</span><span class="sxs-lookup"><span data-stu-id="415a8-113">Used by the [**IWMDRMLicenseQuery::QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) interface to specify the reason an action is not allowed.</span></span> |
| [<span data-ttu-id="415a8-114">**TIPO DI \_ DATI ATTR \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="415a8-114">**DRM\_ATTR\_DATATYPE**</span></span>](drm-attr-datatype.md)                                 | <span data-ttu-id="415a8-115">Definisce i tipi di dati usati per le proprietà e gli attributi DRM.</span><span class="sxs-lookup"><span data-stu-id="415a8-115">Defines the data types used for DRM attributes and properties.</span></span>                                                                                                |
| [<span data-ttu-id="415a8-116">**TIPO DI \_ CRITTOGRAFIA \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="415a8-116">**DRM\_CRYPTO\_TYPE**</span></span>](drm-crypto-type.md)                                     | <span data-ttu-id="415a8-117">Definisce i tipi di algoritmo di crittografia che possono essere usati per crittografare il contenuto.</span><span class="sxs-lookup"><span data-stu-id="415a8-117">Defines the cryptographic algorithm types that can be used to encrypt content.</span></span>                                                                                |
| [<span data-ttu-id="415a8-118">**STATO \_ HTTP \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="415a8-118">**DRM\_HTTP\_STATUS**</span></span>](drmdrm-http-status.md)                                  | <span data-ttu-id="415a8-119">Definisce un intervallo di stati HTTP per una richiesta DRM.</span><span class="sxs-lookup"><span data-stu-id="415a8-119">Defines a range of HTTP states for a DRM request.</span></span>                                                                                                             |
| [<span data-ttu-id="415a8-120">**STATO \_ DI INDIVIDUALIZZAZIONE \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="415a8-120">**DRM\_INDIVIDUALIZATION\_STATUS**</span></span>](drmdrm-individualization-status.md)        | <span data-ttu-id="415a8-121">Definisce gli stati validi per l'individualizzazione DRM.</span><span class="sxs-lookup"><span data-stu-id="415a8-121">Defines the valid states for DRM individualization.</span></span>                                                                                                           |
| [<span data-ttu-id="415a8-122">**CATEGORIA STATO \_ LICENZA \_ \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="415a8-122">**DRM\_LICENSE\_STATE\_CATEGORY**</span></span>](drmdrm-license-state-category.md)           | <span data-ttu-id="415a8-123">Specifica il tipo di restrizione di licenza descritto da una [**struttura DRM \_ LICENSE STATE \_ \_ DATA.**](drmdrm-license-state-data.md)</span><span class="sxs-lookup"><span data-stu-id="415a8-123">Specifies the type of license restriction that is described by a [**DRM\_LICENSE\_STATE\_DATA**](drmdrm-license-state-data.md) structure.</span></span>                    |
| [<span data-ttu-id="415a8-124">**STATO DI \_ MSDRM**</span><span class="sxs-lookup"><span data-stu-id="415a8-124">**MSDRM\_STATUS**</span></span>](msdrm-status.md)                                            | <span data-ttu-id="415a8-125">Definisce le condizioni di stato per il sottosistema DRM.</span><span class="sxs-lookup"><span data-stu-id="415a8-125">Defines status conditions for the DRM subsystem.</span></span>                                                                                                              |
| [<span data-ttu-id="415a8-126">**TIPO DI CRITERI WMDRMNET \_ \_**</span><span class="sxs-lookup"><span data-stu-id="415a8-126">**WMDRMNET\_POLICY\_TYPE**</span></span>](wmdrmnet-policy-type.md)                           | <span data-ttu-id="415a8-127">Elenca i tipi di criteri disponibili per Windows Media DRM per le operazioni dei dispositivi di rete.</span><span class="sxs-lookup"><span data-stu-id="415a8-127">Lists the types of policies that are available for Windows Media DRM for Network Devices operations.</span></span>                                                          |
| [<span data-ttu-id="415a8-128">**DIRITTI \_ WMT**</span><span class="sxs-lookup"><span data-stu-id="415a8-128">**WMT\_RIGHTS**</span></span>](drm-wmt-rights.md)                                            | <span data-ttu-id="415a8-129">Definisce i diritti che possono essere specificati in una licenza DRM.</span><span class="sxs-lookup"><span data-stu-id="415a8-129">Defines the rights that may be specified in a DRM license.</span></span>                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="415a8-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="415a8-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="415a8-131">**Guida di riferimento alla programmazione**</span><span class="sxs-lookup"><span data-stu-id="415a8-131">**Programming Reference**</span></span>](drm-programming-reference.md)
</dt> </dl>

 

 




