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
# <a name="wpdattributeform-enumeration"></a>Enumerazione WpdAttributeForm

Il tipo di enumerazione **WpdAttributeForm** descrive il modo in cui una proprietà archivia i valori.

## <a name="syntax"></a>Sintassi


```C++
typedef enum WpdAttributeForm { 
  WPD_PROPERTY_ATTRIBUTE_FORM_UNSPECIFIED         = 0,
  WPD_PROPERTY_ATTRIBUTE_FORM_RANGE               = 1,
  WPD_PROPERTY_ATTRIBUTE_FORM_ENUMERATION         = 2,
  WPD_PROPERTY_ATTRIBUTE_FORM_REGULAR_EXPRESSION  = 3,
  WPD_PROPERTY_ATTRIBUTE_FORM_OJBECT_IDENTIFIER   = 4
} ;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_UNSPECIFIED"></span><span id="wpd_property_attribute_form_unspecified"></span>**formato dell'attributo della proprietà WPD non \_ \_ \_ \_ specificato**
</dt> <dd>

Il formato dei dati della proprietà non è specificato.

</dd> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_RANGE"></span><span id="wpd_property_attribute_form_range"></span>**\_ \_ \_ intervallo form attributo proprietà \_ WPD**
</dt> <dd>

Il valore è espresso come un intervallo di valori, con un minimo e un massimo.

</dd> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_ENUMERATION"></span><span id="wpd_property_attribute_form_enumeration"></span>**\_enumerazione del \_ form dell'attributo della proprietà WPD \_ \_**
</dt> <dd>

La proprietà dispone di una serie di singoli valori.

</dd> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_REGULAR_EXPRESSION"></span><span id="wpd_property_attribute_form_regular_expression"></span>**\_ \_ \_ \_ espressione regolare dell'attributo della proprietà WPD \_**
</dt> <dd>

Il valore della proprietà è un'espressione regolare, non un'espressione letterale.

</dd> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_OJBECT_IDENTIFIER"></span><span id="wpd_property_attribute_form_ojbect_identifier"></span>**Identificatore della proprietà WPD del \_ \_ form dell'attributo \_ \_ oggetto \_**
</dt> <dd>

Il valore della proprietà rappresenta un identificatore di oggetto.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa enumerazione viene utilizzata dalla proprietà [ \_ form dell' \_ attributo \_ della proprietà WPD](attributes.md) per descrivere la modalità di archiviazione dei dati di una proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture e tipi di enumerazione**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




