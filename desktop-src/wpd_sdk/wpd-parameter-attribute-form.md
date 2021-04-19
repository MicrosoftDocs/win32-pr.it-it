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
# <a name="wpdparameterattributeform-enumeration"></a>Enumerazione WpdParameterAttributeForm

Il tipo di enumerazione [**WpdParameterAttributeForm**](/previous-versions/windows/hardware/drivers/ff597895(v=vs.85)) descrive il modo in cui un parametro (metodo o evento) archivia il valore.

## <a name="syntax"></a>Sintassi


```C++
typedef enum tagWpdParameterAttributeForm { 
  WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED         = 0,
  WPD_PARAMETER_ATTRIBUTE_FORM_RANGE               = 1,
  WPD_PARAMETER_ATTRIBUTE_FORM_ENUMERATION         = 2,
  WPD_PARAMETER_ATTRIBUTE_FORM_REGULAR_EXPRESSION  = 3,
  WPD_PARAMETER_ATTRIBUTE_OBJECT_IDENTIFIER        = 4
} WpdParameterAttributeForm;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED"></span><span id="wpd_parameter_attribute_form_unspecified"></span>**il form dell'attributo del parametro WPD non è \_ \_ \_ \_ specificato**
</dt> <dd>

Il formato del parametro non è specificato.

</dd> <dt>

<span id="WPD_PARAMETER_ATTRIBUTE_FORM_RANGE"></span><span id="wpd_parameter_attribute_form_range"></span>**\_ \_ \_ intervallo form attributo parametro \_ WPD**
</dt> <dd>

Il parametro specifica un intervallo.

</dd> <dt>

<span id="WPD_PARAMETER_ATTRIBUTE_FORM_ENUMERATION"></span><span id="wpd_parameter_attribute_form_enumeration"></span>**\_ \_ \_ enumerazione form attributo parametro \_ WPD**
</dt> <dd>

Il parametro è un'enumerazione.

</dd> <dt>

<span id="WPD_PARAMETER_ATTRIBUTE_FORM_REGULAR_EXPRESSION"></span><span id="wpd_parameter_attribute_form_regular_expression"></span>**\_ \_ \_ \_ espressione regolare dell'attributo del parametro WPD \_**
</dt> <dd>

Il parametro è un'espressione regolare.

</dd> <dt>

<span id="WPD_PARAMETER_ATTRIBUTE_OBJECT_IDENTIFIER"></span><span id="wpd_parameter_attribute_object_identifier"></span>**\_ \_ \_ identificatore oggetto attributo parametro \_ WPD**
</dt> <dd>

Il parametro è un identificatore di oggetto.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



 

