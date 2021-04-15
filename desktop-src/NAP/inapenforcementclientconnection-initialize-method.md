---
title: Metodo Initialize INapEnforcementClientConnection (NapEnforcementClient. h)
description: Inizializza la connessione client.
ms.assetid: da72bfc3-9551-4fb0-b9a5-2931c14f618f
keywords:
- Metodo di inizializzazione NAP
- Metodo Initialize NAP, interfaccia INapEnforcementClientConnection
- Interfaccia NAP di INapEnforcementClientConnection, metodo Initialize
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.Initialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b51f12025bbddb8a9e795a97f2ed443344327a17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475994"
---
# <a name="inapenforcementclientconnectioninitialize-method"></a>Metodo INapEnforcementClientConnection:: Initialize

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapEnforcementClientConnection:: Initialize** Inizializza la connessione client.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Initialize(
  [in] EnforcementEntityId id
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ID* \[ in\]
</dt> <dd>

Puntatore a un [**EnforementEntityId**](nap-datatypes.md) che identifica il client di imposizione che richiede la connessione. Questo valore viene impostato da NapAgent durante la creazione della connessione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

È possibile che vengano restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Operazione riuscita.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Errore delle autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |



 

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

 

 





