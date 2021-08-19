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
ms.openlocfilehash: f51903708bd3993e2837d65107798b1ff546c5857eff3bbed028ed4d6dda47f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783755"
---
# <a name="authzfreecentralaccesspolicycallback-callback-function"></a>Funzione di callback AuthzFreeCentralAccessPolicyCallback

*La funzione AuthzFreeCentralAccessPolicyCallback* è una funzione definita dall'applicazione che libera la memoria allocata dalla [*funzione AuthzGetCentralAccessPolicyCallback.*](authzgetcentralaccesspolicycallback-.md) *AuthzFreeCentralAccessPolicyCallback è* un segnaposto per il nome della funzione definita dall'applicazione.

## <a name="syntax"></a>Sintassi


```C++
BOOL CALLBACK AuthzFreeCentralAccessPolicyCallback(
  _In_ PVOID pCentralAccessPolicy
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pCentralAccessPolicy* \[ Pollici\]
</dt> <dd>

Puntatore ai criteri di accesso centrale da liberare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce **TRUE.**

Se la funzione non è in grado di eseguire la valutazione, restituisce **FALSE.** Usare [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) per restituire un errore alla funzione di controllo dell'accesso.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**AUTHZ \_ INIT \_ INFO**](/windows/desktop/api/Authz/ns-authz-authz_init_info)
</dt> <dt>

[*AuthzGetCentralAccessPolicyCallback*](authzgetcentralaccesspolicycallback-.md)
</dt> </dl>

 

 
