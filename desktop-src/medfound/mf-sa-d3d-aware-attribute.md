---
description: Specifica se una trasformazione Media Foundation (MFT) supporta l'accelerazione video DirectX (DXVA). Questo attributo si applica solo ai video MFTs.
ms.assetid: db6a8b20-fda0-4ffe-b1b5-a77b7604d290
title: Attributo MF_SA_D3D_AWARE (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eb0de8c5a66eaa89f66becf6770f69e6449c1c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314539"
---
# <a name="mf_sa_d3d_aware-attribute"></a><span data-ttu-id="67e63-104">\_Attributo in \_ grado di \_ riconoscere D3D per MF SA</span><span class="sxs-lookup"><span data-stu-id="67e63-104">MF\_SA\_D3D\_AWARE attribute</span></span>

<span data-ttu-id="67e63-105">Specifica se una trasformazione Media Foundation (MFT) supporta l'accelerazione video DirectX (DXVA).</span><span class="sxs-lookup"><span data-stu-id="67e63-105">Specifies whether a Media Foundation transform (MFT) supports DirectX Video Acceleration (DXVA).</span></span> <span data-ttu-id="67e63-106">Questo attributo si applica solo ai video MFTs.</span><span class="sxs-lookup"><span data-stu-id="67e63-106">This attribute applies only to video MFTs.</span></span>

## <a name="data-type"></a><span data-ttu-id="67e63-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="67e63-107">Data type</span></span>

<span data-ttu-id="67e63-108">**Bool** archiviato come **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67e63-108">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="67e63-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="67e63-109">Remarks</span></span>

<span data-ttu-id="67e63-110">Per eseguire una query su questo attributo, chiamare [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) per ottenere l'archivio di attributi globale di MFT.</span><span class="sxs-lookup"><span data-stu-id="67e63-110">To query this attribute, call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) to get the global attribute store of the MFT.</span></span> <span data-ttu-id="67e63-111">Se **GetAttributes** ha esito positivo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="67e63-111">If **GetAttributes** succeeds, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="67e63-112">Questo attributo indica al client se MFT può usare il video Direct3D 9:</span><span class="sxs-lookup"><span data-stu-id="67e63-112">This attribute tells the client whether the MFT can use Direct3D 9 video:</span></span>

-   <span data-ttu-id="67e63-113">Se l'attributo è diverso da zero, il client può assegnare a MFT un puntatore all'interfaccia [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) prima dell'avvio del flusso.</span><span class="sxs-lookup"><span data-stu-id="67e63-113">If the attribute is nonzero, the client can give the MFT a pointer to the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface before streaming starts.</span></span> <span data-ttu-id="67e63-114">A tale scopo, il client invia il messaggio di [**\_ \_ \_ \_ gestione D3D message set D3D**](mft-message-set-d3d-manager.md) al MFT.</span><span class="sxs-lookup"><span data-stu-id="67e63-114">To do so, the client sends the [**MFT\_MESSAGE\_SET\_D3D\_MANAGER**](mft-message-set-d3d-manager.md) message to the MFT.</span></span> <span data-ttu-id="67e63-115">Il client non è necessario per l'invio di questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="67e63-115">The client is not required to send this message.</span></span>
-   <span data-ttu-id="67e63-116">Se questo attributo è zero (**false**), MFT non supporta il video Direct3D 9 e il client non deve inviare il messaggio [**MFT \_ message set \_ di \_ \_ gestione D3D**](mft-message-set-d3d-manager.md) al MFT.</span><span class="sxs-lookup"><span data-stu-id="67e63-116">If this attribute is zero (**FALSE**), the MFT does not support Direct3D 9 video, and the client should not send the [**MFT\_MESSAGE\_SET\_D3D\_MANAGER**](mft-message-set-d3d-manager.md) message to the MFT.</span></span>

<span data-ttu-id="67e63-117">Il valore predefinito di questo attributo è **false**.</span><span class="sxs-lookup"><span data-stu-id="67e63-117">The default value of this attribute is **FALSE**.</span></span> <span data-ttu-id="67e63-118">Considerare questo attributo come di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="67e63-118">Treat this attribute as read-only.</span></span> <span data-ttu-id="67e63-119">Non modificare il valore. il MFT ignorerà tutte le modifiche apportate al valore.</span><span class="sxs-lookup"><span data-stu-id="67e63-119">Do not change the value; the MFT will ignore any changes to the value.</span></span>

<span data-ttu-id="67e63-120">Per altre informazioni sull'implementazione di questo attributo in un MFT personalizzato, vedere [MFTS compatibile con Direct3D](direct3d-aware-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="67e63-120">For more information about implementing this attribute in a custom MFT, see [Direct3D-Aware MFTs](direct3d-aware-mfts.md).</span></span>

<span data-ttu-id="67e63-121">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="67e63-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="67e63-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="67e63-122">Examples</span></span>

<span data-ttu-id="67e63-123">Il codice seguente verifica se un MFT supporta DXVA.</span><span class="sxs-lookup"><span data-stu-id="67e63-123">The following code tests whether an MFT supports DXVA.</span></span>


```C++
// Returns TRUE is an MFT supports DirectX Video Acceleration.

BOOL IsTransformD3DAware(IMFTransform *pMFT)
{
    BOOL bD3DAware = FALSE;
    
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = pMFT->GetAttributes(&pAttributes);
    if (SUCCEEDED(hr))
    {
        bD3DAware = MFGetAttributeUINT32(pAttributes, MF_SA_D3D_AWARE, FALSE);
        pAttributes->Release();
    }
    return bD3DAware;
}
```



## <a name="requirements"></a><span data-ttu-id="67e63-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="67e63-124">Requirements</span></span>



| <span data-ttu-id="67e63-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="67e63-125">Requirement</span></span> | <span data-ttu-id="67e63-126">Valore</span><span class="sxs-lookup"><span data-stu-id="67e63-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="67e63-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="67e63-127">Minimum supported client</span></span><br/> | <span data-ttu-id="67e63-128">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="67e63-128">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                    |
| <span data-ttu-id="67e63-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="67e63-129">Minimum supported server</span></span><br/> | <span data-ttu-id="67e63-130">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="67e63-130">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="67e63-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="67e63-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="67e63-132"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="67e63-132"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67e63-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="67e63-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67e63-134">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="67e63-134">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="67e63-135">MFTs compatibili con Direct3D</span><span class="sxs-lookup"><span data-stu-id="67e63-135">Direct3D-Aware MFTs</span></span>](direct3d-aware-mfts.md)
</dt> <dt>

[<span data-ttu-id="67e63-136">Supporto di DXVA 2,0 in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="67e63-136">Supporting DXVA 2.0 in Media Foundation</span></span>](supporting-dxva-2-0-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="67e63-137">Trasformazioni Media Foundation</span><span class="sxs-lookup"><span data-stu-id="67e63-137">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> <dt>

[<span data-ttu-id="67e63-138">Attributi di trasformazione</span><span class="sxs-lookup"><span data-stu-id="67e63-138">Transform Attributes</span></span>](transform-attributes.md)
</dt> <dt>

[<span data-ttu-id="67e63-139">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="67e63-139">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="67e63-140">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="67e63-140">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="67e63-141">\_Modalità DXVA topologia MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="67e63-141">MF\_TOPOLOGY\_DXVA\_MODE</span></span>](mf-topology-dxva-mode.md)
</dt> </dl>

 

 




