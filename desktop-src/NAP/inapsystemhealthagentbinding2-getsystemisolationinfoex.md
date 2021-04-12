---
title: Metodo INapSystemHealthAgentBinding2 GetSystemIsolationInfoEx (NapSystemHealthAgent. h)
description: Viene chiamato da SHAs per determinare lo stato di isolamento del sistema e lo stato di isolamento esteso.
ms.assetid: 237e5539-889c-457d-8db0-bf3379f28b85
keywords:
- NAP metodo GetSystemIsolationInfoEx
- Metodo GetSystemIsolationInfoEx NAP, interfaccia INapSystemHealthAgentBinding2
- Interfaccia INapSystemHealthAgentBinding2 NAP, metodo GetSystemIsolationInfoEx
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding2.GetSystemIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2643d62afba1a35ebd96b8b39ea2fcf90397576
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517932"
---
# <a name="inapsystemhealthagentbinding2getsystemisolationinfoex-method"></a>Metodo INapSystemHealthAgentBinding2:: GetSystemIsolationInfoEx

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapSystemHealthAgentBinding2:: GetSystemIsolationInfoEx** viene chiamato da Shas per determinare lo stato di isolamento del sistema e lo stato di isolamento esteso.

> [!Note]  
> Usare [**INapSystemHealthAgentBinding:: GetSystemIsolationInfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md) per determinare solo lo stato di isolamento del sistema.

 

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSystemIsolationInfoEx(
  [out] IsolationInfoEx **isolationInfo,
  [out] BOOL            *unknownConnections
) const;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*isolationInfo* \[ out\]
</dt> <dd>

Puntatore a un puntatore a una struttura [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) che contiene lo stato di isolamento esteso del sistema per le connessioni note. *isolationInfo* indica se il sistema è in uno stato di accesso limitato, di prova o senza restrizioni, nonché di informazioni [**ExtendedIsolationState**](/windows/win32/api/naptypes/ne-naptypes-extendedisolationstate) .

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

SHA deve liberare la struttura [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) chiamando [**FreeIsolationInfoEx**](freeisolationinfoex.md).

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

[**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md)
</dt> </dl>

 

 





