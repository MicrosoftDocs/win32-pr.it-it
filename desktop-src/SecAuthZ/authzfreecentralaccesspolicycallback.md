---
description: La funzione AuthzFreeCentralAccessPolicyCallback è una funzione definita dall'applicazione che libera la memoria allocata dalla funzione AuthzGetCentralAccessPolicyCallback.
ms.assetid: F0859A67-4D20-4189-8F35-A78034E41E6A
title: Funzione di callback AuthzFreeCentralAccessPolicyCallback
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzFreeCentralAccessPolicyCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: d2139c9fa106b6070a3c043d417bdbf23379084b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234338"
---
# <a name="authzfreecentralaccesspolicycallback-callback-function"></a>Funzione di callback AuthzFreeCentralAccessPolicyCallback

La funzione *AuthzFreeCentralAccessPolicyCallback* è una funzione definita dall'applicazione che libera la memoria allocata dalla funzione [*AuthzGetCentralAccessPolicyCallback*](authzgetcentralaccesspolicycallback-.md) . *AuthzFreeCentralAccessPolicyCallback* è un segnaposto per il nome della funzione definita dall'applicazione.

## <a name="syntax"></a>Sintassi


```C++
BOOL CALLBACK AuthzFreeCentralAccessPolicyCallback(
  _In_ PVOID pCentralAccessPolicy
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pCentralAccessPolicy* \[ in\]
</dt> <dd>

Puntatore ai criteri di accesso centrale da liberare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce **true**.

Se la funzione non è in grado di eseguire la valutazione, viene restituito **false**. Usare [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) per restituire un errore alla funzione di controllo di accesso.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_informazioni init \_ AUTHZ**](/windows/desktop/api/Authz/ns-authz-authz_init_info)
</dt> <dt>

[*AuthzGetCentralAccessPolicyCallback*](authzgetcentralaccesspolicycallback-.md)
</dt> </dl>

 

 
