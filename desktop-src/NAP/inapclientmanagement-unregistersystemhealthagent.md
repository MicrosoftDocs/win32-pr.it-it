---
title: Metodo INapClientManagement UnregisterSystemHealthAgent (NapManagement.h)
description: Annulla la registrazione di un'applicazione SHA con il sistema di Protezione accesso alla rete.
ms.assetid: c3ad6f2a-c39a-4590-8487-24c802433845
keywords:
- Metodo UnregisterSystemHealthAgent NAP
- Metodo UnregisterSystemHealthAgent NAP , interfaccia INapClientManagement
- Interfaccia INapClientManagement NAP, metodo UnregisterSystemHealthAgent
topic_type:
- apiref
api_name:
- INapClientManagement.UnregisterSystemHealthAgent
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad43df1c7edeb2525ff5c8901278d082c4ba299ea78d56c67a4380f8a7bab019
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134509"
---
# <a name="inapclientmanagementunregistersystemhealthagent-method"></a>Metodo INapClientManagement::UnregisterSystemHealthAgent

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo UnregisterSystemHealthAgent** annulla la registrazione di un'applicazione SHA con il sistema di Protezione accesso alla rete.

## <a name="syntax"></a>Sintassi


```C++
HRESULT UnregisterSystemHealthAgent(
  [in] SystemHealthEntityId id
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*id* \[ in\]
</dt> <dd>

[**SystemHealthEntityId che**](nap-datatypes.md) identifica l'agente integrità sistema di cui annullare la registrazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un codice di stato HRESULT che include, a sua volta, uno degli elementi seguenti.



| Codice restituito                                                                                         | Descrizione                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | Operazione riuscita.<br/>                                   |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl>      | Errore di autorizzazione, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>       | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |
| <dl> <dt>**PROTEZIONE \_ ACCESSO ALLA RETE E ANCORA \_ \_ ASSOCIATA**</dt> </dl> | L'SHA rimane associato e non è stato possibile annullare la registrazione.<br/>    |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                               |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                         |
| Intestazione<br/>                   | <dl> <dt>NapManagement.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapManagement.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapClientManagement**](inapclientmanagement.md)
</dt> </dl>

 

 





