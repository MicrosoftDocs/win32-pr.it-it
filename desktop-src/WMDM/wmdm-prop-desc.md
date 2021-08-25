---
title: WMDM_PROP_DESC struttura
description: La struttura WMDM \_ PROP \_ DESC descrive i valori validi di una proprietà in una particolare configurazione di proprietà.
ms.assetid: e4766e1e-6c1b-4a2d-ad2e-c07035ca2be2
keywords:
- WMDM_PROP_DESC struttura di Windows Media Device Manager
topic_type:
- apiref
api_name:
- WMDM_PROP_DESC
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cad250745d51f00d3bb0492b6da8d3f9802bf87b78d65f4640324a68caa9ddf3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903941"
---
# <a name="wmdm_prop_desc-structure"></a>Struttura WMDM \_ PROP \_ DESC

La **struttura WMDM \_ PROP \_ DESC** descrive i valori validi di una proprietà in una particolare configurazione di proprietà.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _WMDM_PROP_DESC {
  LPWSTR                           pwszPropName;
  WMDM_ENUM_PROP_VALID_VALUES_FORM ValidValuesForm;
  union  {
    WMDM_PROP_VALUES_RANGE ValidValuesRange;
    WMDM_PROP_VALUES_ENUM  EnumeratedValidValues;
  } ValidValues;
} WMDM_PROP_DESC;
```



## <a name="members"></a>Members

<dl> <dt>

**pwszPropName**
</dt> <dd>

Nome della proprietà. L'applicazione deve liberare questa memoria al termine dell'uso.

</dd> <dt>

**ValidValuesForm**
</dt> <dd>

Valore [**di enumerazione WMDM \_ ENUM PROP VALID VALUES \_ \_ \_ \_ FORM**](wmdm-enum-prop-valid-values-form.md) che descrive il tipo di valori, ad esempio un intervallo o un elenco. Il valore di questa enumerazione determina quale variabile membro viene utilizzata.

</dd> <dt>

**Validvalues**
</dt> <dd>

Contiene i valori validi della proprietà in una particolare configurazione di proprietà. Questo membro contiene uno dei tre elementi seguenti: il valore di enumerazione WMDM ENUM PROP VALID VALUES ANY, il membro \_ \_ \_ \_ \_ **ValidValuesRange** o il membro **EnumeratedValidValues**. Il valore o il membro è indicato da **ValidValuesForm.**

<dl> <dt>

**ValidValuesRange**
</dt> <dd>

Struttura [**WMDM \_ PROP VALUES \_ \_ RANGE**](wmdm-prop-values-range.md) contenente un intervallo di valori validi. È presente solo quando **ValidValuesForm** è impostato su WMDM \_ ENUM \_ PROP VALID \_ VALUES \_ \_ RANGE. Vedere la sezione Osservazioni.

</dd> <dt>

**EnumeratedValidValues**
</dt> <dd>

Struttura [**WMDM \_ PROP VALUES \_ \_ ENUM**](wmdm-prop-values-enum.md) contenente un set enumerato di valori validi. È presente solo quando **ValidValuesForm** è impostato su WMDM \_ ENUM \_ PROP VALID \_ VALUES \_ \_ ENUM. Vedere la sezione Osservazioni.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

La **struttura WMDM \_ PROP \_ DESC** contiene una descrizione della proprietà costituita da un nome di proprietà e dai relativi valori validi in una particolare configurazione.

Il chiamante deve liberare la memoria usata da **ValidValuesRange** o **EnumeratedValues.** Per un esempio di come eseguire questa operazione, vedere [**WMDM \_ FORMAT \_ CAPABILITY**](wmdm-format-capability.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[**MODULO DEI VALORI \_ VALIDI DELLE PROPRIETÀ DI \_ ENUMERAZIONE \_ \_ WMDM \_**](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[**FUNZIONALITÀ DEL FORMATO \_ \_ WMDM**](wmdm-format-capability.md)
</dt> <dt>

[**WMDM \_ PROP \_ CONFIG**](wmdm-prop-config.md)
</dt> <dt>

[**ENUMERAZIONE DEI VALORI DELLE PROPRIETÀ WMDM \_ \_ \_**](wmdm-prop-values-enum.md)
</dt> <dt>

[**INTERVALLO DI VALORI DELLE PROPRIETÀ WMDM \_ \_ \_**](wmdm-prop-values-range.md)
</dt> <dt>

[**Strutture**](structures.md)
</dt> </dl>

 

 





