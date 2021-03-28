---
description: Ottiene lo stato dell'account dell'utente.
title: Proprietà DIDiskQuotaUser. AccountStatus
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
ms.openlocfilehash: 155ae627d70c5125fd0d1d501062224450fc8e3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977258"
---
# <a name="didiskquotauseraccountstatus-property"></a>Proprietà DIDiskQuotaUser. AccountStatus

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
| dqAcctUnresolved  | 5     | Informazioni sull'account non risolte.  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5,0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto DIDiskQuotaUser**](didiskquotauser-object.md)
</dt> </dl>

 

 




