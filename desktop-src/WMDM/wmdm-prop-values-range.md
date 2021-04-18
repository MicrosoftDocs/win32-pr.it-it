---
title: Struttura WMDM_PROP_VALUES_RANGE
description: La \_ struttura dell'intervallo WMDM Prop \_ Values \_ descrive un intervallo di valori validi per una particolare proprietà in una particolare configurazione della proprietà.
ms.assetid: fb823a66-cc9c-4632-a4f0-03c7255c3ccb
keywords:
- Struttura di WMDM_PROP_VALUES_RANGE Windows Media Gestione dispositivi
topic_type:
- apiref
api_name:
- WMDM_PROP_VALUES_RANGE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ba82a1067db97e93fff2845e69e89f978548b73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325272"
---
# <a name="wmdm_prop_values_range-structure"></a>\_Struttura dell' \_ intervallo di valori della prop WMDM \_

La struttura dell' **\_ \_ \_ intervallo WMDM prop values** descrive un intervallo di valori validi per una particolare proprietà in una particolare configurazione della proprietà.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _WMDM_PROP_VALUES_RANGE {
  PROPVARIANT rangeMin;
  PROPVARIANT rangeMax;
  PROPVARIANT rangeStep;
} WMDM_PROP_VALUES_RANGE;
```



## <a name="members"></a>Members

<dl> <dt>

**rangeMin**
</dt> <dd>

Valore minimo nell'intervallo.

</dd> <dt>

**rangeMax**
</dt> <dd>

Valore massimo nell'intervallo.

</dd> <dt>

**rangeStep**
</dt> <dd>

Dimensioni del passaggio in cui i valori validi vengono incrementati dal valore minimo al valore massimo. Questo consente di specificare valori discreti consentiti in un intervallo.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene utilizzata nella struttura [**WMDM di \_ prop \_ desc**](wmdm-prop-desc.md) per descrivere un intervallo di valori validi. Un intervallo di valori validi è applicabile quando WMDM \_ enum \_ prop \_ valid \_ Values \_ enum è selezionato dall'enumerazione [**WMDM \_ enum \_ prop \_ valid \_ Values \_ form**](wmdm-enum-prop-valid-values-form.md) Enumeration.

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

[**WMDM \_ prop \_ DESC**](wmdm-prop-desc.md)
</dt> <dt>

[**\_ \_ enumerazione valori Prop \_ WMDM**](wmdm-prop-values-enum.md)
</dt> <dt>

[**Strutture**](structures.md)
</dt> </dl>

 

 





