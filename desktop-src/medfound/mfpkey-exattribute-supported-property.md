---
description: Specifica se un Media Foundation Transform (MFT) copia gli attributi dagli esempi di input agli esempi di output.
ms.assetid: 039ecb35-9aa9-4e8a-bbbc-042b9c4c874c
title: Proprietà MFPKEY_EXATTRIBUTE_SUPPORTED (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33017111eba95f54e88671cbcf026b3f40812a08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880805"
---
# <a name="mfpkey_exattribute_supported-property"></a><span data-ttu-id="a9651-103">\_ \_ Proprietà supportata MFPKEY EXATTRIBUTE</span><span class="sxs-lookup"><span data-stu-id="a9651-103">MFPKEY\_EXATTRIBUTE\_SUPPORTED property</span></span>

<span data-ttu-id="a9651-104">Specifica se un Media Foundation Transform (MFT) copia gli attributi dagli esempi di input agli esempi di output.</span><span class="sxs-lookup"><span data-stu-id="a9651-104">Specifies whether a Media Foundation transform (MFT) copies attributes from input samples to output samples.</span></span>



<span data-ttu-id="a9651-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a9651-105">Data type</span></span>

<span data-ttu-id="a9651-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="a9651-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="a9651-107">membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="a9651-107">PROPVARIANT member</span></span>

<span data-ttu-id="a9651-108">**\_bool Variant**</span><span class="sxs-lookup"><span data-stu-id="a9651-108">**VARIANT\_BOOL**</span></span>

<span data-ttu-id="a9651-109">\_bool VT</span><span class="sxs-lookup"><span data-stu-id="a9651-109">VT\_BOOL</span></span>

<span data-ttu-id="a9651-110">**boolVal**</span><span class="sxs-lookup"><span data-stu-id="a9651-110">**boolVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="a9651-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="a9651-111">Remarks</span></span>

<span data-ttu-id="a9651-112">Questo attributo può avere i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="a9651-112">This attribute can have the following values.</span></span>



| <span data-ttu-id="a9651-113">Valore</span><span class="sxs-lookup"><span data-stu-id="a9651-113">Value</span></span>              | <span data-ttu-id="a9651-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9651-114">Description</span></span>                                                                                                                                             |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9651-115">**VARIANT \_ true**</span><span class="sxs-lookup"><span data-stu-id="a9651-115">**VARIANT\_TRUE**</span></span>  | <span data-ttu-id="a9651-116">Il MFT copia gli attributi dagli esempi di input negli esempi di output.</span><span class="sxs-lookup"><span data-stu-id="a9651-116">The MFT copies attributes from the input samples to the output samples.</span></span>                                                                                 |
| <span data-ttu-id="a9651-117">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="a9651-117">**VARIANT\_FALSE**</span></span> | <span data-ttu-id="a9651-118">La sessione multimediale copia gli attributi dagli esempi di input agli esempi di output.</span><span class="sxs-lookup"><span data-stu-id="a9651-118">The Media Session copies attributes from input samples to output samples.</span></span> <span data-ttu-id="a9651-119">Non sovrascrive gli attributi impostati da MFT sugli esempi di output.</span><span class="sxs-lookup"><span data-stu-id="a9651-119">It does not overwrite any attributes that the MFT sets on the output samples.</span></span> |



 

<span data-ttu-id="a9651-120">Per ottenere questo attributo, chiamare **QueryInterface** sulla MFT per l'interfaccia **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="a9651-120">To get this attribute, call **QueryInterface** on the MFT for the **IPropertyStore** interface.</span></span>

<span data-ttu-id="a9651-121">Il valore predefinito è **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="a9651-121">The default value is **VARIANT\_FALSE**.</span></span> <span data-ttu-id="a9651-122">Se MFT non espone l'interfaccia **IPropertyStore** o se questa proprietà non è impostata, trattare il valore come **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="a9651-122">If the MFT does not expose the **IPropertyStore** interface, or if this property is not set, treat the value as **VARIANT\_FALSE**.</span></span>

<span data-ttu-id="a9651-123">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="a9651-123">This property is read-only.</span></span>

> [!NOTE] 
> <span data-ttu-id="a9651-124">Questo attributo non è applicabile a MFTs asincrono.</span><span class="sxs-lookup"><span data-stu-id="a9651-124">This attribute does not apply to asynchronous MFTs.</span></span> <span data-ttu-id="a9651-125">Gli attributi non verranno copiati dagli esempi di input agli esempi di output per MFTs asincroni, indipendentemente dal valore di questo attributo.</span><span class="sxs-lookup"><span data-stu-id="a9651-125">Attributes will not be copied from the input samples to the output samples for asynchronous MFTs, regardless of the value of this attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="a9651-126">Esempio</span><span class="sxs-lookup"><span data-stu-id="a9651-126">Examples</span></span>

<span data-ttu-id="a9651-127">Nell'esempio seguente viene restituito VARIANT \_ true se una MFT copia gli attributi di esempio.</span><span class="sxs-lookup"><span data-stu-id="a9651-127">The following example returns VARIANT\_TRUE if an MFT copies sample attributes.</span></span>


```C++
BOOL TransformCopiesSampleAttributes(IMFTransform *pMFT)
{
    BOOL bCopiesAttributes = FALSE;

    IPropertyStore *pProps = NULL;

    HRESULT hr = pMFT->QueryInterface(IID_PPV_ARGS(&pProps));
    
    if (SUCCEEDED(hr))
    {
        PROPVARIANT var;
        hr = pProps->GetValue(MFPKEY_EXATTRIBUTE_SUPPORTED, &var);

        if (SUCCEEDED(hr))
        {
            bCopiesAttributes = 
                (var.vt == VT_BOOL && var.boolVal == VARIANT_TRUE);

            PropVariantClear(&var);
        }
        pProps->Release();
    }
    return bCopiesAttributes;
}
```



## <a name="requirements"></a><span data-ttu-id="a9651-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a9651-128">Requirements</span></span>



| <span data-ttu-id="a9651-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9651-129">Requirement</span></span> | <span data-ttu-id="a9651-130">Valore</span><span class="sxs-lookup"><span data-stu-id="a9651-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9651-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9651-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a9651-132">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a9651-132">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a9651-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9651-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a9651-134">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a9651-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a9651-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a9651-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9651-136"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9651-136"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9651-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a9651-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9651-138">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a9651-138">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="a9651-139">Attributi di esempio</span><span class="sxs-lookup"><span data-stu-id="a9651-139">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="a9651-140">**IMFTransform::P rocessOutput**</span><span class="sxs-lookup"><span data-stu-id="a9651-140">**IMFTransform::ProcessOutput**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)
</dt> </dl>

 

 




