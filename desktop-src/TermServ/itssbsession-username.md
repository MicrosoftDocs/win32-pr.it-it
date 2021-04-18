---
title: Proprietà nome utente ITsSbSession
description: Recupera il nome utente per la sessione.
ms.assetid: 0034e8cc-b67b-4e30-a059-47a269bab0fd
ms.tgt_platform: multiple
keywords:
- Proprietà UserName Servizi Desktop remoto
- Servizi Desktop remoto proprietà UserName, interfaccia ITsSbSession
- Interfaccia ITsSbSession Servizi Desktop remoto, proprietà UserName
topic_type:
- apiref
api_name:
- ITsSbSession.Username
- ITsSbSession.get_Username
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5fb66f0639d659fcb6800680ffc3b3486ad12b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302603"
---
# <a name="itssbsessionusername-property"></a>Proprietà ITsSbSession:: username

Recupera il nome utente per la sessione.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Username(
  [out, retval] BSTR *userName
);
```



## <a name="property-value"></a>Valore proprietà

Puntatore a una variabile **BSTR** che riceve il nome utente per la sessione.

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

 

 





