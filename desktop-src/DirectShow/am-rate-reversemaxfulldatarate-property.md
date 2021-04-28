---
description: 'AM_RATE_ReverseMaxFullDataRate proprietà : si applica a Windows Vista e versioni successive.'
ms.assetid: 4f170736-516d-4420-a215-e0e414f036cd
title: AM_RATE_ReverseMaxFullDataRate proprietà (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6e70a330433c8ea6e8116db944d8fb3d2ffff4d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099969"
---
# <a name="am_rate_reversemaxfulldatarate-property"></a><span data-ttu-id="18835-103">Am \_ RATE \_ ReverseMaxFullDataRate - proprietà</span><span class="sxs-lookup"><span data-stu-id="18835-103">AM\_RATE\_ReverseMaxFullDataRate Property</span></span>

<span data-ttu-id="18835-104">Si applica a Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="18835-104">Applies to Windows Vista and later.</span></span>

<span data-ttu-id="18835-105">Restituisce la velocità di riproduzione inversa massima del decodificatore.</span><span class="sxs-lookup"><span data-stu-id="18835-105">Returns the decoder's maximum reverse playback rate.</span></span> <span data-ttu-id="18835-106">Il valore della proprietà è il valore assoluto della velocità inversa massima x 10000.</span><span class="sxs-lookup"><span data-stu-id="18835-106">The value of the property is the absolute value of the maximum reverse speed x 10000.</span></span> <span data-ttu-id="18835-107">Ad esempio, se la velocità inversa massima è -2,0, il valore di questa proprietà è 20000.</span><span class="sxs-lookup"><span data-stu-id="18835-107">For example, if the maximum reverse speed is -2.0, the value of this property is 20000.</span></span>

<span data-ttu-id="18835-108">Il tipo di dati per questa proprietà **è AM \_ MaxFullDataRate,** che è un `typedef` per **LONG.**</span><span class="sxs-lookup"><span data-stu-id="18835-108">The data type for this property is **AM\_MaxFullDataRate**, which is a `typedef` for **LONG**.</span></span>

<span data-ttu-id="18835-109">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="18835-109">This property is read-only.</span></span>



| <span data-ttu-id="18835-110">Label</span><span class="sxs-lookup"><span data-stu-id="18835-110">Label</span></span> | <span data-ttu-id="18835-111">Valore</span><span class="sxs-lookup"><span data-stu-id="18835-111">Value</span></span> |
|-------------------|----------------------------------|
| <span data-ttu-id="18835-112">GUID set di proprietà</span><span class="sxs-lookup"><span data-stu-id="18835-112">Property Set GUID</span></span> | <span data-ttu-id="18835-113">AM \_ KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="18835-113">AM\_KSPROPSETID\_TSRateChange</span></span>    |
| <span data-ttu-id="18835-114">ID proprietà</span><span class="sxs-lookup"><span data-stu-id="18835-114">Property ID</span></span>       | <span data-ttu-id="18835-115">AM \_ RATE \_ ReverseMaxFullDataRate</span><span class="sxs-lookup"><span data-stu-id="18835-115">AM\_RATE\_ReverseMaxFullDataRate</span></span> |
| <span data-ttu-id="18835-116">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="18835-116">Data Type</span></span>         | <span data-ttu-id="18835-117">**AM \_ MaxFullDataRate**</span><span class="sxs-lookup"><span data-stu-id="18835-117">**AM\_MaxFullDataRate**</span></span>          |



 

## <a name="remarks"></a><span data-ttu-id="18835-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="18835-118">Remarks</span></span>

<span data-ttu-id="18835-119">I decodificatori che supportano la riproduzione inversa uniforme devono esporre questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="18835-119">Decoders that support smooth reverse playback should expose this property.</span></span> <span data-ttu-id="18835-120">Per altre informazioni, vedere [Miglioramenti della riproduzione DI DVD in Windows Vista.](dvd-playback-enhancements-in-windows-vista.md)</span><span class="sxs-lookup"><span data-stu-id="18835-120">For more information, see [DVD Playback Enhancements in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="18835-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="18835-121">Requirements</span></span>



| <span data-ttu-id="18835-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="18835-122">Requirement</span></span> | <span data-ttu-id="18835-123">Valore</span><span class="sxs-lookup"><span data-stu-id="18835-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="18835-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="18835-124">Header</span></span><br/> | <dl> <span data-ttu-id="18835-125"><dt>Dvdmedia.h</dt></span><span class="sxs-lookup"><span data-stu-id="18835-125"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18835-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="18835-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18835-127">**Impostare le proprietà di modifica della frequenza**</span><span class="sxs-lookup"><span data-stu-id="18835-127">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




