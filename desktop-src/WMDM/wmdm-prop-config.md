---
title: Struttura WMDM_PROP_CONFIG
description: La \_ \_ struttura di configurazione di WMDM prop descrive un set di valori di proprietà compatibili tra tutte le proprietà supportate dal dispositivo per un particolare formato. Questa struttura contiene un numero di descrizioni delle proprietà in una matrice di \_ strutture WMDM Prop \_ desc.
ms.assetid: cf116861-e31d-4561-b262-e271888afc24
keywords:
- Struttura di WMDM_PROP_CONFIG Windows Media Gestione dispositivi
topic_type:
- apiref
api_name:
- WMDM_PROP_CONFIG
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b19314b2f012d25fa2d97b44b9dc7524f9e3355
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324225"
---
# <a name="wmdm_prop_config-structure"></a>Struttura di configurazione di WMDM \_ prop \_

La struttura di **\_ \_ configurazione di WMDM prop** descrive un set di valori di proprietà compatibili tra tutte le proprietà supportate dal dispositivo per un particolare formato. Questa struttura contiene un numero di descrizioni delle proprietà in una matrice di strutture [**WMDM \_ prop \_ desc**](wmdm-prop-desc.md) .

## <a name="syntax"></a>Sintassi


```C++
typedef struct _WMDM_PROP_CONFIG {
  UINT           nPreference;
  UINT           nPropDesc;
  WMDM_PROP_DESC *pPropDesc;
} WMDM_PROP_CONFIG;
```



## <a name="members"></a>Members

<dl> <dt>

**nPreference**
</dt> <dd>

Livello di preferenza del dispositivo per questa configurazione. Il valore più basso indica la configurazione più preferita.

</dd> <dt>

**nPropDesc**
</dt> <dd>

Numero di descrizioni delle proprietà contenute in questa configurazione. È disponibile una singola descrizione della proprietà per ogni proprietà supportata per il formato specificato.

</dd> <dt>

**pPropDesc**
</dt> <dd>

Puntatore a una matrice di strutture [**WMDM \_ prop \_ desc**](wmdm-prop-desc.md) contenenti descrizioni di proprietà. La dimensione della matrice è uguale al valore di **nPropDesc**. Al termine di questa operazione, l'applicazione deve liberare la memoria.

</dd> </dl>

## <a name="remarks"></a>Commenti

La struttura di [**\_ \_ funzionalità del formato WMDM**](wmdm-format-capability.md) restituita da [**IWMDMDevice3:: GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) per un particolare formato è costituita da una serie di configurazioni di proprietà. **WMDM \_ Le strutture di \_ configurazione prop** descrivono tali configurazioni.

Una configurazione di proprietà descrive i valori per tutte le proprietà supportate per un determinato formato. I valori di proprietà diverse in una singola configurazione sono compatibili tra loro. Ad esempio, per un file audio, una configurazione includerà i valori validi della frequenza di campionamento e i valori validi della velocità in bit in modo che tutte le combinazioni di queste frequenze di campionamento e di bit possano essere riprodotte nel dispositivo.

Il chiamante è necessario per liberare la memoria utilizzata da **pPropDesc**. Per un esempio di come eseguire questa operazione, vedere [**\_ \_ funzionalità di formato WMDM**](wmdm-format-capability.md).

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

[**WMDM \_ prop \_ DESC**](wmdm-prop-desc.md)
</dt> <dt>

[**\_ \_ enumerazione valori Prop \_ WMDM**](wmdm-prop-values-enum.md)
</dt> <dt>

[**WMDM \_ \_ intervallo valori \_ prop**](wmdm-prop-values-range.md)
</dt> <dt>

[**Strutture**](structures.md)
</dt> </dl>

 

 





