---
description: Indica se un flusso contiene contenuto protetto.
ms.assetid: 1c1a201c-4b55-4b86-a08f-d06c1a7db29d
title: Attributo MF_SD_PROTECTED (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c97320d15353b8e23a43fa4efac2e5883a7366f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318414"
---
# <a name="mf_sd_protected-attribute"></a><span data-ttu-id="ffb7e-103">\_ \_ Attributo protetto MF SD</span><span class="sxs-lookup"><span data-stu-id="ffb7e-103">MF\_SD\_PROTECTED attribute</span></span>

<span data-ttu-id="ffb7e-104">Indica se un flusso contiene contenuto protetto.</span><span class="sxs-lookup"><span data-stu-id="ffb7e-104">Indicates whether a stream contains protected content.</span></span>

## <a name="data-type"></a><span data-ttu-id="ffb7e-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="ffb7e-105">Data type</span></span>

<span data-ttu-id="ffb7e-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="ffb7e-106">**UINT32**</span></span>

<span data-ttu-id="ffb7e-107">Considera come valore booleano.</span><span class="sxs-lookup"><span data-stu-id="ffb7e-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffb7e-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="ffb7e-108">Remarks</span></span>

<span data-ttu-id="ffb7e-109">Questo attributo si applica ai descrittori di flusso.</span><span class="sxs-lookup"><span data-stu-id="ffb7e-109">This attribute applies to stream descriptors.</span></span> <span data-ttu-id="ffb7e-110">Se il valore dell'attributo è **true**, il flusso contiene contenuto protetto.</span><span class="sxs-lookup"><span data-stu-id="ffb7e-110">If the value of the attribute is **TRUE**, the stream contains protected content.</span></span> <span data-ttu-id="ffb7e-111">Se il valore è **false** o l'attributo non è impostato, il flusso contiene contenuto non crittografato.</span><span class="sxs-lookup"><span data-stu-id="ffb7e-111">If the value is **FALSE**, or the attribute is not set, the stream contains clear content.</span></span>

<span data-ttu-id="ffb7e-112">Anziché controllare ogni flusso per questo attributo, è possibile passare un descrittore di presentazione alla funzione [**MFRequireProtectedEnvironment**](/windows/desktop/api/mfidl/nf-mfidl-mfrequireprotectedenvironment) .</span><span class="sxs-lookup"><span data-stu-id="ffb7e-112">Instead of checking each stream for this attribute, you can pass a presentation descriptor to the [**MFRequireProtectedEnvironment**](/windows/desktop/api/mfidl/nf-mfidl-mfrequireprotectedenvironment) function.</span></span> <span data-ttu-id="ffb7e-113">Questa funzione verifica se il descrittore della presentazione contiene flussi protetti.</span><span class="sxs-lookup"><span data-stu-id="ffb7e-113">This function tests whether the presentation descriptor contains any protected streams.</span></span>

<span data-ttu-id="ffb7e-114">Un'origine multimediale deve impostare questo attributo sul descrittore del flusso se il contenuto richiede il percorso del supporto protetto (PMP).</span><span class="sxs-lookup"><span data-stu-id="ffb7e-114">A media source should set this attribute on the stream descriptor if the content requires the protected media path (PMP).</span></span>

<span data-ttu-id="ffb7e-115">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="ffb7e-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="ffb7e-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="ffb7e-116">Examples</span></span>


```
// This function returns TRUE if the stream contains protected 
// content. You can also call the MFRequireProtectedEnvironment 
// function to test whether a presentation contains any streams
// with protected content.

BOOL StreamHasProtectedContent(IMFStreamDescriptor *pSD)
{
    return MFGetAttributeUINT32(pSD, MF_SD_PROTECTED, FALSE);
}
```



## <a name="requirements"></a><span data-ttu-id="ffb7e-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ffb7e-117">Requirements</span></span>



| <span data-ttu-id="ffb7e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ffb7e-118">Requirement</span></span> | <span data-ttu-id="ffb7e-119">Valore</span><span class="sxs-lookup"><span data-stu-id="ffb7e-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ffb7e-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ffb7e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ffb7e-121">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="ffb7e-121">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="ffb7e-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ffb7e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ffb7e-123">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="ffb7e-123">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="ffb7e-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ffb7e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ffb7e-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ffb7e-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffb7e-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ffb7e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffb7e-127">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ffb7e-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ffb7e-128">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="ffb7e-128">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="ffb7e-129">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="ffb7e-129">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="ffb7e-130">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="ffb7e-130">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="ffb7e-131">Attributi del descrittore di flusso</span><span class="sxs-lookup"><span data-stu-id="ffb7e-131">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> </dl>

 

 




