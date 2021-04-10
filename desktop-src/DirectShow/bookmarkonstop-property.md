---
description: La proprietà DVDAdm. BookmarkOnStop imposta o recupera un valore che indica all'oggetto MSWebDVD se salvare automaticamente un segnalibro della posizione e delle impostazioni correnti quando l'utente fa clic sul pulsante Interrompi.
ms.assetid: bcadaa3c-23b7-4408-8199-058103a92a34
title: Proprietà BookmarkOnStop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 355ae01c43ef28a086c76f4716fe3d46d250fbe4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125055"
---
# <a name="bookmarkonstop-property"></a><span data-ttu-id="b6b8d-103">Proprietà BookmarkOnStop</span><span class="sxs-lookup"><span data-stu-id="b6b8d-103">BookmarkOnStop Property</span></span>

<span data-ttu-id="b6b8d-104">La `DVDAdm.BookmarkOnStop` proprietà imposta o recupera un valore che indica all'oggetto mswebdvd se salvare automaticamente un segnalibro della posizione e delle impostazioni correnti quando l'utente fa clic sul pulsante **Interrompi** .</span><span class="sxs-lookup"><span data-stu-id="b6b8d-104">The `DVDAdm.BookmarkOnStop` property sets or retrieves a value that tells the MSWebDVD object whether to automatically save a bookmark of the current location and settings when the user clicks the **Stop** button.</span></span>

``` syntax
[ bBookmarkOnStop = ] DVD.DVDAdm.BookmarkOnStop
```

## <a name="return-value"></a><span data-ttu-id="b6b8d-105">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b6b8d-105">Return Value</span></span>

<span data-ttu-id="b6b8d-106">Restituisce un valore booleano che indica se l'oggetto MSDVDAdm salverà un segnalibro di tutte le impostazioni DVD, inclusa la posizione sul disco, il livello padre e il paese padre/area geografica.</span><span class="sxs-lookup"><span data-stu-id="b6b8d-106">Returns a Boolean value indicating whether the MSDVDAdm object will save a bookmark of all DVD settings including position on disc, parental level and parental country/region.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6b8d-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="b6b8d-107">Remarks</span></span>

<span data-ttu-id="b6b8d-108">Questa proprietà è di lettura/scrittura e il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="b6b8d-108">This property is read/write with a default value of false.</span></span>

<span data-ttu-id="b6b8d-109">I segnalibri sono validi solo per un computer specifico.</span><span class="sxs-lookup"><span data-stu-id="b6b8d-109">Bookmarks are valid only for a particular machine.</span></span> <span data-ttu-id="b6b8d-110">Un utente non può salvare un segnalibro e quindi inviarlo a un altro utente per leggere in un computer diverso.</span><span class="sxs-lookup"><span data-stu-id="b6b8d-110">A user cannot save a bookmark and then send it to someone else to read on a different machine.</span></span>

## <a name="see-also"></a><span data-ttu-id="b6b8d-111">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b6b8d-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6b8d-112">**BookmarkOnClose**</span><span class="sxs-lookup"><span data-stu-id="b6b8d-112">**BookmarkOnClose**</span></span>](bookmarkonclose-property.md)
</dt> <dt>

[<span data-ttu-id="b6b8d-113">Oggetto MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="b6b8d-113">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



