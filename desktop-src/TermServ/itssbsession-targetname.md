---
title: Proprietà TargetName di ITsSbSession
description: Recupera il nome della destinazione in cui è stata creata la sessione.
ms.assetid: 5ab4cdd6-9f5f-4253-9b80-6cc35cff8b79
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà TargetName
- Servizi Desktop remoto proprietà TargetName, interfaccia ITsSbSession
- Interfaccia ITsSbSession Servizi Desktop remoto, proprietà TargetName
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
ms.openlocfilehash: dc703a32faedd250115da0b95215e620a8c15e19
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302604"
---
# <a name="itssbsessiontargetname-property"></a>Proprietà ITsSbSession:: TargetName

Recupera il nome della destinazione in cui è stata creata la sessione.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_TargetName(
  [out, retval] BSTR *targetName
);
```



## <a name="property-value"></a>Valore proprietà

Puntatore a una variabile **BSTR** che riceve il nome della destinazione in cui è stata creata la sessione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                            |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                       |
| IDL<br/>                      | <dl> <dt>Sbtsv. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITsSbSession**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> </dl>

 

 





