---
description: Specifica se il decodificatore deve eseguire Lt-Rt riduzioni.
ms.assetid: ce1dc4ea-4326-40ab-bb30-ff1a34f06d79
title: Proprietà MFPKEY_WMADEC_LTRTOUTPUT (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4f4a83d2529ce3b37282be35924b48288d4df45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130542"
---
# <a name="mfpkey_wmadec_ltrtoutput-property"></a><span data-ttu-id="7e8f2-103">MFPKEY \_ WMADEC- \_ Proprietà LTRTOUTPUT</span><span class="sxs-lookup"><span data-stu-id="7e8f2-103">MFPKEY\_WMADEC\_LTRTOUTPUT Property</span></span>

<span data-ttu-id="7e8f2-104">Specifica se il decodificatore deve eseguire Lt-Rt riduzioni.</span><span class="sxs-lookup"><span data-stu-id="7e8f2-104">Specifies whether the decoder should perform Lt-Rt fold down.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="7e8f2-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="7e8f2-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="7e8f2-106">Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="7e8f2-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="7e8f2-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="7e8f2-107">Data Type</span></span>

<span data-ttu-id="7e8f2-108">**\_bool VT**</span><span class="sxs-lookup"><span data-stu-id="7e8f2-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="7e8f2-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="7e8f2-109">Default Value</span></span>

<span data-ttu-id="7e8f2-110">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="7e8f2-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="7e8f2-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="7e8f2-111">Remarks</span></span>

<span data-ttu-id="7e8f2-112">Se questa proprietà presenta un valore VARIANT \_ false e l'output è stereo, il decodificatore audio utilizza una semplice riduzione del canale.</span><span class="sxs-lookup"><span data-stu-id="7e8f2-112">If this property has a value of VARIANT\_FALSE and the output is stereo, the audio decoder uses simple channel fold down.</span></span> <span data-ttu-id="7e8f2-113">Se questa proprietà ha un valore VARIANT \_ true, il decodificatore audio esegue Lt-Rt (matrici) ripiegare verso il basso fino a stereo e quindi qualsiasi decodificatore Dolby surround può essere usato per decodificare il racchiuso in matrici.</span><span class="sxs-lookup"><span data-stu-id="7e8f2-113">If this property has a value of VARIANT\_TRUE, the audio decoder performs Lt-Rt (matrixed) fold down to stereo, and then any Dolby Surround decoder can be used to decode the matrixed surround .</span></span> <span data-ttu-id="7e8f2-114">Ad esempio, il decodificatore audio potrebbe eseguire Lt-Rt riduzione del contenuto 5,1 o 7,1.</span><span class="sxs-lookup"><span data-stu-id="7e8f2-114">For example, the audio decoder could perform Lt-Rt fold down on 5.1 or 7.1 content.</span></span>

<span data-ttu-id="7e8f2-115">Questa proprietà è supportata solo quando il decodificatore funge da oggetto DMO (DirectX Media Object).</span><span class="sxs-lookup"><span data-stu-id="7e8f2-115">This property is supported only when the decoder is acting as a DirectX Media Object (DMO).</span></span> <span data-ttu-id="7e8f2-116">Se il decodificatore funge da Media Foundation trasformazione (MFT), non è supportata alcuna riduzione di alcun tipo.</span><span class="sxs-lookup"><span data-stu-id="7e8f2-116">No fold down of any kind is supported when the decoder is acting as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="7e8f2-117">In Windows Vista, se si ottiene un'interfaccia **IPropertyStore** su un decoder audio, il decodificatore funge da MFT.</span><span class="sxs-lookup"><span data-stu-id="7e8f2-117">On Windows Vista, if you obtain an **IPropertyStore** interface on an audio decoder, the decoder acts as an MFT.</span></span> <span data-ttu-id="7e8f2-118">Di conseguenza, questa proprietà non può essere utilizzata in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7e8f2-118">Consequently, this property cannot be used on Windows Vista.</span></span> <span data-ttu-id="7e8f2-119">Per informazioni su quando un decodificatore funge da DMO o da un MFT, vedere le pagine di riferimento del singolo codec in [oggetti codec](codecobjects.md).</span><span class="sxs-lookup"><span data-stu-id="7e8f2-119">For information on when a decoder acts as a DMO or an MFT, see the individual codec reference pages under [Codec Objects](codecobjects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7e8f2-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7e8f2-120">Requirements</span></span>



| <span data-ttu-id="7e8f2-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e8f2-121">Requirement</span></span> | <span data-ttu-id="7e8f2-122">Valore</span><span class="sxs-lookup"><span data-stu-id="7e8f2-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e8f2-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7e8f2-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7e8f2-124">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7e8f2-124">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7e8f2-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7e8f2-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7e8f2-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7e8f2-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7e8f2-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7e8f2-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e8f2-128"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e8f2-128"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e8f2-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7e8f2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e8f2-130">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7e8f2-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
