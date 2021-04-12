---
description: Rappresenta una richiesta di un campione da un MediaStreamSource.
ms.assetid: 43617cda-84b1-405f-8a20-be793413c186
title: Interfaccia IMFMediaStreamSourceSampleRequest
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaStreamSourceSampleRequest
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: fa159727c6e13a894148391b9508afad4b8dacfc
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351511"
---
# <a name="imfmediastreamsourcesamplerequest-interface"></a><span data-ttu-id="bf4eb-103">Interfaccia IMFMediaStreamSourceSampleRequest</span><span class="sxs-lookup"><span data-stu-id="bf4eb-103">IMFMediaStreamSourceSampleRequest interface</span></span>

<span data-ttu-id="bf4eb-104">Rappresenta una richiesta di un campione da un MediaStreamSource.</span><span class="sxs-lookup"><span data-stu-id="bf4eb-104">Represents a request for a sample from a MediaStreamSource.</span></span>

## <a name="members"></a><span data-ttu-id="bf4eb-105">Membri</span><span class="sxs-lookup"><span data-stu-id="bf4eb-105">Members</span></span>

<span data-ttu-id="bf4eb-106">L'interfaccia **IMFMediaStreamSourceSampleRequest** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="bf4eb-106">The **IMFMediaStreamSourceSampleRequest** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="bf4eb-107">**IMFMediaStreamSourceSampleRequest** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="bf4eb-107">**IMFMediaStreamSourceSampleRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="bf4eb-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="bf4eb-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="bf4eb-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="bf4eb-109">Methods</span></span>

<span data-ttu-id="bf4eb-110">L'interfaccia **IMFMediaStreamSourceSampleRequest** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="bf4eb-110">The **IMFMediaStreamSourceSampleRequest** interface has these methods.</span></span>



| <span data-ttu-id="bf4eb-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="bf4eb-111">Method</span></span>                                                           | <span data-ttu-id="bf4eb-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bf4eb-112">Description</span></span>                                             |
|:-----------------------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="bf4eb-113">**SetSample**</span><span class="sxs-lookup"><span data-stu-id="bf4eb-113">**SetSample**</span></span>](imfmediastreamsourcesamplerequest-setsample.md) | <span data-ttu-id="bf4eb-114">Imposta l'esempio per l'origine del flusso multimediale.</span><span class="sxs-lookup"><span data-stu-id="bf4eb-114">Sets the sample for the media stream source.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bf4eb-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="bf4eb-115">Remarks</span></span>

<span data-ttu-id="bf4eb-116">**MFMediaStreamSourceSampleRequest** viene implementato dalla classe di runtime [**Windows. Media. Core. MediaStreamSourceSampleRequest**](/uwp/api/Windows.Media.Core.MediaStreamSourceSampleRequest?view=winrt-19041) .</span><span class="sxs-lookup"><span data-stu-id="bf4eb-116">**MFMediaStreamSourceSampleRequest** is implemented by the [**Windows.Media.Core.MediaStreamSourceSampleRequest**](/uwp/api/Windows.Media.Core.MediaStreamSourceSampleRequest?view=winrt-19041) runtime class.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf4eb-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf4eb-117">Requirements</span></span>



| <span data-ttu-id="bf4eb-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf4eb-118">Requirement</span></span> | <span data-ttu-id="bf4eb-119">Valore</span><span class="sxs-lookup"><span data-stu-id="bf4eb-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bf4eb-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf4eb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bf4eb-121">App \[ desktop di Windows 8.1 app \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="bf4eb-121">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="bf4eb-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf4eb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bf4eb-123">App desktop di Windows Server 2012 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="bf4eb-123">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                       |
| <span data-ttu-id="bf4eb-124">IDL</span><span class="sxs-lookup"><span data-stu-id="bf4eb-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bf4eb-125"><dt>Mfidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bf4eb-125"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf4eb-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bf4eb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf4eb-127">Interfacce di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bf4eb-127">Media Foundation Interfaces</span></span>](media-foundation-interfaces.md)
</dt> </dl>

 

 
