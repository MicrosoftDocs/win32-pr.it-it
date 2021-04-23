---
description: Si applica a Windows Vista e versioni successive.
ms.assetid: 4f170736-516d-4420-a215-e0e414f036cd
title: AM_RATE_ReverseMaxFullDataRate proprietà (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31e376c6e95160c6a6c3c6637a765d868e282d33
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910239"
---
# <a name="am_rate_reversemaxfulldatarate-property"></a><span data-ttu-id="8ae23-103">Proprietà AM \_ RATE \_ ReverseMaxFullDataRate</span><span class="sxs-lookup"><span data-stu-id="8ae23-103">AM\_RATE\_ReverseMaxFullDataRate Property</span></span>

<span data-ttu-id="8ae23-104">Si applica a Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="8ae23-104">Applies to Windows Vista and later.</span></span>

<span data-ttu-id="8ae23-105">Restituisce la velocità massima di riproduzione inversa del decodificatore.</span><span class="sxs-lookup"><span data-stu-id="8ae23-105">Returns the decoder's maximum reverse playback rate.</span></span> <span data-ttu-id="8ae23-106">Il valore della proprietà è il valore assoluto della velocità inversa massima x 10000.</span><span class="sxs-lookup"><span data-stu-id="8ae23-106">The value of the property is the absolute value of the maximum reverse speed x 10000.</span></span> <span data-ttu-id="8ae23-107">Ad esempio, se la velocità inversa massima è -2,0, il valore di questa proprietà è 20000.</span><span class="sxs-lookup"><span data-stu-id="8ae23-107">For example, if the maximum reverse speed is -2.0, the value of this property is 20000.</span></span>

<span data-ttu-id="8ae23-108">Il tipo di dati per questa proprietà **è AM \_ MaxFullDataRate,** che è un `typedef` per **LONG.**</span><span class="sxs-lookup"><span data-stu-id="8ae23-108">The data type for this property is **AM\_MaxFullDataRate**, which is a `typedef` for **LONG**.</span></span>

<span data-ttu-id="8ae23-109">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="8ae23-109">This property is read-only.</span></span>



| <span data-ttu-id="8ae23-110">Label</span><span class="sxs-lookup"><span data-stu-id="8ae23-110">Label</span></span> | <span data-ttu-id="8ae23-111">Valore</span><span class="sxs-lookup"><span data-stu-id="8ae23-111">Value</span></span> |
|-------------------|----------------------------------|
| <span data-ttu-id="8ae23-112">GUID set di proprietà</span><span class="sxs-lookup"><span data-stu-id="8ae23-112">Property Set GUID</span></span> | <span data-ttu-id="8ae23-113">AM \_ KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="8ae23-113">AM\_KSPROPSETID\_TSRateChange</span></span>    |
| <span data-ttu-id="8ae23-114">ID proprietà</span><span class="sxs-lookup"><span data-stu-id="8ae23-114">Property ID</span></span>       | <span data-ttu-id="8ae23-115">AM \_ RATE \_ ReverseMaxFullDataRate</span><span class="sxs-lookup"><span data-stu-id="8ae23-115">AM\_RATE\_ReverseMaxFullDataRate</span></span> |
| <span data-ttu-id="8ae23-116">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="8ae23-116">Data Type</span></span>         | <span data-ttu-id="8ae23-117">**AM \_ MaxFullDataRate**</span><span class="sxs-lookup"><span data-stu-id="8ae23-117">**AM\_MaxFullDataRate**</span></span>          |



 

## <a name="remarks"></a><span data-ttu-id="8ae23-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="8ae23-118">Remarks</span></span>

<span data-ttu-id="8ae23-119">I decodificatori che supportano la riproduzione inversa uniforme devono esporre questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="8ae23-119">Decoders that support smooth reverse playback should expose this property.</span></span> <span data-ttu-id="8ae23-120">Per altre informazioni, vedere [DVD Playback Enhancements in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="8ae23-120">For more information, see [DVD Playback Enhancements in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8ae23-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8ae23-121">Requirements</span></span>



| <span data-ttu-id="8ae23-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ae23-122">Requirement</span></span> | <span data-ttu-id="8ae23-123">Valore</span><span class="sxs-lookup"><span data-stu-id="8ae23-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8ae23-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8ae23-124">Header</span></span><br/> | <dl> <span data-ttu-id="8ae23-125"><dt>Dvdmedia.h</dt></span><span class="sxs-lookup"><span data-stu-id="8ae23-125"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ae23-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8ae23-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ae23-127">**Rate Change Property Set**</span><span class="sxs-lookup"><span data-stu-id="8ae23-127">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




