---
description: Specifica se una trasformazione Media Foundation (MFT) esegue l'elaborazione asincrona.
ms.assetid: fcc70282-cfac-487c-b9ff-39e62c836f8b
title: Attributo MF_TRANSFORM_ASYNC (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89622bd7bb7fa3e8306c94b02f90217b6367d21b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753151"
---
# <a name="mf_transform_async-attribute"></a><span data-ttu-id="cf100-103">MF \_ Transform ( \_ attributo asincrono)</span><span class="sxs-lookup"><span data-stu-id="cf100-103">MF\_TRANSFORM\_ASYNC attribute</span></span>

<span data-ttu-id="cf100-104">Specifica se una trasformazione Media Foundation (MFT) esegue l'elaborazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="cf100-104">Specifies whether a Media Foundation transform (MFT) performs asynchronous processing.</span></span>

## <a name="data-type"></a><span data-ttu-id="cf100-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="cf100-105">Data type</span></span>

<span data-ttu-id="cf100-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="cf100-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="cf100-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="cf100-107">Get/set</span></span>

<span data-ttu-id="cf100-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="cf100-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="cf100-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="cf100-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="cf100-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="cf100-110">Remarks</span></span>

<span data-ttu-id="cf100-111">L'attributo è un valore booleano:</span><span class="sxs-lookup"><span data-stu-id="cf100-111">The attribute is a Boolean value:</span></span>

-   <span data-ttu-id="cf100-112">Se l'attributo è diverso da zero, il MFT esegue l'elaborazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="cf100-112">If the attribute is nonzero, the MFT performs asynchronous processing.</span></span>
-   <span data-ttu-id="cf100-113">Se l'attributo è 0 o non impostato, il MFT è sincrono.</span><span class="sxs-lookup"><span data-stu-id="cf100-113">If the attribute is 0 or not set, the MFT is synchronous.</span></span>

<span data-ttu-id="cf100-114">Per ottenere questo attributo, chiamare prima [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) per ottenere l'archivio di attributi della MFT.</span><span class="sxs-lookup"><span data-stu-id="cf100-114">To get this attribute, first call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) to get the MFT's attribute store.</span></span> <span data-ttu-id="cf100-115">Se il metodo ha esito positivo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) per ottenere il valore dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="cf100-115">If that method succeeds, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) to get the attribute value.</span></span> <span data-ttu-id="cf100-116">Se uno dei due metodi ha esito negativo, il MFT è sincrono.</span><span class="sxs-lookup"><span data-stu-id="cf100-116">If either of the two methods fails, the MFT is synchronous.</span></span>

<span data-ttu-id="cf100-117">Per MFTs asincrono, questo attributo deve essere impostato su un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="cf100-117">For asynchronous MFTs, this attribute must be set to a nonzero value.</span></span> <span data-ttu-id="cf100-118">Per MFTs sincrono, questo attributo è facoltativo, ma deve essere impostato su 0 se presente.</span><span class="sxs-lookup"><span data-stu-id="cf100-118">For synchronous MFTs, this attribute is optional, but must be set to 0 if present.</span></span>

<span data-ttu-id="cf100-119">MFTs asincroni non sono compatibili con le versioni precedenti di Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="cf100-119">Asynchronous MFTs are not compatible with earlier versions of Media Foundation.</span></span> <span data-ttu-id="cf100-120">Per usare un MFT asincrono, il client deve impostare l'attributo [**MF \_ Transform \_ Async \_ Unlock**](mf-transform-async-unlock.md) in MFT.</span><span class="sxs-lookup"><span data-stu-id="cf100-120">To use an asynchronous MFT, the client must set the [**MF\_TRANSFORM\_ASYNC\_UNLOCK**](mf-transform-async-unlock.md) attribute on the MFT.</span></span> <span data-ttu-id="cf100-121">La pipeline Microsoft Media Foundation esegue questo passaggio automaticamente.</span><span class="sxs-lookup"><span data-stu-id="cf100-121">(The Microsoft Media Foundation pipeline performs this step automatically.)</span></span>

## <a name="examples"></a><span data-ttu-id="cf100-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="cf100-122">Examples</span></span>

<span data-ttu-id="cf100-123">Il codice seguente verifica se un'operazione MFT esegue l'elaborazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="cf100-123">The following code tests whether an MFT performs asynchronous processing.</span></span>


```C++
BOOL IsTransformAsync(IMFTransform *pMFT)
{
    BOOL bAsync = FALSE;
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = pMFT->GetAttributes(&pAttributes);
    if (SUCCEEDED(hr))
    {
        bAsync = MFGetAttributeUINT32(pAttributes, MF_TRANSFORM_ASYNC, FALSE);
        pAttributes->Release();
    }

    return (bAsync != FALSE);
}
```



## <a name="requirements"></a><span data-ttu-id="cf100-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cf100-124">Requirements</span></span>



| <span data-ttu-id="cf100-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf100-125">Requirement</span></span> | <span data-ttu-id="cf100-126">Valore</span><span class="sxs-lookup"><span data-stu-id="cf100-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf100-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cf100-127">Minimum supported client</span></span><br/> | <span data-ttu-id="cf100-128">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="cf100-128">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="cf100-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cf100-129">Minimum supported server</span></span><br/> | <span data-ttu-id="cf100-130">App desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="cf100-130">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="cf100-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cf100-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf100-132"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf100-132"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf100-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cf100-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf100-134">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cf100-134">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="cf100-135">MFTs asincrono</span><span class="sxs-lookup"><span data-stu-id="cf100-135">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> <dt>

[<span data-ttu-id="cf100-136">Attributi di trasformazione</span><span class="sxs-lookup"><span data-stu-id="cf100-136">Transform Attributes</span></span>](transform-attributes.md)
</dt> <dt>

[<span data-ttu-id="cf100-137">**MF \_ trasforma \_ Async \_ sblocco**</span><span class="sxs-lookup"><span data-stu-id="cf100-137">**MF\_TRANSFORM\_ASYNC\_UNLOCK**</span></span>](mf-transform-async-unlock.md)
</dt> </dl>

 

 




