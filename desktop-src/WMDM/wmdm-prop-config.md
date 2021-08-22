---
title: WMDM_PROP_CONFIG struttura
description: La struttura WMDM PROP CONFIG descrive un set di valori di proprietà compatibili in tutte le proprietà supportate dal dispositivo \_ \_ per un particolare formato. Questa struttura contiene una serie di descrizioni di proprietà in una matrice di strutture \_ DESC PROP \_ WMDM.
ms.assetid: cf116861-e31d-4561-b262-e271888afc24
keywords:
- WMDM_PROP_CONFIG struttura windows Media Device Manager
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
ms.openlocfilehash: 6e50cd18f5b7646934a6add71674f93ebaae700ab39e57f833e555ea3688ecb6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862821"
---
# <a name="wmdm_prop_config-structure"></a>Struttura WMDM \_ PROP \_ CONFIG

La **struttura \_ WMDM PROP \_ CONFIG** descrive un set di valori di proprietà compatibili in tutte le proprietà supportate dal dispositivo per un particolare formato. Questa struttura contiene una serie di descrizioni di proprietà in una matrice di [**strutture \_ DESC PROP \_ WMDM.**](wmdm-prop-desc.md)

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

Numero di descrizioni di proprietà contenute in questa configurazione. È disponibile una singola descrizione di proprietà per ogni proprietà supportata per il formato specificato.

</dd> <dt>

**pPropDesc**
</dt> <dd>

Puntatore a una matrice di [**strutture \_ PROP \_ DESC WMDM**](wmdm-prop-desc.md) contenenti descrizioni delle proprietà. La dimensione della matrice è uguale al valore di **nPropDesc**. L'applicazione deve liberare questa memoria al termine dell'operazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

La [**struttura WMDM \_ FORMAT \_ CAPABILITY**](wmdm-format-capability.md) restituita da [**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) per un particolare formato è costituita da una serie di configurazioni di proprietà. **WMDM \_ Le \_ strutture PROP CONFIG** descrivono tali configurazioni.

Una configurazione di proprietà descrive i valori per tutte le proprietà supportate per un formato specificato. I valori di proprietà diverse in una singola configurazione sono compatibili tra loro. Ad esempio, per un file audio, una configurazione includerà valori validi di frequenza di campionamento e valori validi della velocità in bit in modo che tutte le combinazioni di queste frequenze di campionamento e bit possano essere riprodotte nel dispositivo.

Il chiamante deve liberare la memoria usata da **pPropDesc.** Per un esempio di come eseguire questa operazione, vedere [**WMDM \_ FORMAT \_ CAPABILITY**](wmdm-format-capability.md).

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

[**WMDM \_ PROP \_ DESC**](wmdm-prop-desc.md)
</dt> <dt>

[**ENUMERAZIONE DEI VALORI DELLE PROPRIETÀ WMDM \_ \_ \_**](wmdm-prop-values-enum.md)
</dt> <dt>

[**INTERVALLO DI VALORI DELLE PROPRIETÀ WMDM \_ \_ \_**](wmdm-prop-values-range.md)
</dt> <dt>

[**Strutture**](structures.md)
</dt> </dl>

 

 





