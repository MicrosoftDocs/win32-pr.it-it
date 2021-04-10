---
title: Metodo INapEnforcementClientConnection2 SetInstalledShvs (NapEnforcementClient. h)
description: Utilizzato dall'agente NAP per impostare i validator di integrità di sistema installati (SHV) nel client.
ms.assetid: 38aa99b9-a15a-414d-91fc-128de8f5a654
keywords:
- NAP metodo SetInstalledShvs
- Metodo SetInstalledShvs NAP, interfaccia INapEnforcementClientConnection2
- Interfaccia INapEnforcementClientConnection2 NAP, metodo SetInstalledShvs
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.SetInstalledShvs
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6651cd5248094f82d9faa1862492f82648e94125
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121659"
---
# <a name="inapenforcementclientconnection2setinstalledshvs-method"></a>Metodo INapEnforcementClientConnection2:: SetInstalledShvs

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **SetInstalledShvs** viene utilizzato dall'agente NAP per impostare i validator di integrità del sistema installati (SHV) nel client.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetInstalledShvs(
  [in] SystemHealthEntityCount count,
  [in] SystemHealthEntityId    *ids
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*numero* \[ di in\]
</dt> <dd>

Valore [SystemHealthEntityCount](nap-datatypes.md) che specifica il numero di SHV da installare negli *ID*.

</dd> <dt>

*ID* \[ di in\]
</dt> <dd>

Puntatore a un valore [SystemHealthEntityId](nap-datatypes.md) che contiene un elenco di ID di convalida integrità sistema da installare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

È possibile che vengano restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                  | Descrizione                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>        | Il metodo è stato eseguito correttamente.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Il parametro *count* è 0 (zero).<br/> |



 

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

[**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





