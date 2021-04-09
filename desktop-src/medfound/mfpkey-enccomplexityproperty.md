---
description: Specifica la complessità dell'algoritmo di codifica.
ms.assetid: 5dd34818-f282-4859-b423-97e9c4944aec
title: Proprietà MFPKEY_ENCCOMPLEXITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51f50e7966a05affe8ae75869b670cf75f088b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880809"
---
# <a name="mfpkey_enccomplexity-property"></a><span data-ttu-id="03271-103">\_Proprietà ENCCOMPLEXITY di MFPKEY</span><span class="sxs-lookup"><span data-stu-id="03271-103">MFPKEY\_ENCCOMPLEXITY Property</span></span>

<span data-ttu-id="03271-104">Specifica la complessità dell'algoritmo di codifica.</span><span class="sxs-lookup"><span data-stu-id="03271-104">Specifies the complexity of the encoding algorithm.</span></span> <span data-ttu-id="03271-105">Il valore è un numero intero compreso tra 0 e 100, dove 0 specifica l'algoritmo meno complesso e 100 specifica l'algoritmo più complesso.</span><span class="sxs-lookup"><span data-stu-id="03271-105">The value is an integer between 0 and 100, where 0 specifies the least complex algorithm, and 100 specifies the most complex algorithm.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="03271-106">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="03271-106">Constant for IPropertyBag</span></span>

<span data-ttu-id="03271-107">Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="03271-107">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="03271-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="03271-108">Data Type</span></span>

<span data-ttu-id="03271-109">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="03271-109">**VT\_UI4**</span></span>

## <a name="default-value"></a><span data-ttu-id="03271-110">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="03271-110">Default Value</span></span>

<span data-ttu-id="03271-111">100 per Windows Media Audio 10 e Windows Media Audio 10 Professional</span><span class="sxs-lookup"><span data-stu-id="03271-111">100 for Windows Media Audio 10 and Windows Media Audio 10 Professional</span></span>

<span data-ttu-id="03271-112">100 per la versione di Windows Vista di Windows Media Audio 10 Lossless</span><span class="sxs-lookup"><span data-stu-id="03271-112">100 for the Windows Vista release of Windows Media Audio 10 Lossless</span></span>

<span data-ttu-id="03271-113">0 per la versione di Windows 7 Windows Media Audio 10 Lossless</span><span class="sxs-lookup"><span data-stu-id="03271-113">0 for the Windows 7 release Windows Media Audio 10 Lossless</span></span>

## <a name="remarks"></a><span data-ttu-id="03271-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="03271-114">Remarks</span></span>

<span data-ttu-id="03271-115">Se la proprietà [**MFPKEY \_ CONSTRAINECOMPLEXITY**](mfpkey-constrainenccomplexityproperty.md) ha un valore **Variant \_ true**, il codificatore regola la complessità dell'algoritmo in base al valore di questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="03271-115">If the [**MFPKEY\_CONSTRAINECOMPLEXITY**](mfpkey-constrainenccomplexityproperty.md) property has a value of **VARIANT\_TRUE**, the encoder adjusts the complexity of its algorithm according to the value of this property.</span></span>

<span data-ttu-id="03271-116">Per il codificatore Windows Media Audio 10 e il codificatore Windows Media Audio 10 Professional, se il valore di questa proprietà è 100, il codificatore pone una domanda elevata sulla CPU e produce l'output di qualità superiore.</span><span class="sxs-lookup"><span data-stu-id="03271-116">For the Windows Media Audio 10 encoder and the Windows Media Audio 10 Professional encoder, if the value of this property is 100, the encoder places a high demand on the CPU and produces the highest quality output.</span></span> <span data-ttu-id="03271-117">Poiché il valore di questa proprietà diminuisce, la richiesta sulla CPU diminuisce, ma anche la qualità dell'output diminuisce.</span><span class="sxs-lookup"><span data-stu-id="03271-117">As the value of this property decreases, the demand on the CPU decreases, but the quality of the output also decreases.</span></span>

<span data-ttu-id="03271-118">Per il codificatore Windows Media Audio 10 Lossless, se il valore di questa proprietà è 0, il codificatore pone una domanda bassa sulla CPU.</span><span class="sxs-lookup"><span data-stu-id="03271-118">For the Windows Media Audio 10 Lossless encoder, if the value of this property is 0, the encoder places a low demand on the CPU.</span></span> <span data-ttu-id="03271-119">Man mano che aumenta il valore di questa proprietà, la domanda sulla CPU aumenta e le dimensioni dell'output del codificatore diminuiscono leggermente.</span><span class="sxs-lookup"><span data-stu-id="03271-119">As the value of this property increases, the demand on the CPU increases, and the size of the encoder output decreases slightly.</span></span> <span data-ttu-id="03271-120">L'output è lossless indipendentemente dal valore di questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="03271-120">The output is lossless regardless of the value of this property.</span></span>

<span data-ttu-id="03271-121">Se si lascia questa proprietà sul valore predefinito **Variant \_ false**, il codificatore usa l'algoritmo predefinito.</span><span class="sxs-lookup"><span data-stu-id="03271-121">If you leave this property at its default value of **VARIANT\_FALSE**, the encoder uses its default algorithm.</span></span> <span data-ttu-id="03271-122">L'algoritmo predefinito dipende dal codificatore in uso e dalla versione di Windows in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="03271-122">The default algorithm depends on which encoder you are using and which version of Windows is running.</span></span> <span data-ttu-id="03271-123">Nella tabella seguente viene descritto il comportamento predefinito per le diverse combinazioni.</span><span class="sxs-lookup"><span data-stu-id="03271-123">The following table describes the default behavior for the different combinations.</span></span>



| <span data-ttu-id="03271-124">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="03271-124">Operating system</span></span> | <span data-ttu-id="03271-125">Comportamento predefinito</span><span class="sxs-lookup"><span data-stu-id="03271-125">Default behavior</span></span>                                                                                                                                                                                                |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03271-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="03271-126">Windows Vista</span></span>    | <span data-ttu-id="03271-127">Per impostazione predefinita, i codificatori Windows Media Audio 10, Windows Media Audio 10 Professional e Windows Media Audio 10 Lossless utilizzano l'algoritmo più complesso.</span><span class="sxs-lookup"><span data-stu-id="03271-127">The Windows Media Audio 10, Windows Media Audio 10 Professional, and Windows Media Audio 10 Lossless encoders all use the most complex algorithm by default.</span></span>                                                    |
| <span data-ttu-id="03271-128">Windows 7</span><span class="sxs-lookup"><span data-stu-id="03271-128">Windows 7</span></span>        | <span data-ttu-id="03271-129">Per impostazione predefinita, i codificatori Windows Media Audio 10 e Windows Media Audio 10 Professional utilizzano l'algoritmo più complesso.</span><span class="sxs-lookup"><span data-stu-id="03271-129">The Windows Media Audio 10 and Windows Media Audio 10 Professional encoders use the most complex algorithm by default.</span></span> <span data-ttu-id="03271-130">Per impostazione predefinita, il codificatore Windows Media Audio 10 Lossless usa l'algoritmo meno complesso.</span><span class="sxs-lookup"><span data-stu-id="03271-130">The Windows Media Audio 10 Lossless encoder uses the least complex algorithm by default.</span></span> |



 

<span data-ttu-id="03271-131">Se la proprietà [**MFPKEY \_ CONSTRAINECOMPLEXITY**](mfpkey-constrainenccomplexityproperty.md) ha un valore **Variant \_ false**, il codificatore ignora questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="03271-131">If the [**MFPKEY\_CONSTRAINECOMPLEXITY**](mfpkey-constrainenccomplexityproperty.md) property has a value of **VARIANT\_FALSE**, the encoder ignores this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="03271-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="03271-132">Requirements</span></span>



| <span data-ttu-id="03271-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="03271-133">Requirement</span></span> | <span data-ttu-id="03271-134">Valore</span><span class="sxs-lookup"><span data-stu-id="03271-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="03271-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03271-135">Minimum supported client</span></span><br/> | <span data-ttu-id="03271-136">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="03271-136">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="03271-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03271-137">Minimum supported server</span></span><br/> | <span data-ttu-id="03271-138">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="03271-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="03271-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="03271-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="03271-140"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="03271-140"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03271-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="03271-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03271-142">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="03271-142">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
