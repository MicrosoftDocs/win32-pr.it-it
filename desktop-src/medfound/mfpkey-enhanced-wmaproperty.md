---
description: Specifica se il codificatore principale usa il &\# 0034; Più&\# 0034; funzionalità.
ms.assetid: 1ace09da-7dee-469e-a533-63b40ac747ab
title: Proprietà MFPKEY_ENHANCED_WMA (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df1c7ddc0e7bfb6d62d51e535f10b257eac6f2ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333535"
---
# <a name="mfpkey_enhanced_wma-property"></a><span data-ttu-id="b6dd6-103">\_ \_ Proprietà WMA avanzata MFPKEY</span><span class="sxs-lookup"><span data-stu-id="b6dd6-103">MFPKEY\_ENHANCED\_WMA Property</span></span>

<span data-ttu-id="b6dd6-104">Specifica se il codificatore principale utilizza la funzionalità "più".</span><span class="sxs-lookup"><span data-stu-id="b6dd6-104">Specifies whether the core encoder uses the "Plus" feature.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="b6dd6-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="b6dd6-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="b6dd6-106">Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="b6dd6-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="b6dd6-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="b6dd6-107">Data Type</span></span>

<span data-ttu-id="b6dd6-108">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="b6dd6-108">**VT\_UI4**</span></span>

## <a name="default-value"></a><span data-ttu-id="b6dd6-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="b6dd6-109">Default Value</span></span>

<span data-ttu-id="b6dd6-110">0</span><span class="sxs-lookup"><span data-stu-id="b6dd6-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="b6dd6-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="b6dd6-111">Remarks</span></span>

<span data-ttu-id="b6dd6-112">Questa proprietà è disponibile solo per Windows Media Audio Lossless.</span><span class="sxs-lookup"><span data-stu-id="b6dd6-112">This property is available only for Windows Media Audio Lossless.</span></span>

<span data-ttu-id="b6dd6-113">Se si lascia questa proprietà sul valore predefinito 0 oppure se si imposta su 1, il codificatore Core decide se utilizzare la parte "più".</span><span class="sxs-lookup"><span data-stu-id="b6dd6-113">If you leave this property at its default value of 0, or if you set it to 1, the core encoder decides whether the "Plus" portion should be used.</span></span> <span data-ttu-id="b6dd6-114">Se si imposta questa proprietà su 2, il codificatore principale non userà la funzionalità "Plus".</span><span class="sxs-lookup"><span data-stu-id="b6dd6-114">If you set this property to 2, the core encoder does not use the "Plus" feature.</span></span>

<span data-ttu-id="b6dd6-115">Questa proprietà modifica i tipi di supporto enumerati, pertanto se si imposta è necessario eseguire questa operazione prima di impostare il tipo di output.</span><span class="sxs-lookup"><span data-stu-id="b6dd6-115">This property alters the enumerated media types, so if you set it, you must do so before you set the output type.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6dd6-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b6dd6-116">Requirements</span></span>



| <span data-ttu-id="b6dd6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6dd6-117">Requirement</span></span> | <span data-ttu-id="b6dd6-118">Valore</span><span class="sxs-lookup"><span data-stu-id="b6dd6-118">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6dd6-119">Client</span><span class="sxs-lookup"><span data-stu-id="b6dd6-119">Client</span></span><br/> | <span data-ttu-id="b6dd6-120">Windows Vista o Windows 7</span><span class="sxs-lookup"><span data-stu-id="b6dd6-120">Windows Vista or Windows 7</span></span><br/>                                                   |
| <span data-ttu-id="b6dd6-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b6dd6-121">Header</span></span><br/> | <dl> <span data-ttu-id="b6dd6-122"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6dd6-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6dd6-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b6dd6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6dd6-124">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b6dd6-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
