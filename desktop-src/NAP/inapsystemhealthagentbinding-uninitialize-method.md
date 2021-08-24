---
title: Metodo INapSystemHealthAgentBinding Uninitialize (NapSystemHealthAgent.h)
description: Fa in modo che NapAgent rilasci tutti i relativi riferimenti ai puntatori COM dell'agente di integrità del sistema.
ms.assetid: 8b9fabc9-7453-41fe-a1e7-2ec5fa275a3a
keywords:
- Annullare l'inizializzazione del metodo NAP
- Metodo Uninitialize NAP , interfaccia INapSystemHealthAgentBinding
- Interfaccia INapSystemHealthAgentBinding NAP , metodo Uninitialize
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.Uninitialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4eeefaad67130772a44103c721cc9f4efd02d3b43f54fc27c8d2f1bd40983522
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119802761"
---
# <a name="inapsystemhealthagentbindinguninitialize-method"></a>Metodo INapSystemHealthAgentBinding::Uninitialize

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo INapSystemHealthAgentBinding::Uninitialize** fa in modo che NapAgent rilasci tutti i riferimenti ai puntatori COM dell'agente di integrità del sistema.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Uninitialize();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Possono essere restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                             | Descrizione                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Operazione riuscita.<br/>                                                                                                |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl>         | Errore di autorizzazioni, accesso negato.<br/>                                                                                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Limite di risorse di sistema: impossibile eseguire l'operazione.<br/>                                                             |
| <dl> <dt>**PROTEZIONE \_ ACCESSO ALLA RETE NON \_ \_ INIZIALIZZATA**</dt> </dl> | L'SHA non è stato inizializzato in precedenza.<br/>                                                                        |
| <dl> <dt>**RPC \_ E \_ DISCONNESSO**</dt> </dl>     | NapAgent è stato arrestato. Questo oggetto verrà ripristinato automaticamente e riassociato a NapAgent, dopo il riavvio.<br/> |



 

## <a name="remarks"></a>Commenti

NapAgent blocca l'esecuzione di questa chiamata al metodo fino al completamento di tutte le chiamate esistenti sulle interfacce di associazione e callback.

L'SHA deve chiamare [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) prima di chiamare questo metodo o qualsiasi altro metodo dell'interfaccia [**INapSystemHealthAgentBinding2.**](inapsystemhealthagentbinding2.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                      |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





