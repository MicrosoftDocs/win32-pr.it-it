---
description: Funzione definita dall'applicazione che gestisce le voci di controllo di accesso (ACE) di callback durante un controllo di accesso.
ms.assetid: e8a510e6-0739-4765-ad07-3bcb1b9c905c
title: Funzione di callback AuthzAccessCheckCallback
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzAccessCheckCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 82e100092dd7c59e9cc689aa8723365fae8bed29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234340"
---
# <a name="authzaccesscheckcallback-callback-function"></a>Funzione di callback AuthzAccessCheckCallback

La funzione **AuthzAccessCheckCallback** è una funzione definita dall'applicazione che gestisce le [*voci di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACE) di callback durante un controllo di accesso. **AuthzAccessCheckCallback** è un segnaposto per il nome della funzione definita dall'applicazione. L'applicazione registra questo callback chiamando [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager).

## <a name="syntax"></a>Sintassi


```C++
BOOL CALLBACK AuthzAccessCheckCallback(
  _In_     AUTHZ_CLIENT_CONTEXT_HANDLE hAuthzClientContext,
  _In_     PACE_HEADER                 pAce,
  _In_opt_ PVOID                       pArgs,
  _Inout_  PBOOL                       pbAceApplicable
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hAuthzClientContext* \[ in\]
</dt> <dd>

Handle per un contesto client.

</dd> <dt>

*velocità* \[ in\]
</dt> <dd>

Puntatore alla voce ACE da valutare per l'inclusione nella chiamata alla funzione [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) .

</dd> <dt>

*pArgs* \[ in, facoltativo\]
</dt> <dd>

Dati passati nel parametro *DynamicGroupArgs* della chiamata a [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) o [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck).

</dd> <dt>

*pbAceApplicable* \[ in uscita\]
</dt> <dd>

Puntatore a una variabile booleana che riceve i risultati della valutazione della logica definita dall'applicazione.

I risultati sono **true** se la logica determina che la voce ACE è applicabile e verrà inclusa nella chiamata a [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck); in caso contrario, i risultati sono **false**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce **true**.

Se la funzione non è in grado di eseguire la valutazione, viene restituito **false**. Usare [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) per restituire un errore alla funzione di controllo di accesso.

## <a name="remarks"></a>Commenti

Le variabili degli attributi di sicurezza devono essere presenti nel contesto client se si fa riferimento a in un'espressione condizionale. in caso contrario, il termine espressione condizionale che vi fa riferimento restituisce Unknown.

Per ulteriori informazioni, vedere il funzionamento di [AccessCheck](how-dacls-control-access-to-an-object.md) e panoramica dei [criteri di autorizzazione centralizzati](centralized-authorization-policy.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                   |
| Componente ridistribuibile<br/>          | Windows Server 2003 Administration Tools Pack in Windows XP<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di controllo di accesso di base](authorization-functions.md)
</dt> <dt>

[Criteri di autorizzazione centralizzati](centralized-authorization-policy.md)
</dt> <dt>

[Funzionamento di AccessCheck](how-dacls-control-access-to-an-object.md)
</dt> <dt>

[**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)
</dt> <dt>

[**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck)
</dt> <dt>

[**AuthzInitializeRemoteResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager)
</dt> <dt>

[**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> </dl>

 

