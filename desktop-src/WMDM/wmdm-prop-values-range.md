---
title: WMDM_PROP_VALUES_RANGE struttura
description: La struttura WMDM PROP VALUES RANGE descrive un intervallo di valori \_ validi per una determinata proprietà in una particolare configurazione di \_ \_ proprietà.
ms.assetid: fb823a66-cc9c-4632-a4f0-03c7255c3ccb
keywords:
- WMDM_PROP_VALUES_RANGE struttura windows Media Device Manager
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
ms.openlocfilehash: a668b5acd8427df5b4bc163788c225f4eaee9a16b70af25312ae8ec94cb2bb63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004781"
---
# <a name="wmdm_prop_values_range-structure"></a>Struttura WMDM \_ PROP \_ VALUES \_ RANGE

La **struttura WMDM \_ PROP VALUES \_ \_ RANGE** descrive un intervallo di valori validi per una determinata proprietà in una particolare configurazione di proprietà.

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

Dimensione del passaggio in cui i valori validi aumentano dal valore minimo al valore massimo. Ciò consente di specificare valori discreti consentiti in un intervallo.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene usata nella struttura [**WMDM \_ PROP \_ DESC**](wmdm-prop-desc.md) per descrivere un intervallo di valori validi. Un intervallo di valori validi è applicabile quando l'enumerazione WMDM ENUM PROP VALID VALUES ENUM è selezionata dall'enumerazione \_ \_ \_ \_ \_ [**WMDM \_ ENUM \_ PROP VALID VALUES \_ \_ \_ FORM.**](wmdm-enum-prop-valid-values-form.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[**MODULO VALORI \_ VALIDI DELLE PROPRIETÀ DELL'ENUMERAZIONE WMDM \_ \_ \_ \_**](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[**FUNZIONALITÀ DEL \_ FORMATO WMDM \_**](wmdm-format-capability.md)
</dt> <dt>

[**WMDM \_ PROP \_ CONFIG**](wmdm-prop-config.md)
</dt> <dt>

[**WMDM \_ PROP \_ DESC**](wmdm-prop-desc.md)
</dt> <dt>

[**ENUMERAZIONE DEI VALORI DELLA PROPRIETÀ WMDM \_ \_ \_**](wmdm-prop-values-enum.md)
</dt> <dt>

[**Strutture**](structures.md)
</dt> </dl>

 

 





