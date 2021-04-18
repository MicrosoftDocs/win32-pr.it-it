---
description: Specifica le impostazioni ottimali per la qualità visiva da usare per il codificatore di profili avanzato Windows Media Video 9.
ms.assetid: 9449b5fa-4f13-4c33-bfdf-611720e8dd77
title: Proprietà MFPKEY_COMPRESSIONOPTIMIZATIONTYPE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3000caa10aa7db7d201cd11fd9a189fd6ac33591
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310647"
---
# <a name="mfpkey_compressionoptimizationtype-property"></a><span data-ttu-id="04cc4-103">\_Proprietà COMPRESSIONOPTIMIZATIONTYPE di MFPKEY</span><span class="sxs-lookup"><span data-stu-id="04cc4-103">MFPKEY\_COMPRESSIONOPTIMIZATIONTYPE Property</span></span>

<span data-ttu-id="04cc4-104">Specifica le impostazioni ottimali per la qualità visiva da usare per il codificatore di profili avanzato Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="04cc4-104">Specifies the optimal visual quality settings to use for the Windows Media Video 9 Advanced Profile encoder.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="04cc4-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="04cc4-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="04cc4-106">g \_ wszWMVCCompressionOptimizationType</span><span class="sxs-lookup"><span data-stu-id="04cc4-106">g\_wszWMVCCompressionOptimizationType</span></span>

## <a name="data-type"></a><span data-ttu-id="04cc4-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="04cc4-107">Data Type</span></span>

<span data-ttu-id="04cc4-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="04cc4-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="04cc4-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="04cc4-109">Default Value</span></span>

<span data-ttu-id="04cc4-110">0</span><span class="sxs-lookup"><span data-stu-id="04cc4-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="04cc4-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="04cc4-111">Remarks</span></span>

<span data-ttu-id="04cc4-112">Questa proprietà fornisce un modo rapido per configurare una serie di opzioni di codifica video.</span><span class="sxs-lookup"><span data-stu-id="04cc4-112">This property provides a quick way to configure a number of video encoding options.</span></span> <span data-ttu-id="04cc4-113">Può essere impostato su uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="04cc4-113">It may be set to one of the following values.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="04cc4-114">Valore</span><span class="sxs-lookup"><span data-stu-id="04cc4-114">Value</span></span></th>
<th><span data-ttu-id="04cc4-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="04cc4-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="04cc4-116">0</span><span class="sxs-lookup"><span data-stu-id="04cc4-116">0</span></span></td>
<td><span data-ttu-id="04cc4-117">Il codec non forza l'ottimizzazione e utilizzerà tutte le funzionalità specificate da altre proprietà.</span><span class="sxs-lookup"><span data-stu-id="04cc4-117">The codec will not force optimization and will use whatever features are specified by other properties.</span></span> <span data-ttu-id="04cc4-118">In molti casi, il codec userà la logica interna per determinare le impostazioni se non sono specificate.</span><span class="sxs-lookup"><span data-stu-id="04cc4-118">In many cases, the codec will use internal logic to determine settings if they are not specified.</span></span> <span data-ttu-id="04cc4-119">Rappresenta il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="04cc4-119">This is the default value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04cc4-120">1</span><span class="sxs-lookup"><span data-stu-id="04cc4-120">1</span></span></td>
<td><span data-ttu-id="04cc4-121">Abilita le funzionalità che produrranno la qualità visiva migliore. L'uso di questo valore consente di configurare il codec come se fossero state impostate le proprietà seguenti:</span><span class="sxs-lookup"><span data-stu-id="04cc4-121">Enables the features that will produce the best visual quality.Using this value configures the codec as if you had set the following properties:</span></span><br/>
<ul>
<li><span data-ttu-id="04cc4-122"><a href="mfpkey-bdeltaqpproperty.md">MFPKEY_BDELTAQP</a> = 1</span><span class="sxs-lookup"><span data-stu-id="04cc4-122"><a href="mfpkey-bdeltaqpproperty.md">MFPKEY_BDELTAQP</a> = 1</span></span></li>
<li><span data-ttu-id="04cc4-123"><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a> = 3</span><span class="sxs-lookup"><span data-stu-id="04cc4-123"><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a> = 3</span></span></li>
<li><span data-ttu-id="04cc4-124"><a href="mfpkey-loopfilterproperty.md">MFPKEY_LOOPFILTER</a> = 1</span><span class="sxs-lookup"><span data-stu-id="04cc4-124"><a href="mfpkey-loopfilterproperty.md">MFPKEY_LOOPFILTER</a> = 1</span></span></li>
<li><span data-ttu-id="04cc4-125"><a href="mfpkey-motionmatchmethodproperty.md">MFPKEY_MOTIONMATCHMETHOD</a> =-1</span><span class="sxs-lookup"><span data-stu-id="04cc4-125"><a href="mfpkey-motionmatchmethodproperty.md">MFPKEY_MOTIONMATCHMETHOD</a> = -1</span></span></li>
<li><span data-ttu-id="04cc4-126"><a href="mfpkey-motionsearchlevelproperty.md">MFPKEY_MOTIONSEARCHLEVEL</a> = 1</span><span class="sxs-lookup"><span data-stu-id="04cc4-126"><a href="mfpkey-motionsearchlevelproperty.md">MFPKEY_MOTIONSEARCHLEVEL</a> = 1</span></span></li>
<li><span data-ttu-id="04cc4-127"><a href="mfpkey-motionsearchrangeproperty.md">MFPKEY_MOTIONSEARCHRANGE</a> =-1</span><span class="sxs-lookup"><span data-stu-id="04cc4-127"><a href="mfpkey-motionsearchrangeproperty.md">MFPKEY_MOTIONSEARCHRANGE</a> = -1</span></span></li>
<li><span data-ttu-id="04cc4-128"><a href="mfpkey-numbframesproperty.md">MFPKEY_NUMBFRAMES</a> = 1</span><span class="sxs-lookup"><span data-stu-id="04cc4-128"><a href="mfpkey-numbframesproperty.md">MFPKEY_NUMBFRAMES</a> = 1</span></span></li>
</ul>
<span data-ttu-id="04cc4-129">Se si imposta una delle proprietà nell'elenco precedente, il valore impostato sostituisce i valori associati a questa impostazione, ad eccezione di <a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a>.</span><span class="sxs-lookup"><span data-stu-id="04cc4-129">If you set any of the properties in the previous list, the value you set overrides the values associated with this setting, except for <a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="04cc4-130">Impostando il valore della \_ Proprietà COMPRESSIONOPTIMIZATIONTYPE di MFPKEY su 1, l'impostazione dell'opzione DQuant del registro di sistema è impostata su 2 e l'impostazione del registro di sistema del metodo di costo del vettore di movimento su 1.</span><span class="sxs-lookup"><span data-stu-id="04cc4-130">Setting the value of the MFPKEY\_COMPRESSIONOPTIMIZATIONTYPE property to 1 also has the effect of setting the Dquant Option registry setting to 2, and the Motion Vector Cost Method registry setting to 1.</span></span> <span data-ttu-id="04cc4-131">Per altre informazioni, vedere l'articolo relativo all' [uso delle impostazioni avanzate del codec del profilo avanzato Windows Media video 9](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx).</span><span class="sxs-lookup"><span data-stu-id="04cc4-131">For more information, see the web article [Using the Advanced Settings of the Windows Media Video 9 Advanced Profile Codec](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx).</span></span>

## <a name="requirements"></a><span data-ttu-id="04cc4-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04cc4-132">Requirements</span></span>



| <span data-ttu-id="04cc4-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="04cc4-133">Requirement</span></span> | <span data-ttu-id="04cc4-134">Valore</span><span class="sxs-lookup"><span data-stu-id="04cc4-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="04cc4-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="04cc4-135">Minimum supported client</span></span><br/> | <span data-ttu-id="04cc4-136">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="04cc4-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="04cc4-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="04cc4-137">Minimum supported server</span></span><br/> | <span data-ttu-id="04cc4-138">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="04cc4-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="04cc4-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="04cc4-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="04cc4-140"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="04cc4-140"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04cc4-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="04cc4-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04cc4-142">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="04cc4-142">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




