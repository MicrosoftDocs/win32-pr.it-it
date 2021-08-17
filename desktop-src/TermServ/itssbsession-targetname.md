---
title: Proprietà ITsSbSession TargetName
description: Recupera il nome della destinazione in cui è stata creata la sessione.
ms.assetid: 5ab4cdd6-9f5f-4253-9b80-6cc35cff8b79
ms.tgt_platform: multiple
keywords:
- Proprietà TargetName Servizi Desktop remoto
- Proprietà TargetName Servizi Desktop remoto,interfaccia ITsSbSession
- Interfaccia ITsSbSession Servizi Desktop remoto proprietà , TargetName
topic_type:
- apiref
api_name:
- ITsSbSession.TargetName
- ITsSbSession.get_TargetName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfbc1e26aa4bf55a59b6405921d49e6b1aafa14e63a1e487caca9a7c036b1524
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138314"
---
# <a name="itssbsessiontargetname-property"></a>Proprietà ITsSbSession::TargetName

Recupera il nome della destinazione in cui è stata creata la sessione.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_TargetName(
  [out, retval] BSTR *targetName
);
```



## <a name="property-value"></a>Valore proprietà

Puntatore a una **variabile BSTR** che riceve il nome della destinazione in cui è stata creata la sessione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                            |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                       |
| Idl<br/>                      | <dl> <dt>Sbtsv.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITsSbSession**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> </dl>

 

 





