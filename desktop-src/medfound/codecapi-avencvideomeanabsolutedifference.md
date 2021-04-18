---
description: Controlla la segnalazione di MFSampleExtension \_ MeanAbsoluteDifference tramite IMFAttribute in ogni esempio di output.
ms.assetid: 61C0F431-FBF5-4B17-8F3A-0F6AD2BA33B7
title: Proprietà CODECAPI_AVEncVideoMeanAbsoluteDifference (codecapit. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f58a7bc0da9fce88c0b8137d800d527d4717801c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305487"
---
# <a name="codecapi_avencvideomeanabsolutedifference-property"></a><span data-ttu-id="6b1e9-103">Proprietà AVEncVideoMeanAbsoluteDifference di codecapi \_</span><span class="sxs-lookup"><span data-stu-id="6b1e9-103">CODECAPI\_AVEncVideoMeanAbsoluteDifference property</span></span>

<span data-ttu-id="6b1e9-104">Controlla la segnalazione di [MFSampleExtension \_ MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) tramite [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) in ogni esempio di output.</span><span class="sxs-lookup"><span data-stu-id="6b1e9-104">Controls the signaling of [MFSampleExtension\_MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) through [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) on each output sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="6b1e9-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="6b1e9-105">Data type</span></span>

<span data-ttu-id="6b1e9-106">**ULONG** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="6b1e9-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="6b1e9-107">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="6b1e9-107">Property GUID</span></span>

<span data-ttu-id="6b1e9-108">**Codecapis \_ AVEncVideoMeanAbsoluteDifference**</span><span class="sxs-lookup"><span data-stu-id="6b1e9-108">**CODECAPI\_AVEncVideoMeanAbsoluteDifference**</span></span>

## <a name="remarks"></a><span data-ttu-id="6b1e9-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="6b1e9-109">Remarks</span></span>

<span data-ttu-id="6b1e9-110">Se l'applicazione imposta un valore diverso da zero, il codificatore deve aggiungere l'attributo di esempio [MFSampleExtension \_ MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) a ogni esempio di output.</span><span class="sxs-lookup"><span data-stu-id="6b1e9-110">If the application sets a non-zero value then the encoder should add the [MFSampleExtension\_MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) sample attribute to each output sample.</span></span> <span data-ttu-id="6b1e9-111">L' \_ attributo MeanAbsoluteDifference di MFSampleExtension indica la differenza assoluta media tra gli esempi di origine e gli esempi stimati nel piano Y.</span><span class="sxs-lookup"><span data-stu-id="6b1e9-111">The MFSampleExtension\_MeanAbsoluteDifference attribute indicates the mean absolute difference between the source samples and the predicted samples in the Y plane.</span></span>

<span data-ttu-id="6b1e9-112">Se il codificatore restituisce 0 per **GetParameterRange**, il codificatore non supporta l'output di [MFSampleExtension \_ MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) sugli esempi di output.</span><span class="sxs-lookup"><span data-stu-id="6b1e9-112">If the encoder returns 0 for **GetParameterRange**, then the encoder does not support the output of [MFSampleExtension\_MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) on the output samples.</span></span>

<span data-ttu-id="6b1e9-113">Il valore predefinito deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="6b1e9-113">The default value should be 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b1e9-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6b1e9-114">Requirements</span></span>



| <span data-ttu-id="6b1e9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b1e9-115">Requirement</span></span> | <span data-ttu-id="6b1e9-116">Valore</span><span class="sxs-lookup"><span data-stu-id="6b1e9-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6b1e9-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b1e9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6b1e9-118">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6b1e9-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6b1e9-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b1e9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6b1e9-120">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="6b1e9-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6b1e9-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6b1e9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b1e9-122"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b1e9-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b1e9-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6b1e9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b1e9-124">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6b1e9-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




