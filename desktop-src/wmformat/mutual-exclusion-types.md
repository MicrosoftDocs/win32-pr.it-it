---
title: Tipi di esclusione reciproca
description: Tipi di esclusione reciproca
ms.assetid: bfe6cfe6-3df4-49c4-8015-fe4479b693c1
keywords:
- Windows Media Format SDK, esclusione reciproca
- Formato di sistemi avanzati (ASF), esclusione reciproca
- ASF (formato avanzato dei sistemi), esclusione reciproca
- esclusione reciproca, tipi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c425e69c2aa3eac012874837a6970dbc26d1a51
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046268"
---
# <a name="mutual-exclusion-types"></a><span data-ttu-id="99340-107">Tipi di esclusione reciproca</span><span class="sxs-lookup"><span data-stu-id="99340-107">Mutual Exclusion Types</span></span>

<span data-ttu-id="99340-108">È possibile utilizzare i tipi di esclusione reciproca per identificare la natura di un oggetto di esclusione reciproca in un profilo.</span><span class="sxs-lookup"><span data-stu-id="99340-108">You can use mutual exclusion types to identify the nature of a mutual exclusion object in a profile.</span></span> <span data-ttu-id="99340-109">I tipi di esclusione reciproca vengono usati come parametri per [**IWMMutualExclusion:: GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-gettype) e [**IWMMutualExclusion:: seTYPE**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype).</span><span class="sxs-lookup"><span data-stu-id="99340-109">Mutual exclusion types are used as parameters for [**IWMMutualExclusion::GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-gettype) and [**IWMMutualExclusion::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype).</span></span>

<span data-ttu-id="99340-110">Nella tabella seguente sono elencati gli identificatori per i tipi di esclusione reciproca.</span><span class="sxs-lookup"><span data-stu-id="99340-110">The following table lists the identifiers for mutual exclusion types.</span></span>



| <span data-ttu-id="99340-111">Costante tipo di esclusione reciproca</span><span class="sxs-lookup"><span data-stu-id="99340-111">Mutual exclusion type constant</span></span> | <span data-ttu-id="99340-112">GUID</span><span class="sxs-lookup"><span data-stu-id="99340-112">GUID</span></span>                                 |
|--------------------------------|--------------------------------------|
| <span data-ttu-id="99340-113">\_Lingua WMMUTEX \_ CLSID</span><span class="sxs-lookup"><span data-stu-id="99340-113">CLSID\_WMMUTEX\_Language</span></span>       | <span data-ttu-id="99340-114">D6E22A00-35DA-11D1-9034-00A0C90349BE</span><span class="sxs-lookup"><span data-stu-id="99340-114">D6E22A00-35DA-11D1-9034-00A0C90349BE</span></span> |
| <span data-ttu-id="99340-115">\_ \_ Bitrate WMMUTEX CLSID</span><span class="sxs-lookup"><span data-stu-id="99340-115">CLSID\_WMMUTEX\_Bitrate</span></span>        | <span data-ttu-id="99340-116">D6E22A01-35DA-11D1-9034-00A0C90349BE</span><span class="sxs-lookup"><span data-stu-id="99340-116">D6E22A01-35DA-11D1-9034-00A0C90349BE</span></span> |
| <span data-ttu-id="99340-117">\_Presentazione WMMUTEX \_ CLSID</span><span class="sxs-lookup"><span data-stu-id="99340-117">CLSID\_WMMUTEX\_Presentation</span></span>   | <span data-ttu-id="99340-118">D6E22A02-35DA-11D1-9034-00A0C90349BE</span><span class="sxs-lookup"><span data-stu-id="99340-118">D6E22A02-35DA-11D1-9034-00A0C90349BE</span></span> |
| <span data-ttu-id="99340-119">CLSID \_ WMMUTEX \_ sconosciuto</span><span class="sxs-lookup"><span data-stu-id="99340-119">CLSID\_WMMUTEX\_Unknown</span></span>        | <span data-ttu-id="99340-120">D6E22A03-35DA-11D1-9034-00A0C90349BE</span><span class="sxs-lookup"><span data-stu-id="99340-120">D6E22A03-35DA-11D1-9034-00A0C90349BE</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="99340-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="99340-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99340-122">**Valori GUID**</span><span class="sxs-lookup"><span data-stu-id="99340-122">**GUID Values**</span></span>](guid-values.md)
</dt> </dl>

 

 




