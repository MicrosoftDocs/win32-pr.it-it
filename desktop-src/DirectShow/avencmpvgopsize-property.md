---
description: Specifica il numero massimo di immagini da un'intestazione GOP (Group-of-Pictures) all'intestazione GOP successiva.
ms.assetid: 90433df4-5a96-4bc2-a780-93306abcb0a4
title: Proprietà AVEncMPVGOPSize (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c8907d0992153039b1af9a9a0e82ee5782b525d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104049022"
---
# <a name="avencmpvgopsize-property"></a><span data-ttu-id="a064e-103">Proprietà AVEncMPVGOPSize</span><span class="sxs-lookup"><span data-stu-id="a064e-103">AVEncMPVGOPSize property</span></span>

<span data-ttu-id="a064e-104">Specifica il numero massimo di immagini da un'intestazione GOP (Group-of-Pictures) all'intestazione GOP successiva.</span><span class="sxs-lookup"><span data-stu-id="a064e-104">Specifies the maximum number of pictures from one group-of-pictures (GOP) header to the next GOP header.</span></span>

<span data-ttu-id="a064e-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="a064e-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="a064e-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a064e-106">Data type</span></span>

<span data-ttu-id="a064e-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="a064e-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="a064e-108">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="a064e-108">Property GUID</span></span>

<span data-ttu-id="a064e-109">**Codecapis \_ AVEncMPVGOPSize**</span><span class="sxs-lookup"><span data-stu-id="a064e-109">**CODECAPI\_AVEncMPVGOPSize**</span></span>

## <a name="property-value"></a><span data-ttu-id="a064e-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="a064e-110">Property value</span></span>

<span data-ttu-id="a064e-111">I codificatori possono implementare questa proprietà come un set enumerato o come intervallo lineare.</span><span class="sxs-lookup"><span data-stu-id="a064e-111">Encoders can implement this property as an enumerated set or as a linear range.</span></span>

## <a name="remarks"></a><span data-ttu-id="a064e-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="a064e-112">Remarks</span></span>

<span data-ttu-id="a064e-113">Impostare questa proprietà prima di avviare una registrazione.</span><span class="sxs-lookup"><span data-stu-id="a064e-113">Set this property before starting a recording.</span></span>

<span data-ttu-id="a064e-114">**Si applica a Windows 8:** La dimensione del GOP codificata deve essere minore o uguale al numero specificato tramite questa proprietà, in modo da tenere lo stesso modello di frame B impostato da [CODEcapit \_ AVEncMPVDefaultBPictureCount](avencmpvdefaultbpicturecount-property.md) in tutto il GOP o a causa di una modifica della scena.</span><span class="sxs-lookup"><span data-stu-id="a064e-114">**Applies to Windows 8:** The encoded GOP size shall be smaller than or equal to the specified number through this property, in order to keep the same B frame pattern set by [CODECAPI\_AVEncMPVDefaultBPictureCount](avencmpvdefaultbpicturecount-property.md) throughout the GOP or due to scene change.</span></span> <span data-ttu-id="a064e-115">Ad esempio, quando il numero di fotogrammi B in un GOP viene specificato come 2 e le dimensioni del GOP sono 11, il codificatore deve produrre dimensioni GOP di 10 fotogrammi o meno.</span><span class="sxs-lookup"><span data-stu-id="a064e-115">For example, when the number of B frames in a GOP is specified to be 2, and GOP size is 11, then encoder shall produce GOP size of 10 frames or less.</span></span> <span data-ttu-id="a064e-116">Quando la modifica della scena viene eseguita al centro di un GOP, il codificatore può anche inserire il fotogramma chiave e produrre un GOP più piccolo.</span><span class="sxs-lookup"><span data-stu-id="a064e-116">When scene change happens in the middle of a GOP, encoder might also insert key frame and produce smaller GOP.</span></span>

<span data-ttu-id="a064e-117">La dimensione GOP 0 è dipendente dal codificatore e i codificatori possono scegliere Dimensioni GOP diverse in base all'implementazione, alla qualità e alle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="a064e-117">GOP size 0 is encoder dependent and encoders can choose different GOP sizes based on their implementation/quality/performance.</span></span> <span data-ttu-id="a064e-118">I codificatori devono rispettare le dimensioni GOP e troncare i frame B in questo caso.</span><span class="sxs-lookup"><span data-stu-id="a064e-118">Encoders should honor the GOP size and truncate B frames in this case.</span></span>

## <a name="requirements"></a><span data-ttu-id="a064e-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a064e-119">Requirements</span></span>



| <span data-ttu-id="a064e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a064e-120">Requirement</span></span> | <span data-ttu-id="a064e-121">Valore</span><span class="sxs-lookup"><span data-stu-id="a064e-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a064e-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a064e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a064e-123">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="a064e-123">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="a064e-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a064e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a064e-125">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a064e-125">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="a064e-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a064e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a064e-127"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="a064e-127"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a064e-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a064e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a064e-129">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="a064e-129">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="a064e-130">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="a064e-130">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




