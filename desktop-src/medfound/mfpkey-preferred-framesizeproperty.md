---
description: Specifica il numero preferito di campioni per fotogramma.
ms.assetid: ad629dbd-49d8-43d0-95a8-03f2043e397e
title: Proprietà MFPKEY_PREFERRED_FRAMESIZE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fe04ad37c6cd684e3179cbd16328346fd6f11dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333090"
---
# <a name="mfpkey_preferred_framesize-property"></a><span data-ttu-id="2e877-103">\_ \_ Proprietà FRAMESIZE preferita MFPKEY</span><span class="sxs-lookup"><span data-stu-id="2e877-103">MFPKEY\_PREFERRED\_FRAMESIZE Property</span></span>

<span data-ttu-id="2e877-104">Specifica il numero preferito di campioni per fotogramma.</span><span class="sxs-lookup"><span data-stu-id="2e877-104">Specifies the preferred number of samples per frame.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="2e877-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="2e877-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="2e877-106">Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="2e877-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="2e877-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="2e877-107">Data Type</span></span>

<span data-ttu-id="2e877-108">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="2e877-108">**VT\_UI4**</span></span>

## <a name="remarks"></a><span data-ttu-id="2e877-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="2e877-109">Remarks</span></span>

<span data-ttu-id="2e877-110">Per specificare una dimensione del fotogramma preferita, impostare le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="2e877-110">To specifiy a preferred frame size, set the following properties.</span></span>

-   <span data-ttu-id="2e877-111">Impostare [**MFPKEY che \_ richiede \_ un \_ FRAMESIZE**](mfpkey-requesting-a-framesizeproperty.md) a **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="2e877-111">Set [**MFPKEY\_REQUESTING\_A\_FRAMESIZE**](mfpkey-requesting-a-framesizeproperty.md) to **VARIANT\_TRUE**.</span></span>
-   <span data-ttu-id="2e877-112">Impostare **MFPKEY \_ preferenziale \_ FRAMESIZE** sul numero di campioni desiderato in ogni frame.</span><span class="sxs-lookup"><span data-stu-id="2e877-112">Set **MFPKEY\_PREFERRED\_FRAMESIZE** to the number of samples you want in each frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e877-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2e877-113">Requirements</span></span>



| <span data-ttu-id="2e877-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e877-114">Requirement</span></span> | <span data-ttu-id="2e877-115">Valore</span><span class="sxs-lookup"><span data-stu-id="2e877-115">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e877-116">Client</span><span class="sxs-lookup"><span data-stu-id="2e877-116">Client</span></span><br/> | <span data-ttu-id="2e877-117">Windows Vista o Windows 7</span><span class="sxs-lookup"><span data-stu-id="2e877-117">Windows Vista or Windows 7</span></span><br/>                                                   |
| <span data-ttu-id="2e877-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2e877-118">Header</span></span><br/> | <dl> <span data-ttu-id="2e877-119"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e877-119"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e877-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2e877-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e877-121">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2e877-121">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
