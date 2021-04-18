---
description: "Il \\_ \\_ tipo di dati dell'handle di enumerazione LSA viene usato dalla funzione LSA che enumera gli oggetti trustedDomain: LsaEnumerateTrustedDomainsEx."
ms.assetid: 99dad3aa-cb92-4b7e-8a18-2c977cb2737c
title: LSA_ENUMERATION_HANDLE (Ntsecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db71e9522a188956a7aa838b11ba74f08bde39c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312770"
---
# <a name="lsa_enumeration_handle"></a>\_handle di enumerazione LSA \_

Il tipo di dati dell' **\_ \_ handle di enumerazione LSA** viene usato dalla funzione LSA che enumera gli oggetti [**trustedDomain**](trusteddomain-object.md) : [**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex). Questa funzione è progettata in modo da poter effettuare più chiamate per enumerare tutti gli oggetti di un determinato tipo nel database.

Nella chiamata di funzione di enumerazione iniziale si passa un puntatore a una variabile **dell' \_ \_ handle di enumerazione LSA** inizializzata su zero. La funzione aggiorna questo valore. Se la funzione restituisce un valore che indica la presenza di più oggetti da enumerare, chiamare di nuovo la funzione e passare il valore dell' **\_ \_ handle di enumerazione LSA** aggiornato per ottenere un'enumerazione continua dal punto in cui l'enumerazione precedente è stata interrotta.


```C++
typedef ULONG LSA_ENUMERATION_HANDLE, *PLSA_ENUMERATION_HANDLE;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Ntsecapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex)
</dt> </dl>

 

 




