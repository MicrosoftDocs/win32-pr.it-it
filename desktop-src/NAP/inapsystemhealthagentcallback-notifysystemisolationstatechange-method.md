---
title: Metodo INapSystemHealthAgentCallback NotifySystemIsolationStateChange (NapSystemHealthAgent. h)
description: Viene chiamato da NapAgent per indicare che lo stato di isolamento del sistema o l'ora di fine della prova è stato modificato.
ms.assetid: 0837eea4-6d92-44dc-b8b8-eca6be5f63e6
keywords:
- NAP metodo NotifySystemIsolationStateChange
- Metodo NotifySystemIsolationStateChange NAP, interfaccia INapSystemHealthAgentCallback
- Interfaccia INapSystemHealthAgentCallback NAP, metodo NotifySystemIsolationStateChange
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.NotifySystemIsolationStateChange
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c519d1569fe2e43cc6012ffa30c5bfb4402cc56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741954"
---
# <a name="inapsystemhealthagentcallbacknotifysystemisolationstatechange-method"></a>Metodo INapSystemHealthAgentCallback:: NotifySystemIsolationStateChange

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapSystemHealthAgentCallback:: NotifySystemIsolationStateChange** viene chiamato da napagent per indicare che è stato modificato lo stato di isolamento del sistema o l'ora di fine della prova.

## <a name="syntax"></a>Sintassi


```C++
HRESULT NotifySystemIsolationStateChange();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                          | Descrizione                   |
|--------------------------------------------------------------------------------------|-------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Indica l'esito positivo dell'operazione.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo di callback viene dichiarato dal sistema NAP e deve essere implementato dal writer SHA.

L'agente di integrità può eseguire una query sullo stato di protezione accesso alla rete del sistema utilizzando [**INapSystemHealthAgentBinding:: GetSystemIsolationInfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





