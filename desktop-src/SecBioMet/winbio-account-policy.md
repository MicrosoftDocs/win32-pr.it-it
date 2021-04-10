---
title: Struttura WINBIO_ACCOUNT_POLICY (WinBio \_ Adapter. h)
description: Contiene criteri di antispoofing predefiniti o specifici dell'account.
ms.assetid: 7098FC53-E487-42B2-8B4B-EB7E2D296CB6
keywords:
- Struttura di WINBIO_ACCOUNT_POLICY Windows Biometric Framework API
- API Windows Biometric Framework puntatore alla struttura PWINBIO_ACCOUNT_POLICY
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
ms.openlocfilehash: c734fa6d98615b7708a65ebad1dddc47cdc77cc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964215"
---
# <a name="winbio_account_policy-structure"></a>Struttura dei criteri dell' \_ account WINBIO \_

La struttura dei **\_ \_ criteri dell'account WINBIO** contiene un criterio di antispoofing predefinito o specifico per l'account.

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

Struttura [**di \_ identità WINBIO**](winbio-identity.md) che specifica le informazioni sull'account.

</dd> <dt>

**AntiSpoofBehavior**
</dt> <dd>

Uno dei valori di enumerazione dell' [**\_ \_ azione del \_ criterio \_ anti spoofing di WINBIO**](winbio-anti-spoof-policy-action.md) che specifica l'azione del criterio di antispoofing da usare per l'account.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per una descrizione della modalità di utilizzo di questa struttura, vedere la discussione sul metodo [**EngineAdapterSetAccountPolicy**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_account_policy_fn) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2016\]<br/>                                                                     |
| Intestazione<br/>                   | <dl> <dt>WinBio \_ Adapter. h (include WinBio \_ Adapter. h)</dt> </dl> |



 

 





