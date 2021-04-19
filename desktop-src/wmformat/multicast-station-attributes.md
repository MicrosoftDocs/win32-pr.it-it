---
title: Attributi della stazione multicast
description: Attributi della stazione multicast
ms.assetid: 24b81ccb-4030-49a4-802c-5b45f7dd5950
keywords:
- Windows Media Format SDK, attributi
- ASF (Advanced Systems Format), attributi
- ASF (formato avanzato dei sistemi), attributi
- attributi, stazione multicast
- attributi della stazione multicast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f618ffa645055bf10a9247272d57c7e3f76853c0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298895"
---
# <a name="multicast-station-attributes"></a><span data-ttu-id="36a4d-108">Attributi della stazione multicast</span><span class="sxs-lookup"><span data-stu-id="36a4d-108">Multicast Station Attributes</span></span>

<span data-ttu-id="36a4d-109">Quando si esegue il flusso di un file da una stazione multicast, la stazione può imporre alcuni attributi sul file.</span><span class="sxs-lookup"><span data-stu-id="36a4d-109">When a file is streaming from a multicast station, the station can impose some attributes on the file.</span></span> <span data-ttu-id="36a4d-110">Questi attributi, elencati nella tabella seguente, non vengono effettivamente archiviati nel file e sono disponibili solo quando si esegue il flusso del file.</span><span class="sxs-lookup"><span data-stu-id="36a4d-110">These attributes, listed in the following table, are not actually stored in the file and are only available when the file is streaming.</span></span> <span data-ttu-id="36a4d-111">Contengono informazioni sulla stazione e sono in genere identiche per tutto il contenuto della stazione.</span><span class="sxs-lookup"><span data-stu-id="36a4d-111">They contain information about the station and would typically be identical for all content from the station.</span></span>



| <span data-ttu-id="36a4d-112">Attributo stazione multicast</span><span class="sxs-lookup"><span data-stu-id="36a4d-112">Multicast station attribute</span></span>                 | <span data-ttu-id="36a4d-113">Identificatore globale</span><span class="sxs-lookup"><span data-stu-id="36a4d-113">Global identifier</span></span>      | <span data-ttu-id="36a4d-114">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="36a4d-114">Data type</span></span>             |
|---------------------------------------------|------------------------|-----------------------|
| [<span data-ttu-id="36a4d-115">**\_Indirizzo NSC**</span><span class="sxs-lookup"><span data-stu-id="36a4d-115">**NSC\_Address**</span></span>](nsc-address.md)         | <span data-ttu-id="36a4d-116">g \_ wszWMNSCAddress</span><span class="sxs-lookup"><span data-stu-id="36a4d-116">g\_wszWMNSCAddress</span></span>     | <span data-ttu-id="36a4d-117">**\_stringa di tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="36a4d-117">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="36a4d-118">**\_Descrizione NSC**</span><span class="sxs-lookup"><span data-stu-id="36a4d-118">**NSC\_Description**</span></span>](nsc-description.md) | <span data-ttu-id="36a4d-119">g \_ wszWMNSCDescription</span><span class="sxs-lookup"><span data-stu-id="36a4d-119">g\_wszWMNSCDescription</span></span> | <span data-ttu-id="36a4d-120">**\_stringa di tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="36a4d-120">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="36a4d-121">**\_Posta elettronica NSC**</span><span class="sxs-lookup"><span data-stu-id="36a4d-121">**NSC\_Email**</span></span>](nsc-email.md)             | <span data-ttu-id="36a4d-122">g \_ wszWMNSCEmail</span><span class="sxs-lookup"><span data-stu-id="36a4d-122">g\_wszWMNSCEmail</span></span>       | <span data-ttu-id="36a4d-123">**\_stringa di tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="36a4d-123">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="36a4d-124">**\_Nome NSC**</span><span class="sxs-lookup"><span data-stu-id="36a4d-124">**NSC\_Name**</span></span>](nsc-name.md)               | <span data-ttu-id="36a4d-125">g \_ wszWMNSCName</span><span class="sxs-lookup"><span data-stu-id="36a4d-125">g\_wszWMNSCName</span></span>        | <span data-ttu-id="36a4d-126">**\_stringa di tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="36a4d-126">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="36a4d-127">**\_Telefono NSC**</span><span class="sxs-lookup"><span data-stu-id="36a4d-127">**NSC\_Phone**</span></span>](nsc-phone.md)             | <span data-ttu-id="36a4d-128">g \_ wszWMNSCPhone</span><span class="sxs-lookup"><span data-stu-id="36a4d-128">g\_wszWMNSCPhone</span></span>       | <span data-ttu-id="36a4d-129">**\_stringa di tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="36a4d-129">**WMT\_TYPE\_STRING**</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="36a4d-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="36a4d-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36a4d-131">**Attributi per tipo**</span><span class="sxs-lookup"><span data-stu-id="36a4d-131">**Attributes By Type**</span></span>](attributes-by-type.md)
</dt> <dt>

[<span data-ttu-id="36a4d-132">**Elenco degli attributi**</span><span class="sxs-lookup"><span data-stu-id="36a4d-132">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




