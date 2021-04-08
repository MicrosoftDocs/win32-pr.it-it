---
title: Metodo INapEnforcementClientConnection GetPrivateData (NapEnforcementClient. h)
description: Viene usato da NapAgent per ottenere i dati privati.
ms.assetid: d38ef523-b645-401f-b3a9-1315ef39931a
keywords:
- NAP metodo GetPrivateData
- Metodo GetPrivateData NAP, interfaccia INapEnforcementClientConnection
- Interfaccia INapEnforcementClientConnection NAP, metodo GetPrivateData
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetPrivateData
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6618ff7b25ad57cbb943107e80f299d9b6a68bea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873558"
---
# <a name="inapenforcementclientconnectiongetprivatedata-method"></a>Metodo INapEnforcementClientConnection:: GetPrivateData

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapEnforcementClientConnection:: GetPrivateData** viene usato da napagent per ottenere i dati privati.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetPrivateData(
  [out] PrivateData **privateData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PrivateData* \[ out\]
</dt> <dd>

Puntatore a un puntatore a un BLOB di dati opachi [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) che può essere interpretato solo da napagent.

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

 

 





