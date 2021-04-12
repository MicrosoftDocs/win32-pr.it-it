---
title: Metodo INapSystemHealthAgentBinding NotifySoHChange (NapSystemHealthAgent. h)
description: Viene usato da SHAs quando cambia il rapporto di integrità.
ms.assetid: 3a653282-03b0-49d5-833f-966497f46faa
keywords:
- NAP metodo NotifySoHChange
- Metodo NotifySoHChange NAP, interfaccia INapSystemHealthAgentBinding
- Interfaccia INapSystemHealthAgentBinding NAP, metodo NotifySoHChange
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.NotifySoHChange
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b18c03be03c4bc5282e9ea62ec10d5356871cf5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518946"
---
# <a name="inapsystemhealthagentbindingnotifysohchange-method"></a>Metodo INapSystemHealthAgentBinding:: NotifySoHChange

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapSystemHealthAgentBinding:: NotifySoHChange** viene usato da Shas quando il rapporto di integrità viene modificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT NotifySoHChange();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

È possibile che vengano restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                             | Descrizione                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Operazione riuscita.<br/>                                                                                                |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>         | Errore delle autorizzazioni, accesso negato.<br/>                                                                                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/>                                                             |
| <dl> <dt>**NAP \_ E \_ non \_ inizializzato**</dt> </dl> | SHA non è stato inizializzato in precedenza.<br/>                                                                        |
| <dl> <dt>**RPC \_ E \_ disconnessa**</dt> </dl>     | Il NapAgent è stato arrestato. Questo oggetto verrà ripristinato automaticamente e riassociato a NapAgent, una volta riavviato.<br/> |



 

## <a name="remarks"></a>Commenti

SHAs non deve chiamare questa API speculativamente perché comporta uno scambio di rapporto di integrità in rete. Le chiamate a questa API devono essere effettuate solo quando necessario.

Il NapAgent non tiene presente questo thread per elaborare la modifica del rapporto di integrità. Viene invece restituito immediatamente e la modifica viene elaborata in modo asincrono.

SHA deve chiamare [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) prima di chiamare questo metodo o qualsiasi altro metodo dell'interfaccia [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





