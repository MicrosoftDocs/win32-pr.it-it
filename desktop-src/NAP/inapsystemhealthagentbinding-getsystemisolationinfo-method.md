---
title: Metodo INapSystemHealthAgentBinding GetSystemIsolationInfo (NapSystemHealthAgent. h)
description: Viene chiamato da SHAs per determinare lo stato di isolamento del sistema.
ms.assetid: 0401a846-0da2-4975-87bc-3e9fe8b5b67d
keywords:
- NAP metodo GetSystemIsolationInfo
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
ms.openlocfilehash: d0323149be50cd8896a191ca57584cea0c015487
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479048"
---
# <a name="inapsystemhealthagentbindinggetsystemisolationinfo-method"></a>Metodo INapSystemHealthAgentBinding:: GetSystemIsolationInfo

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapSystemHealthAgentBinding:: GetSystemIsolationInfo** viene chiamato da Shas per determinare lo stato di isolamento del sistema.

> [!Note]  
> Usare [**INapSystemHealthAgentBinding2:: GetSystemIsolationInfoEx**](inapsystemhealthagentbinding2-getsystemisolationinfoex.md) per determinare lo stato di isolamento esteso del sistema.

 

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSystemIsolationInfo(
  [out] IsolationInfo **isolationInfo,
  [out] BOOL          *unknownConnections
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*isolationInfo* \[ out\]
</dt> <dd>

Puntatore a un puntatore a una struttura [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) che contiene lo stato di isolamento del sistema per le connessioni note. *isolationInfoindicates* se il sistema è in uno stato di accesso limitato, di prova o senza restrizioni.

</dd> <dt>

*unknownConnections* \[ out\]
</dt> <dd>

Puntatore a un **bool** che è **true** se le connessioni sono in uno stato sconosciuto e **false** in caso contrario.

</dd> </dl>

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

 

 





