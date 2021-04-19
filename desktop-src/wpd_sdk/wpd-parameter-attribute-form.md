---
description: Descrive il modo in cui un parametro (metodo o evento) archivia il valore.
ms.assetid: 066196af-7805-4823-8ab7-cb95c17bba2a
title: Enumerazione WpdParameterAttributeForm (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WpdParameterAttributeForm
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 528008edbb74d5eda626b9868814ad621e676fa9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325807"
---
# <a name="wpdparameterattributeform-enumeration"></a><span data-ttu-id="93d39-103">Enumerazione WpdParameterAttributeForm</span><span class="sxs-lookup"><span data-stu-id="93d39-103">WpdParameterAttributeForm enumeration</span></span>

<span data-ttu-id="93d39-104">Il tipo di enumerazione [**WpdParameterAttributeForm**](/previous-versions/windows/hardware/drivers/ff597895(v=vs.85)) descrive il modo in cui un parametro (metodo o evento) archivia il valore.</span><span class="sxs-lookup"><span data-stu-id="93d39-104">The [**WpdParameterAttributeForm**](/previous-versions/windows/hardware/drivers/ff597895(v=vs.85)) enumeration type describes how a (method or event) parameter stores its value.</span></span>

## <a name="syntax"></a><span data-ttu-id="93d39-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="93d39-105">Syntax</span></span>


```C++
typedef enum tagWpdParameterAttributeForm { 
  WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED         = 0,
  WPD_PARAMETER_ATTRIBUTE_FORM_RANGE               = 1,
  WPD_PARAMETER_ATTRIBUTE_FORM_ENUMERATION         = 2,
  WPD_PARAMETER_ATTRIBUTE_FORM_REGULAR_EXPRESSION  = 3,
  WPD_PARAMETER_ATTRIBUTE_OBJECT_IDENTIFIER        = 4
} WpdParameterAttributeForm;
```



## <a name="constants"></a><span data-ttu-id="93d39-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="93d39-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="93d39-107"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED"></span><span id="wpd_parameter_attribute_form_unspecified"></span>**il form dell'attributo del parametro WPD non è \_ \_ \_ \_ specificato**</span><span class="sxs-lookup"><span data-stu-id="93d39-107"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED"></span><span id="wpd_parameter_attribute_form_unspecified"></span>**WPD\_PARAMETER\_ATTRIBUTE\_FORM\_UNSPECIFIED**</span></span>
</dt> <dd>

<span data-ttu-id="93d39-108">Il formato del parametro non è specificato.</span><span class="sxs-lookup"><span data-stu-id="93d39-108">The form of the parameter is not specified.</span></span>

</dd> <dt>

<span data-ttu-id="93d39-109"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_RANGE"></span><span id="wpd_parameter_attribute_form_range"></span>**\_ \_ \_ intervallo form attributo parametro \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="93d39-109"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_RANGE"></span><span id="wpd_parameter_attribute_form_range"></span>**WPD\_PARAMETER\_ATTRIBUTE\_FORM\_RANGE**</span></span>
</dt> <dd>

<span data-ttu-id="93d39-110">Il parametro specifica un intervallo.</span><span class="sxs-lookup"><span data-stu-id="93d39-110">The parameter specifies a range.</span></span>

</dd> <dt>

<span data-ttu-id="93d39-111"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_ENUMERATION"></span><span id="wpd_parameter_attribute_form_enumeration"></span>**\_ \_ \_ enumerazione form attributo parametro \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="93d39-111"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_ENUMERATION"></span><span id="wpd_parameter_attribute_form_enumeration"></span>**WPD\_PARAMETER\_ATTRIBUTE\_FORM\_ENUMERATION**</span></span>
</dt> <dd>

<span data-ttu-id="93d39-112">Il parametro è un'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="93d39-112">The parameter is an enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="93d39-113"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_REGULAR_EXPRESSION"></span><span id="wpd_parameter_attribute_form_regular_expression"></span>**\_ \_ \_ \_ espressione regolare dell'attributo del parametro WPD \_**</span><span class="sxs-lookup"><span data-stu-id="93d39-113"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_REGULAR_EXPRESSION"></span><span id="wpd_parameter_attribute_form_regular_expression"></span>**WPD\_PARAMETER\_ATTRIBUTE\_FORM\_REGULAR\_EXPRESSION**</span></span>
</dt> <dd>

<span data-ttu-id="93d39-114">Il parametro è un'espressione regolare.</span><span class="sxs-lookup"><span data-stu-id="93d39-114">The parameter is a regular expression.</span></span>

</dd> <dt>

<span data-ttu-id="93d39-115"><span id="WPD_PARAMETER_ATTRIBUTE_OBJECT_IDENTIFIER"></span><span id="wpd_parameter_attribute_object_identifier"></span>**\_ \_ \_ identificatore oggetto attributo parametro \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="93d39-115"><span id="WPD_PARAMETER_ATTRIBUTE_OBJECT_IDENTIFIER"></span><span id="wpd_parameter_attribute_object_identifier"></span>**WPD\_PARAMETER\_ATTRIBUTE\_OBJECT\_IDENTIFIER**</span></span>
</dt> <dd>

<span data-ttu-id="93d39-116">Il parametro è un identificatore di oggetto.</span><span class="sxs-lookup"><span data-stu-id="93d39-116">The parameter is an object identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="93d39-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="93d39-117">Requirements</span></span>



| <span data-ttu-id="93d39-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="93d39-118">Requirement</span></span> | <span data-ttu-id="93d39-119">Valore</span><span class="sxs-lookup"><span data-stu-id="93d39-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="93d39-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="93d39-120">Header</span></span><br/> | <dl> <span data-ttu-id="93d39-121"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="93d39-121"><dt>PortableDevice.h</dt></span></span> </dl> |



 

