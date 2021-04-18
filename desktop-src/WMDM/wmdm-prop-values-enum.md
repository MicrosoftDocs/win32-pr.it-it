---
title: Struttura WMDM_PROP_VALUES_ENUM
description: La \_ \_ struttura enum dei valori di WMDM Prop \_ contiene un set enumerato di valori validi per una particolare proprietà in una particolare configurazione di proprietà.
ms.assetid: 8094f3c0-a7ed-4e63-8503-aaac3fd9c012
keywords:
- Struttura di WMDM_PROP_VALUES_ENUM Windows Media Gestione dispositivi
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
ms.openlocfilehash: a1c70088d57189dd36d360bc8910a15717d964ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325273"
---
# <a name="wmdm_prop_values_enum-structure"></a>\_ \_ Struttura enum dei valori di WMDM Prop \_

La **struttura \_ \_ \_ enum dei valori di WMDM prop** contiene un set enumerato di valori validi per una particolare proprietà in una particolare configurazione di proprietà.

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

Questa struttura viene utilizzata nella struttura **WMDM di \_ prop \_ desc** per descrivere un set enumerato di valori validi. Un set enumerato di valori validi è applicabile quando WMDM \_ enum \_ prop \_ valid \_ Values \_ enum è selezionato nell'enumerazione **WMDM \_ enum \_ prop \_ valid \_ Values \_ form** Enumeration.

Il chiamante è necessario per liberare la memoria utilizzata da **pvalues**. Per un esempio di come eseguire questa operazione, vedere [**\_ \_ funzionalità di formato WMDM**](wmdm-format-capability.md).

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

[**WMDM \_ \_ intervallo valori \_ prop**](wmdm-prop-values-range.md)
</dt> <dt>

[**Strutture**](structures.md)
</dt> </dl>

 

 





