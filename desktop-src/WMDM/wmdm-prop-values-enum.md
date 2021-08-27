---
title: WMDM_PROP_VALUES_ENUM struttura
description: La struttura ENUM WMDM PROP VALUES contiene un set enumerato di valori \_ validi per una determinata proprietà in una particolare configurazione di \_ \_ proprietà.
ms.assetid: 8094f3c0-a7ed-4e63-8503-aaac3fd9c012
keywords:
- WMDM_PROP_VALUES_ENUM struttura windows Media Device Manager
topic_type:
- apiref
api_name:
- WMDM_PROP_VALUES_ENUM
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35766ed71b864c5eb7f0bbbebf5eda384a25e174501aa2a56e790840a4c636c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004791"
---
# <a name="wmdm_prop_values_enum-structure"></a>Struttura \_ ENUM WMDM PROP \_ VALUES \_

La **struttura \_ \_ \_ ENUM WMDM PROP VALUES** contiene un set enumerato di valori validi per una determinata proprietà in una particolare configurazione di proprietà.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _WMDM_PROP_VALUES_ENUM {
  UINT        cEnumValues;
  PROPVARIANT *pValues;
} WMDM_PROP_VALUES_ENUM;
```



## <a name="members"></a>Members

<dl> <dt>

**cEnumValues**
</dt> <dd>

Conteggio dei valori enumerati.

</dd> <dt>

**pValues**
</dt> <dd>

Puntatore a una matrice di valori. La dimensione della matrice è uguale al valore di **cEnumValues**.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene usata nella struttura **\_ WMDM PROP \_ DESC** per descrivere un set enumerato di valori validi. Un set enumerato di valori validi è applicabile quando WMDM ENUM PROP VALID VALUES ENUM viene selezionato dall'enumerazione \_ \_ \_ \_ \_ **WMDM \_ ENUM \_ PROP VALID VALUES \_ \_ \_ FORM.**

Il chiamante deve liberare la memoria usata da **pValues.** Per un esempio di come eseguire questa operazione, vedere [**WMDM \_ FORMAT \_ CAPABILITY**](wmdm-format-capability.md).

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

[**WMDM \_ PROP \_ DESC**](wmdm-prop-desc.md)
</dt> <dt>

[**INTERVALLO DI VALORI DELLA PROPRIETÀ WMDM \_ \_ \_**](wmdm-prop-values-range.md)
</dt> <dt>

[**Strutture**](structures.md)
</dt> </dl>

 

 





