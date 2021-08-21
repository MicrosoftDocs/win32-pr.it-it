---
title: Metodo INapEnforcementClientBinding GetSoHRequest (NapEnforcementClient.h)
description: Viene usato dal client di imposizione per recuperare una richiesta SoH per una connessione specifica.
ms.assetid: 6fce6e84-ce03-48f2-957b-a41efe044fc5
keywords:
- Metodo GetSoHRequest nap
- Metodo GetSoHRequest NAP, interfaccia INapEnforcementClientBinding
- Metodo GetSoHRequest dell'interfaccia INapEnforcementClientBinding nap
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.GetSoHRequest
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 780f144c6f4613006940069896aa8382006b179631acd83283121ee3c64ec0d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134337"
---
# <a name="inapenforcementclientbindinggetsohrequest-method"></a>Metodo INapEnforcementClientBinding::GetSoHRequest

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo INapEnforcementClientBinding::GetSoHRequest** viene usato dal client di imposizione per recuperare una richiesta SoH per una connessione specifica.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSoHRequest(
  [in]  INapEnforcementClientConnection *connection,
  [out] BOOL                            *retriggerHint
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*connessione* \[ Pollici\]
</dt> <dd>

Puntatore COM a [**un'interfaccia INapEnforcementClientConnection.**](inapenforcementclientconnection.md) NapAgent non contiene riferimenti all'oggetto associato a questa interfaccia dopo il completamento del metodo .

</dd> <dt>

*retriggerHint* \[ Cambio\]
</dt> <dd>

Puntatore a **un oggetto BOOL** che indica se la connessione deve essere ri-attivata. È **TRUE se** [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) è stato modificato dopo l'ultima chiamata di questa funzione o se [**ProbationTime**](nap-datatypes.md) è scaduto. In caso contrario, viene restituito **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Possono essere restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                             | Descrizione                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | L'operazione è riuscita.<br/>                            |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl>         | Errore di autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Limite di risorse di sistema: impossibile eseguire l'operazione.<br/> |
| <dl> <dt>**PROTEZIONE \_ ACCESSO ALLA RETE NON \_ \_ INIZIALIZZATA**</dt> </dl> | L'applicazione non è stata inizializzata in precedenza.<br/>       |



 

## <a name="remarks"></a>Commenti

NapAgent imposta [**SoHRequest sull'oggetto**](/windows/win32/api/naptypes/ns-naptypes-soh) connessione.

Se un [**oggetto SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) era in sospeso per questa connessione, viene eliminato e gli SHA vengono informati di **SoHRequest orfani.**

Il client di imposizione deve chiamare il metodo [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) prima di chiamare questo o qualsiasi altro metodo [**dell'interfaccia INapEnforcementClientBinding.**](inapenforcementclientbinding.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                      |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>


</dt> <dt>

[**INapEnforcementClientBinding**](inapenforcementclientbinding.md)
</dt> </dl>

 

 





