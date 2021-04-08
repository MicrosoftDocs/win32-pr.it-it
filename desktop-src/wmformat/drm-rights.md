---
title: DRM_Rights
description: La \_ Proprietà diritti DRM specifica i diritti che l'applicazione richiederà nel tentativo successivo di aprire un file protetto.
ms.assetid: fbf62e8d-069e-427b-9093-6c579cdaa96a
keywords:
- DRM_Rights formato Windows Media
topic_type:
- apiref
api_name:
- DRM_Rights
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 542e511c11111bb2698d9c936a1f0973a2145c9b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046288"
---
# <a name="drm_rights"></a><span data-ttu-id="9c9b2-104">\_Diritti DRM</span><span class="sxs-lookup"><span data-stu-id="9c9b2-104">DRM\_Rights</span></span>

<span data-ttu-id="9c9b2-105">La **proprietà \_ diritti DRM** specifica i diritti che l'applicazione richiederà nel tentativo successivo di aprire un file protetto.</span><span class="sxs-lookup"><span data-stu-id="9c9b2-105">The **DRM\_Rights** property specifies the rights that the application will require in the next attempt to open a protected file.</span></span>

## <a name="global-constant"></a><span data-ttu-id="9c9b2-106">Costante globale</span><span class="sxs-lookup"><span data-stu-id="9c9b2-106">Global Constant</span></span>

<span data-ttu-id="9c9b2-107">\_diritti g wszWMDRM \_</span><span class="sxs-lookup"><span data-stu-id="9c9b2-107">g\_wszWMDRM\_Rights</span></span>

## <a name="data-type"></a><span data-ttu-id="9c9b2-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="9c9b2-108">Data Type</span></span>

<span data-ttu-id="9c9b2-109">**\_stringa di tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="9c9b2-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="9c9b2-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="9c9b2-110">Remarks</span></span>

<span data-ttu-id="9c9b2-111">Si tratta di una proprietà di lettura/scrittura che viene recuperata utilizzando [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) e impostata utilizzando [**IWMDRMReader:: SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty) o [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).</span><span class="sxs-lookup"><span data-stu-id="9c9b2-111">This is a read-write property that is retrieved using [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) and set using either [**IWMDRMReader::SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty) or [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).</span></span>

<span data-ttu-id="9c9b2-112">Nella tabella seguente sono elencati i diritti supportati.</span><span class="sxs-lookup"><span data-stu-id="9c9b2-112">The following table lists the supported rights.</span></span>



| <span data-ttu-id="9c9b2-113">Destra</span><span class="sxs-lookup"><span data-stu-id="9c9b2-113">Right</span></span>                                           | <span data-ttu-id="9c9b2-114">Valore letterale stringa</span><span class="sxs-lookup"><span data-stu-id="9c9b2-114">String literal</span></span>      | <span data-ttu-id="9c9b2-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9c9b2-115">Description</span></span>                                                                                                                                                                                                          |
|-------------------------------------------------|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c9b2-116">g \_ wszWMDRM \_ right \_ backup</span><span class="sxs-lookup"><span data-stu-id="9c9b2-116">g\_wszWMDRM\_RIGHT\_BACKUP</span></span>                      | <span data-ttu-id="9c9b2-117">Backup</span><span class="sxs-lookup"><span data-stu-id="9c9b2-117">"Backup"</span></span>            | <span data-ttu-id="9c9b2-118">Diritto di eseguire il backup della licenza.</span><span class="sxs-lookup"><span data-stu-id="9c9b2-118">Right to back up the license.</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="9c9b2-119">g \_ wszWMDRM \_ right \_ collaborative \_ Play</span><span class="sxs-lookup"><span data-stu-id="9c9b2-119">g\_wszWMDRM\_RIGHT\_COLLABORATIVE\_PLAY</span></span>         | <span data-ttu-id="9c9b2-120">"CollaborativePlay"</span><span class="sxs-lookup"><span data-stu-id="9c9b2-120">"CollaborativePlay"</span></span> | <span data-ttu-id="9c9b2-121">Diritto di riprodurre il file come parte di una playlist collaborativa.</span><span class="sxs-lookup"><span data-stu-id="9c9b2-121">Right to play the file as part of a collaborative playlist.</span></span>                                                                                                                                                          |
| <span data-ttu-id="9c9b2-122">g \_ wszWMDRM \_ \_ copia destra</span><span class="sxs-lookup"><span data-stu-id="9c9b2-122">g\_wszWMDRM\_RIGHT\_COPY</span></span>                        | <span data-ttu-id="9c9b2-123">"Copy"</span><span class="sxs-lookup"><span data-stu-id="9c9b2-123">"Copy"</span></span>              | <span data-ttu-id="9c9b2-124">Diritto di copiare il file in un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9c9b2-124">Right to copy the file to a device.</span></span> <span data-ttu-id="9c9b2-125">Questo diritto sostituisce i precedenti diritti di copia (g \_ wszWMDRM \_ right \_ copy \_ to \_ CD, g \_ wszWMDRM \_ right \_ copy \_ to \_ non \_ SDMI \_ Device e g \_ wszWMDRM \_ right copy \_ \_ to \_ SDMI \_ Device).</span><span class="sxs-lookup"><span data-stu-id="9c9b2-125">This right supersedes the older copy rights (g\_wszWMDRM\_RIGHT\_COPY\_TO\_CD, g\_wszWMDRM\_RIGHT\_COPY\_TO\_NON\_SDMI\_DEVICE, and g\_wszWMDRM\_RIGHT\_COPY\_TO\_SDMI\_DEVICE).</span></span> |
| <span data-ttu-id="9c9b2-126">g \_ wszWMDRM \_ la \_ copia corretta \_ su \_ CD</span><span class="sxs-lookup"><span data-stu-id="9c9b2-126">g\_wszWMDRM\_RIGHT\_COPY\_TO\_CD</span></span>                | <span data-ttu-id="9c9b2-127">"Print. Redbook"</span><span class="sxs-lookup"><span data-stu-id="9c9b2-127">"Print.redbook"</span></span>     | <span data-ttu-id="9c9b2-128">Diritto di copiare il file in un CD (formato di libro rosso). In Windows Media DRM 10, questo diritto viene sostituito da g \_ wszWMDRM \_ right \_ Copy.</span><span class="sxs-lookup"><span data-stu-id="9c9b2-128">Right to copy the file to a CD (Red Book format).In Windows Media DRM 10, this right is replaced by g\_wszWMDRM\_RIGHT\_COPY.</span></span><br/>                                                                             |
| <span data-ttu-id="9c9b2-129">g \_ wszWMDRM \_ la \_ copia destra \_ in un \_ \_ dispositivo non SDMI \_</span><span class="sxs-lookup"><span data-stu-id="9c9b2-129">g\_wszWMDRM\_RIGHT\_COPY\_TO\_NON\_SDMI\_DEVICE</span></span> | <span data-ttu-id="9c9b2-130">"Transfer. NONSDMI"</span><span class="sxs-lookup"><span data-stu-id="9c9b2-130">"Transfer.NONSDMI"</span></span>  | <span data-ttu-id="9c9b2-131">Diritto di copiare il file in un dispositivo non SDMI. In Windows Media DRM 10, questo diritto viene sostituito da g \_ wszWMDRM \_ right \_ Copy.</span><span class="sxs-lookup"><span data-stu-id="9c9b2-131">Right to copy the file to a non-SDMI device.In Windows Media DRM 10, this right is replaced by g\_wszWMDRM\_RIGHT\_COPY.</span></span><br/>                                                                                  |
| <span data-ttu-id="9c9b2-132">g \_ wszWMDRM \_ la \_ Copia \_ destra \_ nel \_ dispositivo SDMI</span><span class="sxs-lookup"><span data-stu-id="9c9b2-132">g\_wszWMDRM\_RIGHT\_COPY\_TO\_SDMI\_DEVICE</span></span>      | <span data-ttu-id="9c9b2-133">"Transfer. SDMI"</span><span class="sxs-lookup"><span data-stu-id="9c9b2-133">"Transfer.SDMI"</span></span>     | <span data-ttu-id="9c9b2-134">Diritto di copiare il file in un dispositivo conforme a SDMI. In Windows Media DRM 10, questo diritto viene sostituito da g \_ wszWMDRM \_ right \_ Copy.</span><span class="sxs-lookup"><span data-stu-id="9c9b2-134">Right to copy the file to an SDMI-compliant device.In Windows Media DRM 10, this right is replaced by g\_wszWMDRM\_RIGHT\_COPY.</span></span><br/>                                                                           |
| <span data-ttu-id="9c9b2-135">g \_ wszWMDRM \_ riproduzione a destra \_</span><span class="sxs-lookup"><span data-stu-id="9c9b2-135">g\_wszWMDRM\_RIGHT\_PLAYBACK</span></span>                    | <span data-ttu-id="9c9b2-136">Play</span><span class="sxs-lookup"><span data-stu-id="9c9b2-136">"Play"</span></span>              | <span data-ttu-id="9c9b2-137">Diritto di riprodurre il file multimediale.</span><span class="sxs-lookup"><span data-stu-id="9c9b2-137">Right to play the media file.</span></span>                                                                                                                                                                                        |



 

<span data-ttu-id="9c9b2-138">Questa proprietà contiene una stringa di caratteri wide di uno o più diritti separati da punti e virgola, ad esempio: L "playback; Copia CollaborativePlay".</span><span class="sxs-lookup"><span data-stu-id="9c9b2-138">This property contains a wide-character string of one or more rights separated by semicolons, for example: L"Playback;Copy;CollaborativePlay".</span></span>

## <a name="see-also"></a><span data-ttu-id="9c9b2-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9c9b2-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c9b2-140">**Proprietà DRM**</span><span class="sxs-lookup"><span data-stu-id="9c9b2-140">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 





