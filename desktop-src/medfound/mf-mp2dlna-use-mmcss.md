---
description: Specifica se il sink di supporto di Digital Living Network Alliance (DLNA) usa il servizio Utilità di pianificazione classi multimediali (MMCSS).
ms.assetid: 4c27e2ec-624a-4b1f-bea9-3aaad1534c9b
title: Attributo MF_MP2DLNA_USE_MMCSS (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccfdaf36ce51f1158e110dcb3682a5b072c060dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050096"
---
# <a name="mf_mp2dlna_use_mmcss-attribute"></a><span data-ttu-id="b72e6-103">MF \_ MP2DLNA \_ usare l' \_ attributo MMCSS</span><span class="sxs-lookup"><span data-stu-id="b72e6-103">MF\_MP2DLNA\_USE\_MMCSS attribute</span></span>

<span data-ttu-id="b72e6-104">Specifica se il sink di supporto di Digital Living Network Alliance (DLNA) usa il servizio Utilità di pianificazione classi multimediali (MMCSS).</span><span class="sxs-lookup"><span data-stu-id="b72e6-104">Specifies whether the Digital Living Network Alliance (DLNA) media sink uses the Multimedia Class Scheduler Service (MMCSS).</span></span>

## <a name="data-type"></a><span data-ttu-id="b72e6-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="b72e6-105">Data type</span></span>

<span data-ttu-id="b72e6-106">**Bool** archiviato come **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b72e6-106">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="b72e6-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="b72e6-107">Get/set</span></span>

<span data-ttu-id="b72e6-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="b72e6-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="b72e6-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="b72e6-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="b72e6-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="b72e6-110">Remarks</span></span>

<span data-ttu-id="b72e6-111">Per impostare questo attributo sul sink multimediale DLNA, eseguire una query sul sink multimediale per l'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="b72e6-111">To set this attribute on the DLNA media sink, query the media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="b72e6-112">Impostare l'attributo prima dell'inizio del flusso.</span><span class="sxs-lookup"><span data-stu-id="b72e6-112">Set the attribute before streaming begins.</span></span>

<span data-ttu-id="b72e6-113">Se questo attributo è **true**, il sink multimediale DLNA si registra con MMCSS.</span><span class="sxs-lookup"><span data-stu-id="b72e6-113">If this attribute is **TRUE**, the DLNA media sink registers itself with MMCSS.</span></span>

## <a name="requirements"></a><span data-ttu-id="b72e6-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b72e6-114">Requirements</span></span>



| <span data-ttu-id="b72e6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b72e6-115">Requirement</span></span> | <span data-ttu-id="b72e6-116">Valore</span><span class="sxs-lookup"><span data-stu-id="b72e6-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b72e6-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b72e6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b72e6-118">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b72e6-118">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b72e6-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b72e6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b72e6-120">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b72e6-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b72e6-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b72e6-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b72e6-122"><dt>Mfmp2dlna. h</dt></span><span class="sxs-lookup"><span data-stu-id="b72e6-122"><dt>Mfmp2dlna.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b72e6-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b72e6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b72e6-124">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b72e6-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




