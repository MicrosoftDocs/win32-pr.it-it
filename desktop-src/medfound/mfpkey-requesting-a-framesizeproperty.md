---
description: Specifica se il codificatore deve usare una dimensione del frame preferita specificata in numero di campioni per fotogramma.
ms.assetid: c9baeff7-53fb-425f-b07b-4066a705ca54
title: Proprietà MFPKEY_REQUESTING_A_FRAMESIZE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3355e84318ba4ad7995ac5ad0f002f4d70767b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333808"
---
# <a name="mfpkey_requesting_a_framesize-property"></a><span data-ttu-id="89cb5-103">MFPKEY che \_ richiede \_ una \_ Proprietà FRAMESIZE</span><span class="sxs-lookup"><span data-stu-id="89cb5-103">MFPKEY\_REQUESTING\_A\_FRAMESIZE Property</span></span>

<span data-ttu-id="89cb5-104">Specifica se il codificatore deve usare una dimensione del frame preferita specificata in numero di campioni per fotogramma.</span><span class="sxs-lookup"><span data-stu-id="89cb5-104">Specifies whether the encoder should use a preferred frame size given in number of samples per frame.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="89cb5-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="89cb5-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="89cb5-106">Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="89cb5-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="89cb5-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="89cb5-107">Data Type</span></span>

<span data-ttu-id="89cb5-108">**\_bool VT**</span><span class="sxs-lookup"><span data-stu-id="89cb5-108">**VT\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="89cb5-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="89cb5-109">Remarks</span></span>

<span data-ttu-id="89cb5-110">Per specificare una dimensione del fotogramma preferita, impostare le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="89cb5-110">To specifiy a preferred frame size, set the following properties.</span></span>

-   <span data-ttu-id="89cb5-111">Impostare **MFPKEY che \_ richiede \_ un \_ FRAMESIZE** a Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="89cb5-111">Set **MFPKEY\_REQUESTING\_A\_FRAMESIZE** to VARIANT\_TRUE.</span></span>
-   <span data-ttu-id="89cb5-112">Impostare [**MFPKEY \_ preferenziale \_ FRAMESIZE**](mfpkey-preferred-framesizeproperty.md) sul numero di campioni desiderato in ogni frame.</span><span class="sxs-lookup"><span data-stu-id="89cb5-112">Set [**MFPKEY\_PREFERRED\_FRAMESIZE**](mfpkey-preferred-framesizeproperty.md) to the number of samples you want in each frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="89cb5-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="89cb5-113">Requirements</span></span>



| <span data-ttu-id="89cb5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="89cb5-114">Requirement</span></span> | <span data-ttu-id="89cb5-115">Valore</span><span class="sxs-lookup"><span data-stu-id="89cb5-115">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="89cb5-116">Client</span><span class="sxs-lookup"><span data-stu-id="89cb5-116">Client</span></span><br/> | <span data-ttu-id="89cb5-117">Windows Vista o Windows 7</span><span class="sxs-lookup"><span data-stu-id="89cb5-117">Windows Vista or Windows 7</span></span><br/>                                                   |
| <span data-ttu-id="89cb5-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="89cb5-118">Header</span></span><br/> | <dl> <span data-ttu-id="89cb5-119"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="89cb5-119"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89cb5-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="89cb5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89cb5-121">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="89cb5-121">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
