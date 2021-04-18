---
description: Specifica il livello di volume medio del contenuto audio.
ms.assetid: eabb36ff-300f-4ed1-aca3-9415627ac1a7
title: Proprietà MFPKEY_WMADRC_AVGREF (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf18c37b00f84cc3ae3fdf1f44b2fbefcc56d9f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309110"
---
# <a name="mfpkey_wmadrc_avgref-property"></a><span data-ttu-id="fde8f-103">MFPKEY \_ WMADRC- \_ Proprietà AVGREF</span><span class="sxs-lookup"><span data-stu-id="fde8f-103">MFPKEY\_WMADRC\_AVGREF Property</span></span>

<span data-ttu-id="fde8f-104">Specifica il livello di volume medio del contenuto audio.</span><span class="sxs-lookup"><span data-stu-id="fde8f-104">Specifies the average volume level of audio content.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="fde8f-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="fde8f-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="fde8f-106">g \_ wszWMADRCAverageReference</span><span class="sxs-lookup"><span data-stu-id="fde8f-106">g\_wszWMADRCAverageReference</span></span>

## <a name="data-type"></a><span data-ttu-id="fde8f-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="fde8f-107">Data Type</span></span>

<span data-ttu-id="fde8f-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="fde8f-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="fde8f-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="fde8f-109">Remarks</span></span>

<span data-ttu-id="fde8f-110">È possibile ottenere questo valore dal codificatore dopo l'elaborazione del contenuto.</span><span class="sxs-lookup"><span data-stu-id="fde8f-110">You can get this value from the encoder after the content is processed.</span></span> <span data-ttu-id="fde8f-111">Questo valore può essere impostato anche nel decodificatore allo scopo di un controllo intervallo dinamico, ma avrà effetto solo se è impostata la proprietà [MFPKEY \_ WMADEC \_ DRCMODE](mfpkey-wmadec-drcmodeproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="fde8f-111">This value can also be set on the decoder for the purpose of dynamic range control, but it will have an effect only if the [MFPKEY\_WMADEC\_DRCMODE](mfpkey-wmadec-drcmodeproperty.md) property is set.</span></span>

<span data-ttu-id="fde8f-112">Per ulteriori informazioni sul controllo dinamico degli intervalli, vedere l'articolo Web [Windows Media audio funzionalità dei codec professionali](/previous-versions/ms867218(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="fde8f-112">For more information on dynamic range control see the web article [Windows Media Audio Professional Codec Features](/previous-versions/ms867218(v=msdn.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="fde8f-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fde8f-113">Requirements</span></span>



| <span data-ttu-id="fde8f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fde8f-114">Requirement</span></span> | <span data-ttu-id="fde8f-115">Valore</span><span class="sxs-lookup"><span data-stu-id="fde8f-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fde8f-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fde8f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fde8f-117">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="fde8f-117">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="fde8f-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fde8f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fde8f-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fde8f-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fde8f-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fde8f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fde8f-121"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fde8f-121"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fde8f-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fde8f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fde8f-123">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fde8f-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
