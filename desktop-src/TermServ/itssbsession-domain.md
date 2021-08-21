---
title: ITsSbSession Domain - proprietà
description: Recupera il nome di dominio dell'utente.
ms.assetid: bbb9a805-7270-4555-8fee-130a46bc3903
ms.tgt_platform: multiple
keywords:
- Proprietà di dominio Servizi Desktop remoto
- Proprietà di Servizi Desktop remoto, interfaccia ITsSbSession
- Interfaccia ITsSbSession Servizi Desktop remoto , proprietà Domain
topic_type:
- apiref
api_name:
- ITsSbSession.Domain
- ITsSbSession.get_Domain
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d52854f719830933c96bc130dbec4f0b15f1264344396382ad59099d4c37cf02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118128306"
---
# <a name="itssbsessiondomain-property"></a>Proprietà ITsSbSession::D omain

Recupera il nome di dominio dell'utente.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Domain(
  [out, retval] BSTR *domain
);
```



## <a name="property-value"></a>Valore proprietà

Puntatore a una **variabile BSTR** che riceve il nome di dominio dell'utente.

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

 

 





