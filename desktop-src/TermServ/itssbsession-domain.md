---
title: Proprietà di dominio ITsSbSession
description: Recupera il nome di dominio dell'utente.
ms.assetid: bbb9a805-7270-4555-8fee-130a46bc3903
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto della proprietà di dominio
- Servizi Desktop remoto di proprietà del dominio, interfaccia ITsSbSession
- Interfaccia ITsSbSession Servizi Desktop remoto, proprietà del dominio
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
ms.openlocfilehash: 4501413888d17a70610160117df3ad03fde73b76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302606"
---
# <a name="itssbsessiondomain-property"></a>ITsSbSession::D Proprietà ominio

Recupera il nome di dominio dell'utente.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Domain(
  [out, retval] BSTR *domain
);
```



## <a name="property-value"></a>Valore proprietà

Puntatore a una variabile **BSTR** che riceve il nome di dominio dell'utente.

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

 

 





