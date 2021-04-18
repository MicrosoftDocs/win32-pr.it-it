---
description: Specifica se il codificatore è vincolato da un requisito di latenza del decodificatore massimo.
ms.assetid: 054e445e-fc71-4d4f-9e9f-f5ff71f0b4ee
title: Proprietà MFPKEY_CONSTRAINDECLATENCY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 343bcc9bd365b9f1321b200baa203fc27784594c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310646"
---
# <a name="mfpkey_constraindeclatency-property"></a><span data-ttu-id="17a31-103">\_Proprietà CONSTRAINDECLATENCY di MFPKEY</span><span class="sxs-lookup"><span data-stu-id="17a31-103">MFPKEY\_CONSTRAINDECLATENCY Property</span></span>

<span data-ttu-id="17a31-104">Specifica se il codificatore è vincolato da un requisito di latenza del decodificatore massimo.</span><span class="sxs-lookup"><span data-stu-id="17a31-104">Specifies whether the encoder is constrained by a maximum decoder latency requirement.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="17a31-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="17a31-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="17a31-106">Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="17a31-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="17a31-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="17a31-107">Data Type</span></span>

<span data-ttu-id="17a31-108">**\_bool VT**</span><span class="sxs-lookup"><span data-stu-id="17a31-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="17a31-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="17a31-109">Default Value</span></span>

<span data-ttu-id="17a31-110">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="17a31-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="17a31-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="17a31-111">Remarks</span></span>

<span data-ttu-id="17a31-112">Se si lascia questa proprietà sul valore predefinito **Variant \_ false**, il codificatore enumera un set predefinito di modalità con circa 1500 millisecondi di latenza del decodificatore.</span><span class="sxs-lookup"><span data-stu-id="17a31-112">If you leave this property at its default value of **VARIANT\_FALSE**, the encoder enumerates a default set of modes that have about 1500 milliseconds of decoder latency.</span></span> <span data-ttu-id="17a31-113">Se si imposta questa proprietà su **Variant \_ true**, è necessario specificare anche una latenza di decodificazione massima impostando la proprietà [**MFPKEY \_ MAXDECLATENCYMS**](mfpkey-maxdeclatencymsproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="17a31-113">If you set this property to **VARIANT\_TRUE**, you must also specify a maximum decoder latency by setting the [**MFPKEY\_MAXDECLATENCYMS**](mfpkey-maxdeclatencymsproperty.md) property.</span></span> <span data-ttu-id="17a31-114">In tal caso, il codificatore crea le modalità che soddisfano il requisito di latenza ed enumera solo le modalità.</span><span class="sxs-lookup"><span data-stu-id="17a31-114">In that case, the encoder creates modes that satisfy the latency requirement and enumerates only those modes.</span></span> <span data-ttu-id="17a31-115">Il codificatore garantisce che i requisiti di preroll (dimensione del buffer del decodificatore) siano minori o uguali a **MFPKEY \_ MAXDECLATENCYMS**.</span><span class="sxs-lookup"><span data-stu-id="17a31-115">The encoder ensures that the preroll requirements (decoder buffer size) are less than or equal to **MFPKEY\_MAXDECLATENCYMS**.</span></span>

## <a name="requirements"></a><span data-ttu-id="17a31-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="17a31-116">Requirements</span></span>



| <span data-ttu-id="17a31-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="17a31-117">Requirement</span></span> | <span data-ttu-id="17a31-118">Valore</span><span class="sxs-lookup"><span data-stu-id="17a31-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17a31-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17a31-119">Minimum supported client</span></span><br/> | <span data-ttu-id="17a31-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="17a31-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="17a31-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17a31-121">Minimum supported server</span></span><br/> | <span data-ttu-id="17a31-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="17a31-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="17a31-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="17a31-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="17a31-124"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="17a31-124"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17a31-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="17a31-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17a31-126">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="17a31-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
