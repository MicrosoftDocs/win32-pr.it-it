---
title: Struttura WMDM_PROP_DESC
description: La \_ struttura WMDM Prop \_ desc descrive i valori validi di una proprietà in una particolare configurazione della proprietà.
ms.assetid: e4766e1e-6c1b-4a2d-ad2e-c07035ca2be2
keywords:
- Struttura di WMDM_PROP_DESC Windows Media Gestione dispositivi
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
ms.openlocfilehash: 98f6ea406a3d48d0ed65098d66721fcadbb98411
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331899"
---
# <a name="wmdm_prop_desc-structure"></a>\_Struttura WMDM Prop \_ DESC

La struttura **WMDM \_ prop \_ desc** descrive i valori validi di una proprietà in una particolare configurazione della proprietà.

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

Nome della proprietà. L'applicazione deve liberare questa memoria quando viene eseguita utilizzandola.

</dd> <dt>

**ValidValuesForm**
</dt> <dd>

Valore di enumerazione del [**\_ modulo WMDM enum \_ prop \_ \_ valori \_ validi**](wmdm-enum-prop-valid-values-form.md) che descrive il tipo di valori, ad esempio un intervallo o un elenco. Il valore di questa enumerazione determina quale variabile membro viene utilizzata.

</dd> <dt>

**ValidValues**
</dt> <dd>

Include i valori validi della proprietà in una configurazione di proprietà specifica. Questo membro include uno dei tre elementi seguenti: il valore di enumerazione WMDM \_ enum \_ prop \_ valid \_ Values \_ any, il membro **ValidValuesRange** o il membro **EnumeratedValidValues**. Il valore o il membro è indicato da **ValidValuesForm**.

<dl> <dt>

**ValidValuesRange**
</dt> <dd>

Una struttura [**WMDM dell' \_ \_ \_ intervallo di valori prop**](wmdm-prop-values-range.md) contenente un intervallo di valori validi. Questa operazione è presente solo quando **ValidValuesForm** è impostato su WMDM \_ enum \_ prop \_ valid \_ Values \_ Range. Vedere la sezione Osservazioni.

</dd> <dt>

**EnumeratedValidValues**
</dt> <dd>

Una struttura di [**\_ \_ \_ enumerazione di valori prop WMDM**](wmdm-prop-values-enum.md) contenente un set enumerato di valori validi. Questa operazione è presente solo quando **ValidValuesForm** è impostato su WMDM \_ enum \_ prop \_ valid \_ Values \_ enum. Vedere la sezione Osservazioni.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

La struttura **WMDM \_ prop \_ desc** contiene una descrizione della proprietà costituita da un nome di proprietà e dai relativi valori validi in una particolare configurazione.

Il chiamante è necessario per liberare la memoria usata da **ValidValuesRange** o **EnumeratedValues**. Per un esempio di come eseguire questa operazione, vedere [**\_ \_ funzionalità di formato WMDM**](wmdm-format-capability.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[**\_ \_ \_ \_ form valori validi dell'enumerazione \_ WMDM**](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[**\_funzionalità di formato WMDM \_**](wmdm-format-capability.md)
</dt> <dt>

[**\_configurazione della prop WMDM \_**](wmdm-prop-config.md)
</dt> <dt>

[**\_ \_ enumerazione valori Prop \_ WMDM**](wmdm-prop-values-enum.md)
</dt> <dt>

[**WMDM \_ \_ intervallo valori \_ prop**](wmdm-prop-values-range.md)
</dt> <dt>

[**Strutture**](structures.md)
</dt> </dl>

 

 





