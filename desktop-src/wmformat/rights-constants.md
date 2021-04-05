---
title: Costanti Rights
description: Costanti Rights
ms.assetid: fb20dc57-25da-4613-a324-e081ba87df73
keywords:
- Windows Media Format SDK, costanti
- Digital Rights Management (DRM), costanti
- DRM (Digital Rights Management), costanti
- API estese del client DRM, costanti
- API estese client, costanti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1349da53b63b1b7df59c13e0e69f7fdbf47ee3f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116897"
---
# <a name="rights-constants"></a><span data-ttu-id="bee25-108">Costanti Rights</span><span class="sxs-lookup"><span data-stu-id="bee25-108">Rights Constants</span></span>

<span data-ttu-id="bee25-109">Le costanti elencate nella tabella seguente vengono usate per identificare le azioni DRM e compilare elenchi di azioni.</span><span class="sxs-lookup"><span data-stu-id="bee25-109">The constants listed in the following table are used to identify DRM actions and to build lists of actions.</span></span>



| <span data-ttu-id="bee25-110">Costante</span><span class="sxs-lookup"><span data-stu-id="bee25-110">Constant</span></span>                                        | <span data-ttu-id="bee25-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bee25-111">Description</span></span>                                                                                                                                                                                                                                                    |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bee25-112">g \_ wszWMDRM \_ tag di azione \_</span><span class="sxs-lookup"><span data-stu-id="bee25-112">g\_wszWMDRM\_ACTIONLIST\_TAG</span></span>                    | <span data-ttu-id="bee25-113">Definisce il nome dell'elemento XML per un elenco di azioni.</span><span class="sxs-lookup"><span data-stu-id="bee25-113">Defines the XML element name for an action list.</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="bee25-114">g \_ wszWMDRM \_ \_ tag azione</span><span class="sxs-lookup"><span data-stu-id="bee25-114">g\_wszWMDRM\_ACTION\_TAG</span></span>                        | <span data-ttu-id="bee25-115">Definisce il nome dell'elemento XML per una voce in un elenco di azioni.</span><span class="sxs-lookup"><span data-stu-id="bee25-115">Defines the XML element name for an entry in an action list.</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="bee25-116">g \_ wszWMDRM \_ riproduzione a destra \_</span><span class="sxs-lookup"><span data-stu-id="bee25-116">g\_wszWMDRM\_RIGHT\_PLAYBACK</span></span>                    | <span data-ttu-id="bee25-117">Definisce la stringa per il diritto di riprodurre il contenuto.</span><span class="sxs-lookup"><span data-stu-id="bee25-117">Defines the string for the right to play content.</span></span>                                                                                                                                                                                                              |
| <span data-ttu-id="bee25-118">g \_ wszWMDRM \_ \_ copia destra</span><span class="sxs-lookup"><span data-stu-id="bee25-118">g\_wszWMDRM\_RIGHT\_COPY</span></span>                        | <span data-ttu-id="bee25-119">Definisce la stringa per il diritto di copiare il contenuto.</span><span class="sxs-lookup"><span data-stu-id="bee25-119">Defines the string for the right to copy content.</span></span>                                                                                                                                                                                                              |
| <span data-ttu-id="bee25-120">g \_ wszWMDRM a \_ destra della \_ playlist \_</span><span class="sxs-lookup"><span data-stu-id="bee25-120">g\_wszWMDRM\_RIGHT\_PLAYLIST\_BURN</span></span>              | <span data-ttu-id="bee25-121">Definisce la stringa per il diritto di masterizzare il contenuto su CD come parte di una playlist.</span><span class="sxs-lookup"><span data-stu-id="bee25-121">Defines the string for the right to burn content to CD as part of a playlist.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="bee25-122">g \_ wszWMDRM a \_ destra \_ creare un' \_ immagine di anteprima \_</span><span class="sxs-lookup"><span data-stu-id="bee25-122">g\_wszWMDRM\_RIGHT\_CREATE\_THUMBNAIL\_IMAGE</span></span>    | <span data-ttu-id="bee25-123">Definisce la stringa per il diritto di creare un'immagine di anteprima dal contenuto video.</span><span class="sxs-lookup"><span data-stu-id="bee25-123">Defines the string for the right to create a thumbnail image from video content.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="bee25-124">g \_ wszWMDRM \_ la \_ copia corretta \_ su \_ CD</span><span class="sxs-lookup"><span data-stu-id="bee25-124">g\_wszWMDRM\_RIGHT\_COPY\_TO\_CD</span></span>                | <span data-ttu-id="bee25-125">Definisce la stringa per il diritto di copiare il contenuto in un CD.</span><span class="sxs-lookup"><span data-stu-id="bee25-125">Defines the string for the right to copy content to a CD.</span></span> <span data-ttu-id="bee25-126">Le nuove licenze non devono utilizzare questo diritto.</span><span class="sxs-lookup"><span data-stu-id="bee25-126">New licenses should not use this right.</span></span> <span data-ttu-id="bee25-127">Al contrario, tutti i diritti che concedono l'autorizzazione per la copia del contenuto devono essere coperti dal diritto di copia e dal diritto di masterizzazione della playlist.</span><span class="sxs-lookup"><span data-stu-id="bee25-127">Instead, all rights granting permission to copy content should be covered by the copy right and the playlist burn right.</span></span>                                     |
| <span data-ttu-id="bee25-128">g \_ wszWMDRM \_ la \_ Copia \_ destra \_ nel \_ dispositivo SDMI</span><span class="sxs-lookup"><span data-stu-id="bee25-128">g\_wszWMDRM\_RIGHT\_COPY\_TO\_SDMI\_DEVICE</span></span>      | <span data-ttu-id="bee25-129">Definisce la stringa per il diritto di copiare il contenuto in un dispositivo conforme a Secure Digital Music Initiative (SDMI).</span><span class="sxs-lookup"><span data-stu-id="bee25-129">Defines the string for the right to copy content to a device that conforms to the Secure Digital Music Initiative (SDMI).</span></span> <span data-ttu-id="bee25-130">Le nuove licenze non devono utilizzare questo diritto.</span><span class="sxs-lookup"><span data-stu-id="bee25-130">New licenses should not use this right.</span></span> <span data-ttu-id="bee25-131">Al contrario, tutti i diritti che concedono l'autorizzazione per la copia del contenuto devono essere coperti dal diritto di copia.</span><span class="sxs-lookup"><span data-stu-id="bee25-131">Instead, all rights granting permission to copy content should be covered by the copy right.</span></span> |
| <span data-ttu-id="bee25-132">g \_ wszWMDRM \_ la \_ copia destra \_ in un \_ \_ dispositivo non SDMI \_</span><span class="sxs-lookup"><span data-stu-id="bee25-132">g\_wszWMDRM\_RIGHT\_COPY\_TO\_NON\_SDMI\_DEVICE</span></span> | <span data-ttu-id="bee25-133">Definisce la stringa per il diritto di copiare in un dispositivo che non è conforme a Secure Digital Music Initiative (SDMI).</span><span class="sxs-lookup"><span data-stu-id="bee25-133">Defines the string for the right to copy to a device that does not conform to the Secure Digital Music Initiative (SDMI).</span></span> <span data-ttu-id="bee25-134">Le nuove licenze non devono utilizzare questo diritto.</span><span class="sxs-lookup"><span data-stu-id="bee25-134">New licenses should not use this right.</span></span> <span data-ttu-id="bee25-135">Al contrario, tutti i diritti che concedono l'autorizzazione per la copia del contenuto devono essere coperti dal diritto di copia.</span><span class="sxs-lookup"><span data-stu-id="bee25-135">Instead, all rights granting permission to copy content should be covered by the copy right.</span></span> |
| <span data-ttu-id="bee25-136">g \_ wszWMDRM \_ right \_ backup</span><span class="sxs-lookup"><span data-stu-id="bee25-136">g\_wszWMDRM\_RIGHT\_BACKUP</span></span>                      | <span data-ttu-id="bee25-137">Definisce la stringa per il diritto di eseguire il backup della licenza.</span><span class="sxs-lookup"><span data-stu-id="bee25-137">Defines the string for the right to backup the license.</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="bee25-138">g \_ wszWMDRM \_ right \_ collaborative \_ Play</span><span class="sxs-lookup"><span data-stu-id="bee25-138">g\_wszWMDRM\_RIGHT\_COLLABORATIVE\_PLAY</span></span>         | <span data-ttu-id="bee25-139">Definisce la stringa per il diritto di riprodurre il contenuto su una rete come parte di una playlist condivisa.</span><span class="sxs-lookup"><span data-stu-id="bee25-139">Defines the string for the right to play content over a network as part of a shared playlist.</span></span>                                                                                                                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="bee25-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bee25-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bee25-141">**Costanti**</span><span class="sxs-lookup"><span data-stu-id="bee25-141">**Constants**</span></span>](constants.md)
</dt> </dl>

 

 




