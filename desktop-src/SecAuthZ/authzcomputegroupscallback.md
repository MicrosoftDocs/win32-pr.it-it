---
description: Funzione definita dall'applicazione che crea un elenco di identificatori di sicurezza (SID) che si applicano a un client. AuthzComputeGroupsCallback è un segnaposto per il nome della funzione definita dall'applicazione.
ms.assetid: c20a02a0-5303-4433-a484-5a89999b32b9
title: Funzione di callback AuthzComputeGroupsCallback
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzComputeGroupsCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 3728f8114d87d07ddb33dd77a6fda5db30d07cf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760829"
---
# <a name="authzcomputegroupscallback-callback-function"></a>Funzione di callback AuthzComputeGroupsCallback

La funzione **AuthzComputeGroupsCallback** è una funzione definita dall'applicazione che crea un elenco di [*identificatori di sicurezza*](/windows/desktop/SecGloss/s-gly) (SID) che si applicano a un client. **AuthzComputeGroupsCallback** è un segnaposto per il nome della funzione definita dall'applicazione.

## <a name="syntax"></a>Sintassi


```C++
BOOL CALLBACK AuthzComputeGroupsCallback(
  _In_  AUTHZ_CLIENT_CONTEXT_HANDLE hAuthzClientContext,
  _In_  PVOID                       Args,
  _Out_ PSID_AND_ATTRIBUTES         *pSidAttrArray,
  _Out_ PDWORD                      pSidCount,
  _Out_ PSID_AND_ATTRIBUTES         *pRestrictedSidAttrArray,
  _Out_ PDWORD                      pRestrictedSidCount
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hAuthzClientContext* \[ in\]
</dt> <dd>

Handle per un contesto client.

</dd> <dt>

*Argomenti* \[ in\]
</dt> <dd>

Dati passati nel parametro *DynamicGroupArgs* di una chiamata alla funzione [**AuthzInitializeContextFromAuthzContext**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext), [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid)o [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) .

</dd> <dt>

*pSidAttrArray* \[ out\]
</dt> <dd>

Puntatore a una variabile puntatore che riceve l'indirizzo di una matrice di strutture di [**SID \_ e \_ attributi**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) . Queste strutture rappresentano i gruppi ai quali appartiene il client.

</dd> <dt>

*pSidCount* \[ out\]
</dt> <dd>

Numero di strutture in *pSidAttrArray*.

</dd> <dt>

*pRestrictedSidAttrArray* \[ out\]
</dt> <dd>

Puntatore a una variabile puntatore che riceve l'indirizzo di una matrice di strutture di [**SID \_ e \_ attributi**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) . Queste strutture rappresentano i gruppi da cui il client è limitato.

</dd> <dt>

*pRestrictedSidCount* \[ out\]
</dt> <dd>

Numero di strutture in *pSidRestrictedAttrArray*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione restituisce correttamente un elenco di SID, il valore restituito è **true**.

Se la funzione ha esito negativo, il valore restituito è **false**.

## <a name="remarks"></a>Commenti

Le applicazioni possono inoltre aggiungere SID al contesto client chiamando [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext).

Le variabili di attributo devono essere sotto forma di espressione se utilizzate con operatori logici; in caso contrario, vengono valutati come sconosciuti.

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

[**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext)
</dt> <dt>

[**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck)
</dt> <dt>

[**AuthzInitializeContextFromAuthzContext**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext)
</dt> <dt>

[**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid)
</dt> <dt>

[**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken)
</dt> <dt>

[**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> <dt>

[**SID \_ e \_ attributi**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes)
</dt> </dl>

 

