---
description: Specifica il tempo massimo, in millisecondi, tra i fotogrammi chiave nell'output del codec.
ms.assetid: 2a52e6a5-10a0-46dd-aa31-cb55094903b5
title: Proprietà MFPKEY_KEYDIST (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d55925811db71f24cf360113aa6d03a325bcdc11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880797"
---
# <a name="mfpkey_keydist-property"></a><span data-ttu-id="3122e-103">\_Proprietà MFPKEY</span><span class="sxs-lookup"><span data-stu-id="3122e-103">MFPKEY\_KEYDIST Property</span></span>

<span data-ttu-id="3122e-104">Specifica il tempo massimo, in millisecondi, tra i fotogrammi chiave nell'output del codec.</span><span class="sxs-lookup"><span data-stu-id="3122e-104">Specifies the maximum time, in milliseconds, between key frames in the codec output.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="3122e-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="3122e-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="3122e-106">g \_ wszWMVCKeyframeDistance</span><span class="sxs-lookup"><span data-stu-id="3122e-106">g\_wszWMVCKeyframeDistance</span></span>

## <a name="data-type"></a><span data-ttu-id="3122e-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="3122e-107">Data Type</span></span>

<span data-ttu-id="3122e-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="3122e-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="3122e-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="3122e-109">Default Value</span></span>

<span data-ttu-id="3122e-110">Il valore predefinito dipende dalla versione di Windows in esecuzione, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="3122e-110">The default value depends on which version of Windows is running, as shown in the following table.</span></span>



| <span data-ttu-id="3122e-111">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="3122e-111">Operating system</span></span> | <span data-ttu-id="3122e-112">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="3122e-112">Default value</span></span> |
|------------------|---------------|
| <span data-ttu-id="3122e-113">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3122e-113">Windows XP</span></span>       | <span data-ttu-id="3122e-114">8000</span><span class="sxs-lookup"><span data-stu-id="3122e-114">8000</span></span>          |
| <span data-ttu-id="3122e-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3122e-115">Windows Vista</span></span>    | <span data-ttu-id="3122e-116">8000</span><span class="sxs-lookup"><span data-stu-id="3122e-116">8000</span></span>          |
| <span data-ttu-id="3122e-117">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3122e-117">Windows 7</span></span>        | <span data-ttu-id="3122e-118">2000</span><span class="sxs-lookup"><span data-stu-id="3122e-118">2000</span></span>          |



 

## <a name="remarks"></a><span data-ttu-id="3122e-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="3122e-119">Remarks</span></span>

<span data-ttu-id="3122e-120">La logica interna del codec determina la posizione effettiva di ogni fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="3122e-120">The internal logic of the codec determines the actual location of each key frame.</span></span> <span data-ttu-id="3122e-121">La distanza tra due fotogrammi chiave può essere inferiore al valore di questa proprietà, tuttavia, non sarà mai maggiore.</span><span class="sxs-lookup"><span data-stu-id="3122e-121">The distance between any two key frames may be less than the value of this property, however, it will never be greater.</span></span>

## <a name="requirements"></a><span data-ttu-id="3122e-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3122e-122">Requirements</span></span>



| <span data-ttu-id="3122e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="3122e-123">Requirement</span></span> | <span data-ttu-id="3122e-124">Valore</span><span class="sxs-lookup"><span data-stu-id="3122e-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3122e-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3122e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3122e-126">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3122e-126">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3122e-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3122e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3122e-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3122e-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3122e-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3122e-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="3122e-130"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3122e-130"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3122e-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3122e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3122e-132">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3122e-132">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




