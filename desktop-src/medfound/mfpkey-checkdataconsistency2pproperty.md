---
description: Specifica se il codificatore deve verificare la coerenza dei dati tra i passaggi quando si esegue la codifica VBR a due passaggi. Lettura/scrittura.
ms.assetid: 68750820-e931-41c2-9d12-89ab83b4b97e
title: Proprietà MFPKEY_CHECKDATACONSISTENCY2P (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abc706712ef1e8bff36a118031fde155bb9bda31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324706"
---
# <a name="mfpkey_checkdataconsistency2p-property"></a><span data-ttu-id="34b3f-104">\_Proprietà CHECKDATACONSISTENCY2P di MFPKEY</span><span class="sxs-lookup"><span data-stu-id="34b3f-104">MFPKEY\_CHECKDATACONSISTENCY2P Property</span></span>

<span data-ttu-id="34b3f-105">Specifica se il codificatore deve verificare la coerenza dei dati tra i passaggi quando si esegue la codifica VBR a due passaggi.</span><span class="sxs-lookup"><span data-stu-id="34b3f-105">Specifies whether whether the encoder should check for data consistency across passes when performing two-pass VBR encoding.</span></span> <span data-ttu-id="34b3f-106">Lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="34b3f-106">Read-write.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="34b3f-107">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="34b3f-107">Constant for IPropertyBag</span></span>

<span data-ttu-id="34b3f-108">Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="34b3f-108">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="34b3f-109">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="34b3f-109">Data Type</span></span>

<span data-ttu-id="34b3f-110">**\_bool VT**</span><span class="sxs-lookup"><span data-stu-id="34b3f-110">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="34b3f-111">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="34b3f-111">Default Value</span></span>

<span data-ttu-id="34b3f-112">**VARIANT \_ true**</span><span class="sxs-lookup"><span data-stu-id="34b3f-112">**VARIANT\_TRUE**</span></span>

## <a name="remarks"></a><span data-ttu-id="34b3f-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="34b3f-113">Remarks</span></span>

<span data-ttu-id="34b3f-114">Se si lascia questa proprietà sul valore predefinito **Variant \_ true**, il codificatore verifica che gli esempi di input corrispondano tra le due sessioni e non riesce se rileva una discrepanza.</span><span class="sxs-lookup"><span data-stu-id="34b3f-114">If you leave this property at its default value of **VARIANT\_TRUE**, the encoder verifies that the input samples match between the two passes, and fails if it detects a discrepancy.</span></span> <span data-ttu-id="34b3f-115">Lo scenario principale che causa una discrepanza consiste nel momento in cui l'input deriva da un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="34b3f-115">The main scenario that leads to a discrepancy is when the input comes from a device.</span></span>

## <a name="requirements"></a><span data-ttu-id="34b3f-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="34b3f-116">Requirements</span></span>



| <span data-ttu-id="34b3f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="34b3f-117">Requirement</span></span> | <span data-ttu-id="34b3f-118">Valore</span><span class="sxs-lookup"><span data-stu-id="34b3f-118">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="34b3f-119">Client</span><span class="sxs-lookup"><span data-stu-id="34b3f-119">Client</span></span><br/> | <span data-ttu-id="34b3f-120">Windows Vista o Windows 7</span><span class="sxs-lookup"><span data-stu-id="34b3f-120">Windows Vista or Windows 7</span></span><br/>                                                   |
| <span data-ttu-id="34b3f-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="34b3f-121">Header</span></span><br/> | <dl> <span data-ttu-id="34b3f-122"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="34b3f-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34b3f-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="34b3f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34b3f-124">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="34b3f-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
