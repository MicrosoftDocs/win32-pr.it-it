---
description: Specifica se la complessità dell'algoritmo di codifica audio è vincolata.
ms.assetid: a50b840f-9fe8-4291-b93f-f09c241fe802
title: Proprietà MFPKEY_CONSTRAINENCOMPLEXITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdc6e3d5a7077c72e5933ecbc235092174e263fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310649"
---
# <a name="mfpkey_constrainencomplexity-property"></a><span data-ttu-id="176f9-103">\_Proprietà CONSTRAINENCOMPLEXITY di MFPKEY</span><span class="sxs-lookup"><span data-stu-id="176f9-103">MFPKEY\_CONSTRAINENCOMPLEXITY Property</span></span>

<span data-ttu-id="176f9-104">Specifica se la complessità dell'algoritmo di codifica audio è vincolata.</span><span class="sxs-lookup"><span data-stu-id="176f9-104">Specifies whether the complexity of the audio encoding algorithm is constrained.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="176f9-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="176f9-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="176f9-106">Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="176f9-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="176f9-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="176f9-107">Data Type</span></span>

<span data-ttu-id="176f9-108">**\_bool VT**</span><span class="sxs-lookup"><span data-stu-id="176f9-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="176f9-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="176f9-109">Default Value</span></span>

<span data-ttu-id="176f9-110">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="176f9-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="176f9-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="176f9-111">Remarks</span></span>

<span data-ttu-id="176f9-112">Se si lascia questa proprietà sul valore predefinito **Variant \_ false**, il codificatore audio utilizza l'algoritmo predefinito.</span><span class="sxs-lookup"><span data-stu-id="176f9-112">If you leave this property at its default value of **VARIANT\_FALSE**, the audio encoder uses its default algorithm.</span></span> <span data-ttu-id="176f9-113">L'algoritmo predefinito dipende dal tipo di output e dalla versione di Windows in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="176f9-113">The default algorithm depends on the output type and which version of Windows is running.</span></span> <span data-ttu-id="176f9-114">Nella tabella seguente viene descritto il comportamento predefinito per le diverse combinazioni.</span><span class="sxs-lookup"><span data-stu-id="176f9-114">The following table describes the default behavior for the different combinations.</span></span>



| <span data-ttu-id="176f9-115">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="176f9-115">Operating system</span></span> | <span data-ttu-id="176f9-116">Comportamento predefinito</span><span class="sxs-lookup"><span data-stu-id="176f9-116">Default behavior</span></span>                                                                                                                                                                                    |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="176f9-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="176f9-117">Windows Vista</span></span>    | <span data-ttu-id="176f9-118">Per tutti i tipi di output, per impostazione predefinita il codificatore audio utilizza l'algoritmo più complesso.</span><span class="sxs-lookup"><span data-stu-id="176f9-118">For all output types, the audio encoder uses the most complex algorithm by default.</span></span>                                                                                                                 |
| <span data-ttu-id="176f9-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="176f9-119">Windows 7</span></span>        | <span data-ttu-id="176f9-120">Per i tipi di output standard e Professional, per impostazione predefinita il codificatore audio utilizza l'algoritmo più complesso.</span><span class="sxs-lookup"><span data-stu-id="176f9-120">For Standard and Professional output types, the audio encoder uses the most complex algorithm by default.</span></span> <span data-ttu-id="176f9-121">Per i tipi di output Lossless, per impostazione predefinita il codificatore audio utilizza l'algoritmo meno complesso.</span><span class="sxs-lookup"><span data-stu-id="176f9-121">For Lossless output types, the audio encoder uses the least complex algorithm by default.</span></span> |



 

<span data-ttu-id="176f9-122">Se si imposta questa proprietà su **Variant \_ true**, è necessario specificare anche un valore di complessità impostando la proprietà [**MFPKEY \_ ENCCOMPLEXITY**](mfpkey-enccomplexityproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="176f9-122">If you set this property to **VARIANT\_TRUE**, you must also specify a complexity value by setting the [**MFPKEY\_ENCCOMPLEXITY**](mfpkey-enccomplexityproperty.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="176f9-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="176f9-123">Requirements</span></span>



| <span data-ttu-id="176f9-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="176f9-124">Requirement</span></span> | <span data-ttu-id="176f9-125">Valore</span><span class="sxs-lookup"><span data-stu-id="176f9-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="176f9-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="176f9-126">Minimum supported client</span></span><br/> | <span data-ttu-id="176f9-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="176f9-127">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="176f9-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="176f9-128">Minimum supported server</span></span><br/> | <span data-ttu-id="176f9-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="176f9-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="176f9-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="176f9-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="176f9-131"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="176f9-131"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="176f9-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="176f9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="176f9-133">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="176f9-133">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
