---
title: Metodo INapEnforcementClientConnection SetIsolationInfo (NapEnforcementClient. h)
description: Viene usato da NapAgent per impostare le informazioni di isolamento del client.
ms.assetid: e92d8762-4ae9-40e5-a18e-7da757aa6f9e
keywords:
- NAP metodo SetIsolationInfo
- Metodo SetIsolationInfo NAP, interfaccia INapEnforcementClientConnection
- Interfaccia INapEnforcementClientConnection NAP, metodo SetIsolationInfo
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetIsolationInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c1cfd7ad227fec6942e0660769f52b3d4f12201
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740927"
---
# <a name="inapenforcementclientconnectionsetisolationinfo-method"></a>Metodo INapEnforcementClientConnection:: SetIsolationInfo

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapEnforcementClientConnection:: SetIsolationInfo** viene usato da napagent per impostare le informazioni di isolamento del client.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetIsolationInfo(
  [in] const IsolationInfo *isolationInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*isolationInfo* \[ in\]
</dt> <dd>

Puntatore a una struttura [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) che contiene lo stato di connettività del client.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

È possibile che vengano restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Operazione riuscita.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Errore delle autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |



 

## <a name="remarks"></a>Commenti

Queste informazioni vengono impostate da NapAgent dopo l'elaborazione di un SoHResponse e non devono essere impostate dall'applicazione.

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

 

 





