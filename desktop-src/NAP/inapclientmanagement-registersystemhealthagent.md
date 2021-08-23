---
title: Metodo INapClientManagement RegisterSystemHealthAgent (NapManagement.h)
description: Registra un'istanza di SHA con il sistema di Protezione accesso alla rete.
ms.assetid: 37acfd11-8282-42ba-ae02-9a45c4509b8b
keywords:
- Metodo RegisterSystemHealthAgent NAP
- Metodo RegisterSystemHealthAgent NAP, interfaccia INapClientManagement
- Interfaccia INapClientManagement NAP, metodo RegisterSystemHealthAgent
topic_type:
- apiref
api_name:
- INapClientManagement.RegisterSystemHealthAgent
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52e028e1f3dab17fb154ad1676acbf14fe1a31ce69a8f4c511e7f1447d2303bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803151"
---
# <a name="inapclientmanagementregistersystemhealthagent-method"></a>Metodo INapClientManagement::RegisterSystemHealthAgent

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo RegisterSystemHealthAgent** registra un'applicazione SHA con il sistema di Protezione accesso alla rete.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RegisterSystemHealthAgent(
  [in] const NapComponentRegistrationInfo *agent
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*agente* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) che contiene le informazioni di registrazione per l'SHA.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un codice di stato HRESULT che include, a sua volta, uno degli elementi seguenti.



| Codice restituito                                                                                            | Descrizione                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Operazione riuscita.<br/>                                   |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl>         | Errore di autorizzazione, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |
| <dl> <dt>**ID \_ IN CONFLITTO DI PROTEZIONE ACCESSO ALLA RETE \_ \_ E**</dt> </dl> | Un sha che usa questo ID è già registrato.<br/>         |



 

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

 

 





