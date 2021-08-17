---
title: Metodo INapSystemHealthAgentBinding GetSystemIsolationInfo (NapSystemHealthAgent.h)
description: Viene chiamato dagli sha per determinare lo stato di isolamento del sistema.
ms.assetid: 0401a846-0da2-4975-87bc-3e9fe8b5b67d
keywords:
- Metodo GetSystemIsolationInfo NAP
- Metodo GetSystemIsolationInfo NAP, interfaccia INapSystemHealthAgentBinding
- Interfaccia INapSystemHealthAgentBinding NAP, metodo GetSystemIsolationInfo
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.GetSystemIsolationInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9058b78bcff60b27bb27f25f11b785a8cd341f9addafe1829c1e8a7f3fb02a15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939558"
---
# <a name="inapsystemhealthagentbindinggetsystemisolationinfo-method"></a>Metodo INapSystemHealthAgentBinding::GetSystemIsolationInfo

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo INapSystemHealthAgentBinding::GetSystemIsolationInfo** viene chiamato dagli sha per determinare lo stato di isolamento del sistema.

> [!Note]  
> Usare [**INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx**](inapsystemhealthagentbinding2-getsystemisolationinfoex.md) per determinare lo stato di isolamento esteso del sistema.

 

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSystemIsolationInfo(
  [out] IsolationInfo **isolationInfo,
  [out] BOOL          *unknownConnections
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*isolationInfo* \[ Cambio\]
</dt> <dd>

Puntatore a un puntatore a una [**struttura IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) che contiene lo stato di isolamento del sistema per le connessioni note. *isolationInfoindicates* se il sistema si trova in uno stato di accesso con restrizioni, di sondaggio o di accesso senza restrizioni.

</dd> <dt>

*unknownConnections* \[ Cambio\]
</dt> <dd>

Puntatore a un **oggetto BOOL che** è **TRUE se** le connessioni sono in uno stato sconosciuto e FALSE in **caso contrario.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Possono essere restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                             | Descrizione                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Operazione riuscita.<br/>                                                                                                |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl>         | Errore di autorizzazione, accesso negato.<br/>                                                                                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/>                                                             |
| <dl> <dt>**PROTEZIONE \_ ACCESSO ALLA RETE E NON \_ \_ INIZIALIZZATA**</dt> </dl> | L'sha non è stato inizializzato in precedenza.<br/>                                                                        |
| <dl> <dt>**RPC \_ E \_ DISCONNESSO**</dt> </dl>     | NapAgent è stato arrestato. Questo oggetto verrà ripristinato automaticamente e riassociato a NapAgent, dopo il riavvio.<br/> |



 

## <a name="remarks"></a>Commenti

L'SHA deve [**chiamare Initialize**](inapsystemhealthagentbinding-initialize-method.md) prima di chiamare questo metodo o qualsiasi altro metodo dell'interfaccia [**INapSystemHealthAgentBinding2.**](inapsystemhealthagentbinding2.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                      |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





