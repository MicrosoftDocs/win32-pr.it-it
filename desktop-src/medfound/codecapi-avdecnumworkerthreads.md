---
description: Imposta il numero di thread di lavoro utilizzati da un decodificatore video.
ms.assetid: A1570BB5-62BC-46C0-B9C9-61F99AA13BBE
title: Proprietà CODECAPI_AVDecNumWorkerThreads (codecapit. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5d7c57d1b4176ad65313a5583a70f9ba4f7427a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305503"
---
# <a name="codecapi_avdecnumworkerthreads-property"></a><span data-ttu-id="98733-103">Proprietà AVDecNumWorkerThreads di codecapi \_</span><span class="sxs-lookup"><span data-stu-id="98733-103">CODECAPI\_AVDecNumWorkerThreads property</span></span>

<span data-ttu-id="98733-104">Imposta il numero di thread di lavoro utilizzati da un decodificatore video.</span><span class="sxs-lookup"><span data-stu-id="98733-104">Sets the number of worker threads that are used by a video decoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="98733-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="98733-105">Data type</span></span>

<span data-ttu-id="98733-106">**Long** (**VT \_ I4**)</span><span class="sxs-lookup"><span data-stu-id="98733-106">**LONG** (**VT\_I4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="98733-107">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="98733-107">Property GUID</span></span>

<span data-ttu-id="98733-108">Codecapis \_ AVDecNumWorkerThreads</span><span class="sxs-lookup"><span data-stu-id="98733-108">CODECAPI\_AVDecNumWorkerThreads</span></span>

## <a name="remarks"></a><span data-ttu-id="98733-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="98733-109">Remarks</span></span>

<span data-ttu-id="98733-110">Se il valore è 1, il decodificatore seleziona il numero di thread.</span><span class="sxs-lookup"><span data-stu-id="98733-110">If the value is  1, the decoder selects the number of threads.</span></span>

<span data-ttu-id="98733-111">Per l'interfaccia [**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi) , impostare questa proprietà come valore **Long** (**VT \_ I4**).</span><span class="sxs-lookup"><span data-stu-id="98733-111">For the [**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi) interface, set this property as a **LONG** value (**VT\_I4**).</span></span> <span data-ttu-id="98733-112">Per l'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) , impostare questa proprietà come **UInt32**, anche se il valore è firmato.</span><span class="sxs-lookup"><span data-stu-id="98733-112">For the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface, set this property as a **UINT32**, although the value is signed.</span></span>

## <a name="requirements"></a><span data-ttu-id="98733-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="98733-113">Requirements</span></span>



| <span data-ttu-id="98733-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="98733-114">Requirement</span></span> | <span data-ttu-id="98733-115">Valore</span><span class="sxs-lookup"><span data-stu-id="98733-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="98733-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98733-116">Minimum supported client</span></span><br/> | <span data-ttu-id="98733-117">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="98733-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="98733-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98733-118">Minimum supported server</span></span><br/> | <span data-ttu-id="98733-119">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="98733-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="98733-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="98733-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="98733-121"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="98733-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98733-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="98733-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98733-123">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="98733-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="98733-124">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="98733-124">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

