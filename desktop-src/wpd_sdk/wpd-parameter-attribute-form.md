---
description: Descrive il modo in cui un parametro (metodo o evento) archivia il relativo valore.
ms.assetid: 066196af-7805-4823-8ab7-cb95c17bba2a
title: Enumerazione WpdParameterAttributeForm (PortableDevice.h)
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
ms.openlocfilehash: f50665768d62d8155bd0ac9001f4ae5029766d7d5b27a942941f8f41b9492e10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026749"
---
# <a name="wpdparameterattributeform-enumeration"></a>Enumerazione WpdParameterAttributeForm

Il [**tipo di enumerazione WpdParameterAttributeForm**](/previous-versions/windows/hardware/drivers/ff597895(v=vs.85)) descrive il modo in cui un parametro (metodo o evento) archivia il relativo valore.

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

<span id="WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED"></span><span id="wpd_parameter_attribute_form_unspecified"></span>**FORMATO DELL'ATTRIBUTO DEL PARAMETRO WPD \_ \_ NON \_ \_ SPECIFICATO**
</dt> <dd>

Il formato del parametro non è specificato.

</dd> <dt>

<span id="WPD_PARAMETER_ATTRIBUTE_FORM_RANGE"></span><span id="wpd_parameter_attribute_form_range"></span>**INTERVALLO DI MODULI \_ DEGLI \_ ATTRIBUTI DEI PARAMETRI \_ WPD \_**
</dt> <dd>

Il parametro specifica un intervallo.

</dd> <dt>

<span id="WPD_PARAMETER_ATTRIBUTE_FORM_ENUMERATION"></span><span id="wpd_parameter_attribute_form_enumeration"></span>**ENUMERAZIONE DEL MODULO DEGLI \_ ATTRIBUTI \_ DEI PARAMETRI \_ \_ WPD**
</dt> <dd>

Il parametro è un'enumerazione .

</dd> <dt>

<span id="WPD_PARAMETER_ATTRIBUTE_FORM_REGULAR_EXPRESSION"></span><span id="wpd_parameter_attribute_form_regular_expression"></span>**ESPRESSIONE REGOLARE DEL FORMATO \_ \_ DELL'ATTRIBUTO DEL PARAMETRO \_ \_ \_ WPD**
</dt> <dd>

Il parametro è un'espressione regolare.

</dd> <dt>

<span id="WPD_PARAMETER_ATTRIBUTE_OBJECT_IDENTIFIER"></span><span id="wpd_parameter_attribute_object_identifier"></span>**IDENTIFICATORE DI OGGETTO \_ \_ DELL'ATTRIBUTO \_ DEL PARAMETRO \_ WPD**
</dt> <dd>

Il parametro è un identificatore di oggetto.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



 

