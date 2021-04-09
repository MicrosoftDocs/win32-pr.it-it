---
description: Contiene i nomi descrittivi degli stili SAMI (Synchronized Media Interchange) definiti nel file SAMI.
ms.assetid: bc679f0e-17f6-455c-8a00-1d435538ef86
title: Attributo MF_PD_SAMI_STYLELIST (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebb07dd1713faa81fd02bfe7a32c81398cddb736
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885190"
---
# <a name="mf_pd_sami_stylelist-attribute"></a><span data-ttu-id="9fb8f-103">Attributo di stile dell'aspetto di MF \_ PD \_ Sami \_</span><span class="sxs-lookup"><span data-stu-id="9fb8f-103">MF\_PD\_SAMI\_STYLELIST attribute</span></span>

<span data-ttu-id="9fb8f-104">Contiene i nomi descrittivi degli stili SAMI (Synchronized Media Interchange) definiti nel file SAMI.</span><span class="sxs-lookup"><span data-stu-id="9fb8f-104">Contains the friendly names of the Synchronized Accessible Media Interchange (SAMI) styles defined in the SAMI file.</span></span>

<span data-ttu-id="9fb8f-105">L' [origine dei supporti Sami](sami-media-source.md) imposta questo attributo sul descrittore della presentazione che crea.</span><span class="sxs-lookup"><span data-stu-id="9fb8f-105">The [SAMI Media Source](sami-media-source.md) sets this attribute on the presentation descriptor that it creates.</span></span>

## <a name="data-type"></a><span data-ttu-id="9fb8f-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="9fb8f-106">Data type</span></span>

<span data-ttu-id="9fb8f-107">Matrice di byte</span><span class="sxs-lookup"><span data-stu-id="9fb8f-107">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="9fb8f-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="9fb8f-108">Remarks</span></span>

<span data-ttu-id="9fb8f-109">Il BLOB dell'attributo presenta la struttura seguente:</span><span class="sxs-lookup"><span data-stu-id="9fb8f-109">The attribute blob has the following structure:</span></span>



<span data-ttu-id="9fb8f-110">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="9fb8f-110">Data Type</span></span>

<span data-ttu-id="9fb8f-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9fb8f-111">Description</span></span>

<span data-ttu-id="9fb8f-112">Dimensioni (byte)</span><span class="sxs-lookup"><span data-stu-id="9fb8f-112">Size (bytes)</span></span>

<span data-ttu-id="9fb8f-113">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="9fb8f-113">**DWORD**</span></span>

<span data-ttu-id="9fb8f-114">Numero di stringhe di stile.</span><span class="sxs-lookup"><span data-stu-id="9fb8f-114">Number of style strings.</span></span>

<span data-ttu-id="9fb8f-115">4</span><span class="sxs-lookup"><span data-stu-id="9fb8f-115">4</span></span>

<span data-ttu-id="9fb8f-116">Per ogni stringa di stile:</span><span class="sxs-lookup"><span data-stu-id="9fb8f-116">For each style string:</span></span>

<span data-ttu-id="9fb8f-117">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="9fb8f-117">**DWORD**</span></span>

<span data-ttu-id="9fb8f-118">Dimensioni in byte della stringa, incluso il carattere **null** .</span><span class="sxs-lookup"><span data-stu-id="9fb8f-118">Size of the string in bytes, including the **NULL** character.</span></span>

<span data-ttu-id="9fb8f-119">4</span><span class="sxs-lookup"><span data-stu-id="9fb8f-119">4</span></span>

<span data-ttu-id="9fb8f-120">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="9fb8f-120">**LPWSTR**</span></span>

<span data-ttu-id="9fb8f-121">Stringa di caratteri wide con terminazione null contenente il nome dello stile.</span><span class="sxs-lookup"><span data-stu-id="9fb8f-121">Null-terminated wide-character string containing the name of the style.</span></span>

<span data-ttu-id="9fb8f-122">Varia</span><span class="sxs-lookup"><span data-stu-id="9fb8f-122">Varies</span></span>



 

<span data-ttu-id="9fb8f-123">Per impostare lo stile o recuperare lo stile corrente, utilizzare l'interfaccia [**IMFSAMIStyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle) .</span><span class="sxs-lookup"><span data-stu-id="9fb8f-123">To set the style or retrieve the current style, use the [**IMFSAMIStyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle) interface.</span></span>

<span data-ttu-id="9fb8f-124">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="9fb8f-124">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="9fb8f-125">Esempio</span><span class="sxs-lookup"><span data-stu-id="9fb8f-125">Examples</span></span>


```C++
HRESULT DisplaySAMIStyleNames(IMFPresentationDescriptor *pPD)
{
    UINT8 *pBuf = NULL;
    UINT32 cbBuf = 0;

    HRESULT hr = pPD->GetAllocatedBlob(MF_PD_SAMI_STYLELIST, &pBuf, &cbBuf);

    if (SUCCEEDED(hr))
    {

        DWORD cStyles = ((DWORD*)pBuf)[0];
        UINT8 *pStrings = pBuf + sizeof(DWORD);

        for (DWORD i = 0; i < cStyles; i++)
        {
            DWORD cbString = ((DWORD*)pStrings)[0];
            pStrings += sizeof(DWORD);

            wprintf_s(L"%s\n", (WCHAR*)pStrings);

            pStrings += cbString;
        }
    }
    CoTaskMemFree(pBuf);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="9fb8f-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9fb8f-126">Requirements</span></span>



| <span data-ttu-id="9fb8f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fb8f-127">Requirement</span></span> | <span data-ttu-id="9fb8f-128">Valore</span><span class="sxs-lookup"><span data-stu-id="9fb8f-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9fb8f-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9fb8f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9fb8f-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9fb8f-130">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9fb8f-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9fb8f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9fb8f-132">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9fb8f-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9fb8f-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9fb8f-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="9fb8f-134"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fb8f-134"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fb8f-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9fb8f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fb8f-136">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9fb8f-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9fb8f-137">**IMFAttributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="9fb8f-137">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="9fb8f-138">**IMFAttributes:: seblob**</span><span class="sxs-lookup"><span data-stu-id="9fb8f-138">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="9fb8f-139">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="9fb8f-139">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="9fb8f-140">Attributi del descrittore della presentazione</span><span class="sxs-lookup"><span data-stu-id="9fb8f-140">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="9fb8f-141">Origine supporto SAMI</span><span class="sxs-lookup"><span data-stu-id="9fb8f-141">SAMI Media Source</span></span>](sami-media-source.md)
</dt> </dl>

 

 




