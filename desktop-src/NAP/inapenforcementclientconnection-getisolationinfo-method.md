---
title: Metodo INapEnforcementClientConnection GetIsolationInfo (NapEnforcementClient. h)
description: Viene usato per ottenere le informazioni di isolamento del client.
ms.assetid: 33040554-dcbe-4563-b047-fc7e28bac55c
keywords:
- NAP metodo GetIsolationInfo
- Metodo GetIsolationInfo NAP, interfaccia INapEnforcementClientConnection
- Interfaccia INapEnforcementClientConnection NAP, metodo GetIsolationInfo
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetIsolationInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 890f7268801fda77a9794ed21c4d36e78a52dd5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964962"
---
# <a name="inapenforcementclientconnectiongetisolationinfo-method"></a>Metodo INapEnforcementClientConnection:: GetIsolationInfo

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapEnforcementClientConnection:: GetIsolationInfo** viene usato per ottenere le informazioni di isolamento del client.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetIsolationInfo(
  [out] IsolationInfo **isolationInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*isolationInfo* \[ out\]
</dt> <dd>

Puntatore a un puntatore a una struttura [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) che contiene lo stato di connettività del client.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

È possibile che vengano restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Operazione riuscita.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Errore delle autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |



 

## <a name="remarks"></a>Commenti

Queste informazioni vengono impostate da NapAgent dopo l'elaborazione di un [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) e non devono essere impostate dall'applicazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapEnforcementClient. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapEnforcementClient. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





