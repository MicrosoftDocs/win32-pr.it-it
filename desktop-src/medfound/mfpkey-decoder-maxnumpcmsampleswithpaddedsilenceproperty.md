---
description: Specifica il numero massimo di campioni PCM aggiuntivi che potrebbero essere restituiti alla fine di dopo la decodifica di un file.
ms.assetid: 82b3676c-7653-421c-aac7-7f20a642779f
title: Proprietà MFPKEY_Decoder_MaxNumPCMSamplesWithPaddedSilence (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b1f97b55c2eedd8cc7d6d524379569073fa35d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310640"
---
# <a name="mfpkey_decoder_maxnumpcmsampleswithpaddedsilence-property"></a><span data-ttu-id="003f3-103">\_Proprietà MaxNumPCMSamplesWithPaddedSilence del decodificatore MFPKEY \_</span><span class="sxs-lookup"><span data-stu-id="003f3-103">MFPKEY\_Decoder\_MaxNumPCMSamplesWithPaddedSilence Property</span></span>

<span data-ttu-id="003f3-104">Specifica il numero massimo di campioni PCM aggiuntivi che potrebbero essere restituiti alla fine di dopo la decodifica di un file.</span><span class="sxs-lookup"><span data-stu-id="003f3-104">Specifies the maximum number of additional PCM samples that might be returned at the end of after decoding a file.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="003f3-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="003f3-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="003f3-106">Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="003f3-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="003f3-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="003f3-107">Data Type</span></span>

<span data-ttu-id="003f3-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="003f3-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="003f3-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="003f3-109">Default Value</span></span>

<span data-ttu-id="003f3-110">2048</span><span class="sxs-lookup"><span data-stu-id="003f3-110">2048</span></span>

## <a name="remarks"></a><span data-ttu-id="003f3-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="003f3-111">Remarks</span></span>

<span data-ttu-id="003f3-112">Questa proprietà può essere usata per stimare il silenzio artificiale che viene inserito tra i brani Man mano che vengono inseriti nel decodificatore uno dopo l'altro.</span><span class="sxs-lookup"><span data-stu-id="003f3-112">This property can be used to estimate artificial silence that gets is inserted between songs as they are fed to the decoder one after another.</span></span>

<span data-ttu-id="003f3-113">Per i decodificatori senza perdita di Windows Media Audio 10 Professional e Windows Media Audio 9, questa proprietà è sempre uguale a 0.</span><span class="sxs-lookup"><span data-stu-id="003f3-113">For the Windows Media Audio 10 Professional and Windows Media Audio 9 Lossless decoders, this property is always equal to 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="003f3-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="003f3-114">Requirements</span></span>



| <span data-ttu-id="003f3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="003f3-115">Requirement</span></span> | <span data-ttu-id="003f3-116">Valore</span><span class="sxs-lookup"><span data-stu-id="003f3-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="003f3-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="003f3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="003f3-118">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="003f3-118">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="003f3-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="003f3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="003f3-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="003f3-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="003f3-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="003f3-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="003f3-122"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="003f3-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="003f3-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="003f3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="003f3-124">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="003f3-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
