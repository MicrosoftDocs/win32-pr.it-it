---
title: Metodo INapEnforcementClientConnection GetEnforcerPrivateData (NapEnforcementClient. h)
description: Viene usato dall'applicazione per ottenere i dati privati.
ms.assetid: a1f5b5a7-c862-4e5b-bf9c-b137f99f6165
keywords:
- NAP metodo GetEnforcerPrivateData
- Metodo GetEnforcerPrivateData NAP, interfaccia INapEnforcementClientConnection
- Interfaccia INapEnforcementClientConnection NAP, metodo GetEnforcerPrivateData
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetEnforcerPrivateData
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d592ad0b11abf2b349b0810d67b05f2ee4086060
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121598"
---
# <a name="inapenforcementclientconnectiongetenforcerprivatedata-method"></a>Metodo INapEnforcementClientConnection:: GetEnforcerPrivateData

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapEnforcementClientConnection:: GetEnforcerPrivateData** viene usato dall'applicazione per ottenere i dati privati.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetEnforcerPrivateData(
  [out] PrivateData **privateData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PrivateData* \[ out\]
</dt> <dd>

Puntatore a un puntatore a un BLOB di dati opachi [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) che può essere interpretato solo dall'applicazione.

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

 

 





