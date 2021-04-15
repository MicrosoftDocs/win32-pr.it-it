---
description: Consente l'uso di una trasformazione di Media Foundation asincrona (MFT).
ms.assetid: e12ab57e-ebc2-46af-afdf-d78d4db16fcf
title: Attributo MF_TRANSFORM_ASYNC_UNLOCK (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e7876b3f1fca80e881414399d40e69112a64d8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527402"
---
# <a name="mf_transform_async_unlock-attribute"></a><span data-ttu-id="63116-103">Attributo di sblocco di MF \_ Transform \_ Async \_</span><span class="sxs-lookup"><span data-stu-id="63116-103">MF\_TRANSFORM\_ASYNC\_UNLOCK attribute</span></span>

<span data-ttu-id="63116-104">Consente l'uso di una trasformazione di Media Foundation asincrona (MFT).</span><span class="sxs-lookup"><span data-stu-id="63116-104">Enables the use of an asynchronous Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="63116-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="63116-105">Data type</span></span>

<span data-ttu-id="63116-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="63116-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="63116-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="63116-107">Get/set</span></span>

<span data-ttu-id="63116-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="63116-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="63116-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="63116-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="63116-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="63116-110">Remarks</span></span>

<span data-ttu-id="63116-111">MFTs asincroni non sono compatibili con le versioni precedenti di Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="63116-111">Asynchronous MFTs are not compatible with earlier versions of Microsoft Media Foundation.</span></span> <span data-ttu-id="63116-112">Per evitare che le applicazioni esistenti utilizzino accidentalmente un MFT asincrono, questo attributo deve essere impostato su un valore diverso da zero prima di poter utilizzare un MFT asincrono.</span><span class="sxs-lookup"><span data-stu-id="63116-112">To prevent existing applications from accidentally using an asynchronous MFT, this attribute must be set to a nonzero value before an asynchronous MFT can be used.</span></span> <span data-ttu-id="63116-113">La pipeline Media Foundation imposta automaticamente l'attributo, in modo che la maggior parte delle applicazioni non debba utilizzare questo attributo.</span><span class="sxs-lookup"><span data-stu-id="63116-113">The Media Foundation pipeline automatically sets the attribute, so that most applications do not need to use this attribute.</span></span> <span data-ttu-id="63116-114">Tuttavia, se un'applicazione usa una MFT asincrona al di fuori della pipeline di Media Foundation, l'applicazione deve impostare questo attributo.</span><span class="sxs-lookup"><span data-stu-id="63116-114">However, if an application uses an asynchronous MFT outside of the Media Foundation pipeline, the application must set this attribute.</span></span>

<span data-ttu-id="63116-115">MFTs sincroni non richiedono questo attributo.</span><span class="sxs-lookup"><span data-stu-id="63116-115">Synchronous MFTs do not require this attribute.</span></span>

<span data-ttu-id="63116-116">Per verificare se un MFT è asincrono, ottenere il valore dell'attributo [MF \_ Transform \_ Async](mf-transform-async.md) in MFT.</span><span class="sxs-lookup"><span data-stu-id="63116-116">To test whether an MFT is asynchronous, get the value of the [MF\_TRANSFORM\_ASYNC](mf-transform-async.md) attribute on the MFT.</span></span>

## <a name="examples"></a><span data-ttu-id="63116-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="63116-117">Examples</span></span>

<span data-ttu-id="63116-118">Il codice seguente sblocca un MFT asincrono.</span><span class="sxs-lookup"><span data-stu-id="63116-118">The following code unlocks an asynchronous MFT.</span></span>


```C++
HRESULT UnlockAsyncMFT(IMFTransform *pMFT)
{
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = hr = pMFT->GetAttributes(&pAttributes);

    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_TRANSFORM_ASYNC_UNLOCK, TRUE);
        pAttributes->Release();
    }
    
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="63116-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="63116-119">Requirements</span></span>



| <span data-ttu-id="63116-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="63116-120">Requirement</span></span> | <span data-ttu-id="63116-121">Valore</span><span class="sxs-lookup"><span data-stu-id="63116-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="63116-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63116-122">Minimum supported client</span></span><br/> | <span data-ttu-id="63116-123">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="63116-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="63116-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63116-124">Minimum supported server</span></span><br/> | <span data-ttu-id="63116-125">App desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="63116-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="63116-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="63116-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="63116-127"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="63116-127"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63116-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="63116-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63116-129">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="63116-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="63116-130">MFTs asincrono</span><span class="sxs-lookup"><span data-stu-id="63116-130">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> <dt>

[<span data-ttu-id="63116-131">Attributi di trasformazione</span><span class="sxs-lookup"><span data-stu-id="63116-131">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




