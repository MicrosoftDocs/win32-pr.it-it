---
description: Si applica a Windows Vista e versioni successive.
ms.assetid: 4f170736-516d-4420-a215-e0e414f036cd
title: Proprietà AM_RATE_ReverseMaxFullDataRate (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 679e83038a74e64d7a39e8757a9ffaf61fc88c93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330325"
---
# <a name="am_rate_reversemaxfulldatarate-property"></a><span data-ttu-id="38f86-103">\_Proprietà rate \_ ReverseMaxFullDataRate</span><span class="sxs-lookup"><span data-stu-id="38f86-103">AM\_RATE\_ReverseMaxFullDataRate Property</span></span>

<span data-ttu-id="38f86-104">Si applica a Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="38f86-104">Applies to Windows Vista and later.</span></span>

<span data-ttu-id="38f86-105">Restituisce la frequenza massima di riproduzione inversa del decodificatore.</span><span class="sxs-lookup"><span data-stu-id="38f86-105">Returns the decoder's maximum reverse playback rate.</span></span> <span data-ttu-id="38f86-106">Il valore della proprietà è il valore assoluto della velocità inversa massima x 10000.</span><span class="sxs-lookup"><span data-stu-id="38f86-106">The value of the property is the absolute value of the maximum reverse speed x 10000.</span></span> <span data-ttu-id="38f86-107">Se ad esempio la velocità massima inversa è-2,0, il valore di questa proprietà è 20000.</span><span class="sxs-lookup"><span data-stu-id="38f86-107">For example, if the maximum reverse speed is -2.0, the value of this property is 20000.</span></span>

<span data-ttu-id="38f86-108">Il tipo di dati di questa proprietà **è \_ MaxFullDataRate**, che è un oggetto `typedef` per **Long**.</span><span class="sxs-lookup"><span data-stu-id="38f86-108">The data type for this property is **AM\_MaxFullDataRate**, which is a `typedef` for **LONG**.</span></span>

<span data-ttu-id="38f86-109">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="38f86-109">This property is read-only.</span></span>



|                   |                                  |
|-------------------|----------------------------------|
| <span data-ttu-id="38f86-110">GUID set di proprietà</span><span class="sxs-lookup"><span data-stu-id="38f86-110">Property Set GUID</span></span> | <span data-ttu-id="38f86-111">\_TSRateChange KSPROPSETID \_</span><span class="sxs-lookup"><span data-stu-id="38f86-111">AM\_KSPROPSETID\_TSRateChange</span></span>    |
| <span data-ttu-id="38f86-112">ID proprietà</span><span class="sxs-lookup"><span data-stu-id="38f86-112">Property ID</span></span>       | <span data-ttu-id="38f86-113">\_Frequenza \_ ReverseMaxFullDataRate</span><span class="sxs-lookup"><span data-stu-id="38f86-113">AM\_RATE\_ReverseMaxFullDataRate</span></span> |
| <span data-ttu-id="38f86-114">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="38f86-114">Data Type</span></span>         | <span data-ttu-id="38f86-115">**AM \_ MaxFullDataRate**</span><span class="sxs-lookup"><span data-stu-id="38f86-115">**AM\_MaxFullDataRate**</span></span>          |



 

## <a name="remarks"></a><span data-ttu-id="38f86-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="38f86-116">Remarks</span></span>

<span data-ttu-id="38f86-117">I decodificatori che supportano la riproduzione Smooth inversa devono esporre questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="38f86-117">Decoders that support smooth reverse playback should expose this property.</span></span> <span data-ttu-id="38f86-118">Per ulteriori informazioni, vedere [miglioramenti della riproduzione DVD in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="38f86-118">For more information, see [DVD Playback Enhancements in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="38f86-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="38f86-119">Requirements</span></span>



| <span data-ttu-id="38f86-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="38f86-120">Requirement</span></span> | <span data-ttu-id="38f86-121">Valore</span><span class="sxs-lookup"><span data-stu-id="38f86-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="38f86-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="38f86-122">Header</span></span><br/> | <dl> <span data-ttu-id="38f86-123"><dt>Dvdmedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="38f86-123"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38f86-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="38f86-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38f86-125">**Set di proprietà di modifica della frequenza**</span><span class="sxs-lookup"><span data-stu-id="38f86-125">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




