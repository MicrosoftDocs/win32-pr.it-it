---
description: Il tipo di enumerazione WpdAttributeForm descrive il modo in cui una proprietà archivia i valori.
ms.assetid: 3ad8d1f9-1b74-4f34-9af5-1acdd588b650
title: Enumerazione WpdAttributeForm (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WpdAttributeForm
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 4c70f68dc04adcb454fcc7c5ae301f0dabf60c28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333520"
---
# <a name="wpdattributeform-enumeration"></a><span data-ttu-id="c8b51-103">Enumerazione WpdAttributeForm</span><span class="sxs-lookup"><span data-stu-id="c8b51-103">WpdAttributeForm enumeration</span></span>

<span data-ttu-id="c8b51-104">Il tipo di enumerazione **WpdAttributeForm** descrive il modo in cui una proprietà archivia i valori.</span><span class="sxs-lookup"><span data-stu-id="c8b51-104">The **WpdAttributeForm** enumeration type describes how a property stores its values.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8b51-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c8b51-105">Syntax</span></span>


```C++
typedef enum WpdAttributeForm { 
  WPD_PROPERTY_ATTRIBUTE_FORM_UNSPECIFIED         = 0,
  WPD_PROPERTY_ATTRIBUTE_FORM_RANGE               = 1,
  WPD_PROPERTY_ATTRIBUTE_FORM_ENUMERATION         = 2,
  WPD_PROPERTY_ATTRIBUTE_FORM_REGULAR_EXPRESSION  = 3,
  WPD_PROPERTY_ATTRIBUTE_FORM_OJBECT_IDENTIFIER   = 4
} ;
```



## <a name="constants"></a><span data-ttu-id="c8b51-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="c8b51-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c8b51-107"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_UNSPECIFIED"></span><span id="wpd_property_attribute_form_unspecified"></span>**formato dell'attributo della proprietà WPD non \_ \_ \_ \_ specificato**</span><span class="sxs-lookup"><span data-stu-id="c8b51-107"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_UNSPECIFIED"></span><span id="wpd_property_attribute_form_unspecified"></span>**WPD\_PROPERTY\_ATTRIBUTE\_FORM\_UNSPECIFIED**</span></span>
</dt> <dd>

<span data-ttu-id="c8b51-108">Il formato dei dati della proprietà non è specificato.</span><span class="sxs-lookup"><span data-stu-id="c8b51-108">The form of the property's data is not specified.</span></span>

</dd> <dt>

<span data-ttu-id="c8b51-109"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_RANGE"></span><span id="wpd_property_attribute_form_range"></span>**\_ \_ \_ intervallo form attributo proprietà \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="c8b51-109"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_RANGE"></span><span id="wpd_property_attribute_form_range"></span>**WPD\_PROPERTY\_ATTRIBUTE\_FORM\_RANGE**</span></span>
</dt> <dd>

<span data-ttu-id="c8b51-110">Il valore è espresso come un intervallo di valori, con un minimo e un massimo.</span><span class="sxs-lookup"><span data-stu-id="c8b51-110">The value is expressed as a range of values, with a minimum and a maximum.</span></span>

</dd> <dt>

<span data-ttu-id="c8b51-111"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_ENUMERATION"></span><span id="wpd_property_attribute_form_enumeration"></span>**\_enumerazione del \_ form dell'attributo della proprietà WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c8b51-111"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_ENUMERATION"></span><span id="wpd_property_attribute_form_enumeration"></span>**WPD\_PROPERTY\_ATTRIBUTE\_FORM\_ENUMERATION**</span></span>
</dt> <dd>

<span data-ttu-id="c8b51-112">La proprietà dispone di una serie di singoli valori.</span><span class="sxs-lookup"><span data-stu-id="c8b51-112">The property has a series of individual values.</span></span>

</dd> <dt>

<span data-ttu-id="c8b51-113"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_REGULAR_EXPRESSION"></span><span id="wpd_property_attribute_form_regular_expression"></span>**\_ \_ \_ \_ espressione regolare dell'attributo della proprietà WPD \_**</span><span class="sxs-lookup"><span data-stu-id="c8b51-113"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_REGULAR_EXPRESSION"></span><span id="wpd_property_attribute_form_regular_expression"></span>**WPD\_PROPERTY\_ATTRIBUTE\_FORM\_REGULAR\_EXPRESSION**</span></span>
</dt> <dd>

<span data-ttu-id="c8b51-114">Il valore della proprietà è un'espressione regolare, non un'espressione letterale.</span><span class="sxs-lookup"><span data-stu-id="c8b51-114">The property value is a regular expression, not a literal expression.</span></span>

</dd> <dt>

<span data-ttu-id="c8b51-115"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_OJBECT_IDENTIFIER"></span><span id="wpd_property_attribute_form_ojbect_identifier"></span>**Identificatore della proprietà WPD del \_ \_ form dell'attributo \_ \_ oggetto \_**</span><span class="sxs-lookup"><span data-stu-id="c8b51-115"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_OJBECT_IDENTIFIER"></span><span id="wpd_property_attribute_form_ojbect_identifier"></span>**WPD\_PROPERTY\_ATTRIBUTE\_FORM\_OJBECT\_IDENTIFIER**</span></span>
</dt> <dd>

<span data-ttu-id="c8b51-116">Il valore della proprietà rappresenta un identificatore di oggetto.</span><span class="sxs-lookup"><span data-stu-id="c8b51-116">The property value represents an object identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c8b51-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="c8b51-117">Remarks</span></span>

<span data-ttu-id="c8b51-118">Questa enumerazione viene utilizzata dalla proprietà [ \_ form dell' \_ attributo \_ della proprietà WPD](attributes.md) per descrivere la modalità di archiviazione dei dati di una proprietà.</span><span class="sxs-lookup"><span data-stu-id="c8b51-118">This enumeration is used by the [WPD\_PROPERTY\_ATTRIBUTE\_FORM](attributes.md) property to describe how a property's data is stored.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8b51-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c8b51-119">Requirements</span></span>



| <span data-ttu-id="c8b51-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8b51-120">Requirement</span></span> | <span data-ttu-id="c8b51-121">Valore</span><span class="sxs-lookup"><span data-stu-id="c8b51-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8b51-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c8b51-122">Header</span></span><br/> | <dl> <span data-ttu-id="c8b51-123"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8b51-123"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8b51-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c8b51-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8b51-125">**Strutture e tipi di enumerazione**</span><span class="sxs-lookup"><span data-stu-id="c8b51-125">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




