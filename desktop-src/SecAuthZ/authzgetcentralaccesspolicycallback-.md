---
description: La funzione AuthzGetCentralAccessPolicyCallback è una funzione definita dall'applicazione che recupera i criteri di accesso centrale. AuthzGetCentralAccessPolicyCallback è un segnaposto per il nome della funzione definita dall'applicazione.
ms.assetid: 1D5831EF-ACA8-4EE9-A7C1-E1A3CB74CEC0
title: Funzione di callback AuthzGetCentralAccessPolicyCallback
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzGetCentralAccessPolicyCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 5e8fd0afbd901d48386859e9b5d3557a173cfe6a23d749dc776992a4aedebed1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783745"
---
# <a name="authzgetcentralaccesspolicycallback-callback-function"></a>Funzione di callback AuthzGetCentralAccessPolicyCallback

La *funzione AuthzGetCentralAccessPolicyCallback* è una funzione definita dall'applicazione che recupera i criteri di accesso centrale. *AuthzGetCentralAccessPolicyCallback è* un segnaposto per il nome della funzione definita dall'applicazione.

## <a name="syntax"></a>Sintassi


```C++
BOOL CALLBACK AuthzGetCentralAccessPolicyCallback (
  _In_     AUTHZ_CLIENT_CONTEXT_HANDLE hAuthzClientContext,
  _In_     PSID                        capid,
  _In_opt_ PVOID                       pArgs,
  _Out_    PBOOL                       pCentralAccessPolicyApplicable,
  _Out_    PVOID                       ppCentralAccessPolicy
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hAuthzClientContext* \[ Pollici\]
</dt> <dd>

Handle per il contesto client.

</dd> <dt>

*capid* \[ Pollici\]
</dt> <dd>

ID dei criteri di accesso centrale da recuperare.

</dd> <dt>

*pArgs* \[ in, facoltativo\]
</dt> <dd>

Argomenti facoltativi passati alla funzione [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) tramite il membro **OptionalArguments** della [**struttura AUTHZ \_ ACCESS \_ REQUEST.**](/windows/desktop/api/Authz/ns-authz-authz_access_request)

</dd> <dt>

*pCentralAccessPolicyApplicable* \[ Cambio\]
</dt> <dd>

Puntatore a un valore booleano usato dal gestore di risorse per indicare se i criteri di accesso centrale devono essere usati durante la valutazione dell'accesso.

</dd> <dt>

*ppCentralAccessPolicy* \[ Cambio\]
</dt> <dd>

Puntatore ai criteri di accesso centrale da usare per la valutazione dell'accesso. Se questo valore è **NULL,** viene applicato il cap predefinito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce **TRUE.**

Se la funzione non è in grado di eseguire la valutazione, restituisce **FALSE.** Usare [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) per restituire un errore alla funzione di controllo dell'accesso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                   |
| Componente ridistribuibile<br/>          | Windows Server 2003 Administration Tools Pack in Windows XP<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RICHIESTA DI ACCESSO AUTHZ \_ \_**](/windows/desktop/api/Authz/ns-authz-authz_access_request)
</dt> <dt>

[**AUTHZ \_ INIT \_ INFO**](/windows/desktop/api/Authz/ns-authz-authz_init_info)
</dt> <dt>

[**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)
</dt> </dl>

 

