---
description: Specifica se una trasformazione Media Foundation (MFT) supporta Microsoft Direct3D 11.
ms.assetid: 23482B8A-58F3-4B39-9C6D-54EC27D36C01
title: Attributo MF_SA_D3D11_AWARE (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d90f560e3d31b80c1b3fbcbb5c25c4e20815f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344176"
---
# <a name="mf_sa_d3d11_aware-attribute"></a><span data-ttu-id="03543-103">\_ \_ \_ Attributo Aware SA d3d11</span><span class="sxs-lookup"><span data-stu-id="03543-103">MF\_SA\_D3D11\_AWARE attribute</span></span>

<span data-ttu-id="03543-104">Specifica se una trasformazione Media Foundation (MFT) supporta Microsoft Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="03543-104">Specifies whether a Media Foundation transform (MFT) supports Microsoft Direct3D 11.</span></span>

## <a name="data-type"></a><span data-ttu-id="03543-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="03543-105">Data type</span></span>

<span data-ttu-id="03543-106">**Bool** archiviato come **UInt32**</span><span class="sxs-lookup"><span data-stu-id="03543-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="03543-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="03543-107">Remarks</span></span>

<span data-ttu-id="03543-108">Questo attributo si applica solo ai video MFTs.</span><span class="sxs-lookup"><span data-stu-id="03543-108">This attribute applies only to video MFTs.</span></span> <span data-ttu-id="03543-109">Per eseguire una query su questo attributo, chiamare [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) per ottenere l'archivio di attributi MFT.</span><span class="sxs-lookup"><span data-stu-id="03543-109">To query this attribute, call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) to get the MFT attribute store.</span></span> <span data-ttu-id="03543-110">Se **GetAttributes** ha esito positivo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="03543-110">If **GetAttributes** succeeds, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

-   <span data-ttu-id="03543-111">Se l'attributo è diverso da zero, il client può assegnare a MFT un puntatore all'interfaccia [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) prima dell'avvio del flusso.</span><span class="sxs-lookup"><span data-stu-id="03543-111">If the attribute is nonzero, the client can give the MFT a pointer to the [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) interface before streaming starts.</span></span> <span data-ttu-id="03543-112">A tale scopo, il client invia il messaggio di [**\_ \_ \_ \_ gestione D3D message set D3D**](mft-message-set-d3d-manager.md) al MFT.</span><span class="sxs-lookup"><span data-stu-id="03543-112">To do so, the client sends the [**MFT\_MESSAGE\_SET\_D3D\_MANAGER**](mft-message-set-d3d-manager.md) message to the MFT.</span></span> <span data-ttu-id="03543-113">Il client non è necessario per l'invio di questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="03543-113">The client is not required to send this message.</span></span>
-   <span data-ttu-id="03543-114">Se questo attributo è zero (**false**), MFT non supporta Direct3D 11 e il client non deve inviare il messaggio [**MFT \_ message \_ set \_ D3D \_ Manager**](mft-message-set-d3d-manager.md) al MFT.</span><span class="sxs-lookup"><span data-stu-id="03543-114">If this attribute is zero (**FALSE**), the MFT does not support Direct3D 11, and the client should not send the [**MFT\_MESSAGE\_SET\_D3D\_MANAGER**](mft-message-set-d3d-manager.md) message to the MFT.</span></span>

<span data-ttu-id="03543-115">Il valore predefinito di questo attributo è **false**.</span><span class="sxs-lookup"><span data-stu-id="03543-115">The default value of this attribute is **FALSE**.</span></span> <span data-ttu-id="03543-116">Considerare questo attributo come di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="03543-116">Treat this attribute as read-only.</span></span> <span data-ttu-id="03543-117">Non modificare il valore. il MFT ignorerà tutte le modifiche apportate al valore.</span><span class="sxs-lookup"><span data-stu-id="03543-117">Do not change the value; the MFT will ignore any changes to the value.</span></span>

## <a name="requirements"></a><span data-ttu-id="03543-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="03543-118">Requirements</span></span>



| <span data-ttu-id="03543-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="03543-119">Requirement</span></span> | <span data-ttu-id="03543-120">Valore</span><span class="sxs-lookup"><span data-stu-id="03543-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="03543-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03543-121">Minimum supported client</span></span><br/> | <span data-ttu-id="03543-122">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="03543-122">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="03543-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03543-123">Minimum supported server</span></span><br/> | <span data-ttu-id="03543-124">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="03543-124">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="03543-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="03543-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="03543-126"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="03543-126"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03543-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="03543-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03543-128">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="03543-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="03543-129">Supporto della decodifica video Direct3D 11 in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="03543-129">Supporting Direct3D 11 Video Decoding in Media Foundation</span></span>](supporting-direct3d-11-video-decoding-in-media-foundation.md)
</dt> </dl>

 

 




