---
description: Il tipo di enumerazione WpdAttributeForm descrive il modo in cui una proprietà archivia i relativi valori.
ms.assetid: 3ad8d1f9-1b74-4f34-9af5-1acdd588b650
title: Enumerazione WpdAttributeForm (PortableDevice.h)
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
ms.openlocfilehash: 8366f90fe41eaa92d826f4d761fe8cdf58304f54e1f57cb074ae94d6fd9f1ea9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118696279"
---
# <a name="wpdattributeform-enumeration"></a>Enumerazione WpdAttributeForm

Il **tipo di enumerazione WpdAttributeForm** descrive il modo in cui una proprietà archivia i relativi valori.

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

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_UNSPECIFIED"></span><span id="wpd_property_attribute_form_unspecified"></span>**FORMATO ATTRIBUTO \_ PROPRIETÀ WPD NON \_ \_ \_ SPECIFICATO**
</dt> <dd>

Il formato dei dati della proprietà non è specificato.

</dd> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_RANGE"></span><span id="wpd_property_attribute_form_range"></span>**INTERVALLO DI FORM ATTRIBUTO PROPRIETÀ WPD \_ \_ \_ \_**
</dt> <dd>

Il valore è espresso come intervallo di valori, con un valore minimo e un massimo.

</dd> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_ENUMERATION"></span><span id="wpd_property_attribute_form_enumeration"></span>**ENUMERAZIONE FORM ATTRIBUTO PROPRIETÀ WPD \_ \_ \_ \_**
</dt> <dd>

La proprietà ha una serie di valori singoli.

</dd> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_REGULAR_EXPRESSION"></span><span id="wpd_property_attribute_form_regular_expression"></span>**ESPRESSIONE REGOLARE \_ DELL'ATTRIBUTO \_ DI \_ PROPRIETÀ \_ \_ WPD**
</dt> <dd>

Il valore della proprietà è un'espressione regolare, non un'espressione letterale.

</dd> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_OJBECT_IDENTIFIER"></span><span id="wpd_property_attribute_form_ojbect_identifier"></span>**IDENTIFICATORE \_ \_ \_ \_ OJBECT DELL'ATTRIBUTO DI PROPRIETÀ WPD \_**
</dt> <dd>

Il valore della proprietà rappresenta un identificatore di oggetto.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa enumerazione viene usata dalla proprietà [ \_ WPD PROPERTY ATTRIBUTE \_ \_ FORM](attributes.md) per descrivere come vengono archiviati i dati di una proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture e tipi di enumerazione**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




