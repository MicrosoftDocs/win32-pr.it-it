---
description: Indica se un campione è un punto di accesso casuale.
ms.assetid: 03d4bfd8-1148-4551-8e71-05cfba2e15fa
title: Attributo MFSampleExtension_CleanPoint (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a54ea9bf4f1ca207a6ab12bac331c57db63136a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527948"
---
# <a name="mfsampleextension_cleanpoint-attribute"></a><span data-ttu-id="774d9-103">\_Attributo CleanPoint di MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="774d9-103">MFSampleExtension\_CleanPoint attribute</span></span>

<span data-ttu-id="774d9-104">Indica se un campione è un punto di accesso casuale.</span><span class="sxs-lookup"><span data-stu-id="774d9-104">Indicates whether a sample is a random access point.</span></span>

## <a name="data-type"></a><span data-ttu-id="774d9-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="774d9-105">Data type</span></span>

<span data-ttu-id="774d9-106">**Bool** archiviato come **UInt32**</span><span class="sxs-lookup"><span data-stu-id="774d9-106">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="774d9-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="774d9-107">Get/set</span></span>

<span data-ttu-id="774d9-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="774d9-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="774d9-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="774d9-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="774d9-110">Si applica a</span><span class="sxs-lookup"><span data-stu-id="774d9-110">Applies to</span></span>

[<span data-ttu-id="774d9-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="774d9-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="774d9-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="774d9-112">Remarks</span></span>

<span data-ttu-id="774d9-113">Questo attributo si applica agli esempi.</span><span class="sxs-lookup"><span data-stu-id="774d9-113">This attribute applies to samples.</span></span> <span data-ttu-id="774d9-114">Se l'attributo è **true**, l'esempio è un punto di accesso casuale e la decodifica può iniziare da questo esempio.</span><span class="sxs-lookup"><span data-stu-id="774d9-114">If the attribute is **TRUE**, the sample is a random access point and decoding can begin from this sample.</span></span> <span data-ttu-id="774d9-115">In caso contrario, l'esempio non è un punto di accesso casuale.</span><span class="sxs-lookup"><span data-stu-id="774d9-115">Otherwise, the sample is not a random access point.</span></span>

<span data-ttu-id="774d9-116">Se questo attributo non è impostato, il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="774d9-116">If this attribute is not set, the default value is **FALSE**.</span></span>

<span data-ttu-id="774d9-117">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="774d9-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="774d9-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="774d9-118">Examples</span></span>


```C++
inline BOOL IsRandomAccessPoint(IMFSample *pSample)
{
    // Check for the "clean point" attribute. Default to FALSE.
    return MFGetAttributeUINT32(pSample, MFSampleExtension_CleanPoint, FALSE);
}
```



## <a name="requirements"></a><span data-ttu-id="774d9-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="774d9-119">Requirements</span></span>



| <span data-ttu-id="774d9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="774d9-120">Requirement</span></span> | <span data-ttu-id="774d9-121">Valore</span><span class="sxs-lookup"><span data-stu-id="774d9-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="774d9-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="774d9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="774d9-123">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="774d9-123">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="774d9-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="774d9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="774d9-125">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="774d9-125">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="774d9-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="774d9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="774d9-127"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="774d9-127"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="774d9-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="774d9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="774d9-129">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="774d9-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="774d9-130">Attributi di esempio</span><span class="sxs-lookup"><span data-stu-id="774d9-130">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="774d9-131">Esempi di supporti</span><span class="sxs-lookup"><span data-stu-id="774d9-131">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 




