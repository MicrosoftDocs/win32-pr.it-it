---
title: Enumerazione WMDM_ENUM_PROP_VALID_VALUES_FORM
description: Il \_ \_ \_ tipo di enumerazione del modulo WMDM enum prop valid \_ Values \_ descrive le possibili forme di valori validi per una proprietà.
ms.assetid: 49d174b4-c8a3-4c16-ad21-4b66dcf8088f
keywords:
- Enumerazione WMDM_ENUM_PROP_VALID_VALUES_FORM Windows Media Gestione dispositivi
topic_type:
- apiref
api_name:
- WMDM_ENUM_PROP_VALID_VALUES_FORM
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d7db971f359a9cead2aae6083a934086d42c481
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324587"
---
# <a name="wmdm_enum_prop_valid_values_form-enumeration"></a>\_ \_ \_ \_ \_ Enumerazione form valori validi dell'enumerazione WMDM

Il tipo di enumerazione del **\_ modulo WMDM enum \_ prop \_ valid \_ Values \_** descrive le possibili forme di valori validi per una proprietà.

## <a name="syntax"></a>Sintassi


```C++
typedef enum _WMDM_ENUM_PROP_VALID_VALUES_FORM { 
  WMDM_ENUM_PROP_VALID_VALUES_ANY,
  WMDM_ENUM_PROP_VALID_VALUES_RANGE,
  WMDM_ENUM_PROP_VALID_VALUES_ENUM
} WMDM_ENUM_PROP_VALID_VALUES_FORM;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="WMDM_ENUM_PROP_VALID_VALUES_ANY"></span><span id="wmdm_enum_prop_valid_values_any"></span>**WMDM \_ enum \_ prop \_ \_ valori validi \_ any**
</dt> <dd>

Tutti i valori sono validi.

</dd> <dt>

<span id="WMDM_ENUM_PROP_VALID_VALUES_RANGE"></span><span id="wmdm_enum_prop_valid_values_range"></span>**WMDM \_ enum \_ prop \_ \_ valori validi \_ intervallo**
</dt> <dd>

I valori validi sono espressi come un intervallo. Per informazioni dettagliate, vedere la struttura [**WMDM \_ prop \_ Values \_ Range**](wmdm-prop-values-range.md) .

</dd> <dt>

<span id="WMDM_ENUM_PROP_VALID_VALUES_ENUM"></span><span id="wmdm_enum_prop_valid_values_enum"></span>**\_enumerazione WMDM enum \_ prop \_ valid \_ Values \_**
</dt> <dd>

I valori validi sono un set enumerato. Per informazioni dettagliate, vedere la struttura di [**\_ \_ \_ enumerazione WMDM prop values**](wmdm-prop-values-enum.md) .

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa enumerazione viene usata nella struttura [**WMDM \_ prop \_ desc**](wmdm-prop-desc.md) per specificare il formato dei valori validi per una proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Tipi di enumerazione**](enumeration-types.md)
</dt> <dt>

[**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[**\_funzionalità di formato WMDM \_**](wmdm-format-capability.md)
</dt> <dt>

[**\_configurazione della prop WMDM \_**](wmdm-prop-config.md)
</dt> <dt>

[**WMDM \_ prop \_ DESC**](wmdm-prop-desc.md)
</dt> <dt>

[**\_ \_ enumerazione valori Prop \_ WMDM**](wmdm-prop-values-enum.md)
</dt> <dt>

[**WMDM \_ \_ intervallo valori \_ prop**](wmdm-prop-values-range.md)
</dt> </dl>

 

 





