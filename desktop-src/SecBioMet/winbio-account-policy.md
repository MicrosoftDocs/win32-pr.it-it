---
title: WINBIO_ACCOUNT_POLICY (Adapter.h \_ Winbio)
description: Contiene un criterio antispoofing predefinito o specifico dell'account.
ms.assetid: 7098FC53-E487-42B2-8B4B-EB7E2D296CB6
keywords:
- WINBIO_ACCOUNT_POLICY struttura Windows'API Biometric Framework
- PWINBIO_ACCOUNT_POLICY puntatore alla struttura Windows'API Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_ACCOUNT_POLICY
api_location:
- Winbio_adapter.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c30241f0e13528c8427367c61362b803caaa9fc8c0a15a0eefad72689517d40f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035251"
---
# <a name="winbio_account_policy-structure"></a>Struttura DEI CRITERI ACCOUNT WINBIO \_ \_

La **struttura CRITERI \_ ACCOUNT \_ WINBIO** contiene criteri antispoofing predefiniti o specifici dell'account.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _WINBIO_ACCOUNT_POLICY {
  WINBIO_IDENTITY                 Identity;
  WINBIO_ANTI_SPOOF_POLICY_ACTION AntiSpoofBehavior;
} WINBIO_ACCOUNT_POLICY, *PWINBIO_ACCOUNT_POLICY;
```



## <a name="members"></a>Members

<dl> <dt>

**Identità**
</dt> <dd>

Struttura [**WINBIO \_ IDENTITY**](winbio-identity.md) che specifica le informazioni sull'account.

</dd> <dt>

**AntiSpoofBehavior**
</dt> <dd>

Uno dei valori di enumerazione DI [**WINBIO \_ ANTI SPOOF POLICY \_ \_ \_ ACTION**](winbio-anti-spoof-policy-action.md) che specifica quale azione dei criteri antispoofing usare per l'account.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per una descrizione dell'uso di questa struttura, vedere la discussione sul metodo [**EngineAdapterSetAccountPolicy.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_account_policy_fn)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                                              |
| Server minimo supportato<br/> | \[Windows Server 2016 solo app desktop\]<br/>                                                                     |
| Intestazione<br/>                   | <dl> <dt>Adapter.h Winbio \_ (include \_ Adapter.h Winbio)</dt> </dl> |



 

 





