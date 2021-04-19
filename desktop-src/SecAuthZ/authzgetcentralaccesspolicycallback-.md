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
ms.openlocfilehash: b96832fa647fde920a70ac3d6608c8ebb0048892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319921"
---
# <a name="authzgetcentralaccesspolicycallback-callback-function"></a>Funzione di callback AuthzGetCentralAccessPolicyCallback

La funzione *AuthzGetCentralAccessPolicyCallback* è una funzione definita dall'applicazione che recupera i criteri di accesso centrale. *AuthzGetCentralAccessPolicyCallback* è un segnaposto per il nome della funzione definita dall'applicazione.

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

*hAuthzClientContext* \[ in\]
</dt> <dd>

Handle per il contesto client.

</dd> <dt>

*capiti* \[ in\]
</dt> <dd>

ID dei criteri di accesso centrale da recuperare.

</dd> <dt>

*pArgs* \[ in, facoltativo\]
</dt> <dd>

Argomenti facoltativi passati alla funzione [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) tramite il membro **OptionalArguments** della struttura della [**\_ \_ richiesta di accesso AUTHZ**](/windows/desktop/api/Authz/ns-authz-authz_access_request) .

</dd> <dt>

*pCentralAccessPolicyApplicable* \[ out\]
</dt> <dd>

Puntatore a un valore booleano utilizzato dal gestore delle risorse per indicare se è necessario utilizzare un criterio di accesso centrale durante la valutazione dell'accesso.

</dd> <dt>

*ppCentralAccessPolicy* \[ out\]
</dt> <dd>

Puntatore ai criteri di accesso centrale da utilizzare per la valutazione dell'accesso. Se questo valore è **null**, viene applicato il limite predefinito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce **true**.

Se la funzione non è in grado di eseguire la valutazione, viene restituito **false**. Usare [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) per restituire un errore alla funzione di controllo di accesso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                   |
| Componente ridistribuibile<br/>          | Windows Server 2003 Administration Tools Pack in Windows XP<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_richiesta di accesso AUTHZ \_**](/windows/desktop/api/Authz/ns-authz-authz_access_request)
</dt> <dt>

[**\_informazioni init \_ AUTHZ**](/windows/desktop/api/Authz/ns-authz-authz_init_info)
</dt> <dt>

[**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)
</dt> </dl>

 

