---
title: DRM_SAPLEVEL (deprecato)
description: Specifica il livello SAP (Secure Audio Path) supportato dall'applicazione.
ms.assetid: a2648083-f9ec-43c7-96c8-4d8b5f8285d1
keywords:
- DRM_SAPLEVEL (obsoleto) formato Windows Media
topic_type:
- apiref
api_name:
- DRM_SAPLEVEL (deprecated)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43711c6c394761f599271809419a46311265d8b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324057"
---
# <a name="drm_saplevel-deprecated"></a><span data-ttu-id="99649-104">DRM \_ SAPLEVEL (deprecato)</span><span class="sxs-lookup"><span data-stu-id="99649-104">DRM\_SAPLEVEL (deprecated)</span></span>

<span data-ttu-id="99649-105">\[**DRM \_ SAPLEVEL** non è più disponibile per l'utilizzo in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="99649-105">\[**DRM\_SAPLEVEL** is no longer available for use as of Windows Vista.</span></span> <span data-ttu-id="99649-106">In alternativa, usare l'audio della modalità utente protetto (PUMA) nella libreria Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="99649-106">Instead, use Protected User Mode Audio (PUMA) in the Media Foundation library.</span></span> <span data-ttu-id="99649-107">\]</span><span class="sxs-lookup"><span data-stu-id="99649-107">\]</span></span>

<span data-ttu-id="99649-108">La proprietà **DRM \_ SAPLEVEL** specifica il livello SAP (Secure Audio Path) supportato dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="99649-108">The **DRM\_SAPLEVEL** property specifies the secure audio path (SAP) level supported by your application.</span></span>

## <a name="global-constant"></a><span data-ttu-id="99649-109">Costante globale</span><span class="sxs-lookup"><span data-stu-id="99649-109">Global Constant</span></span>

<span data-ttu-id="99649-110">g \_ wszWMDRM \_ SAPLEVEL</span><span class="sxs-lookup"><span data-stu-id="99649-110">g\_wszWMDRM\_SAPLEVEL</span></span>

## <a name="data-type"></a><span data-ttu-id="99649-111">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="99649-111">Data Type</span></span>

<span data-ttu-id="99649-112">**\_stringa di tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="99649-112">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="99649-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="99649-113">Remarks</span></span>

<span data-ttu-id="99649-114">Si tratta di una proprietà di sola scrittura impostata chiamando [**IWMDRMReader:: SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="99649-114">This is a write-only property that is set by calling [**IWMDRMReader::SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty).</span></span> <span data-ttu-id="99649-115">Il valore è una rappresentazione di stringa a caratteri wide del livello SAP, ad esempio L "200".</span><span class="sxs-lookup"><span data-stu-id="99649-115">The value is a wide-character string representation of the SAP level, such as L"200".</span></span> <span data-ttu-id="99649-116">I valori correnti supportati sono 200 e 300.</span><span class="sxs-lookup"><span data-stu-id="99649-116">Current supported values are 200 and 300.</span></span>

## <a name="requirements"></a><span data-ttu-id="99649-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="99649-117">Requirements</span></span>



| <span data-ttu-id="99649-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="99649-118">Requirement</span></span> | <span data-ttu-id="99649-119">Valore</span><span class="sxs-lookup"><span data-stu-id="99649-119">Value</span></span> |
|----------------------------------|--------------------------------|
| <span data-ttu-id="99649-120">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="99649-120">End of client support</span></span><br/> | <span data-ttu-id="99649-121">Windows XP</span><span class="sxs-lookup"><span data-stu-id="99649-121">Windows XP</span></span><br/>          |
| <span data-ttu-id="99649-122">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="99649-122">End of server support</span></span><br/> | <span data-ttu-id="99649-123">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="99649-123">Windows Server 2003</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="99649-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="99649-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99649-125">**Proprietà DRM**</span><span class="sxs-lookup"><span data-stu-id="99649-125">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 





