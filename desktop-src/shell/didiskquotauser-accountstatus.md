---
description: Ottiene lo stato dell'account dell'utente.
title: DIDiskQuotaUser.AccountStatus - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.AccountStatus
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: ff2234f7-4758-43c7-a3c2-8fb980b27c04
ms.openlocfilehash: e27e86fadab02616f91a4838acfc4be93e985ebd
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841652"
---
# <a name="didiskquotauseraccountstatus-property"></a>DIDiskQuotaUser.AccountStatus - proprietà

Ottiene lo stato dell'account dell'utente.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
iAccountStatus = DIDiskQuotaUser.AccountStatus
```



## <a name="property-value"></a>Valore proprietà

Questa proprietà può assumere uno dei valori seguenti.



| Stato            | Valore | Descrizione                         |
|-------------------|-------|-------------------------------------|
| dqAcctResolved    | 0     | Le informazioni sull'account vengono risolte.    |
| dqAcctUnavailable | 1     | Le informazioni sull'account non sono disponibili. |
| dqAcctDeleted     | 2     | L'account è stato eliminato.           |
| dqAcctInvalid     | 3     | L'account non è valido.                 |
| dqAcctUnknown     | 4     | Impossibile trovare l'account.            |
| dqAcctUnresolved  | 5     | Le informazioni sull'account non sono risolte.  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5.0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto DIDiskQuotaUser**](didiskquotauser-object.md)
</dt> </dl>

 

 




