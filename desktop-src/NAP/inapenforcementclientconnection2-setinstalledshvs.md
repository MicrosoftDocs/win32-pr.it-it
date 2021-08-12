---
title: Metodo SetInstalledShvs INapEnforcementClientConnection2 (NapEnforcementClient.h)
description: Usato dall'agente protezione accesso alla rete per impostare i validator dell'integrità del sistema installati nel client.
ms.assetid: 38aa99b9-a15a-414d-91fc-128de8f5a654
keywords:
- Metodo SetInstalledShvs nap
- Metodo SetInstalledShvs NAP , interfaccia INapEnforcementClientConnection2
- Interfaccia INapEnforcementClientConnection2 nap, metodo SetInstalledShvs
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
ms.openlocfilehash: 31a95f9ad491b0b5a6354bb5c44a7ff54f64b29ffa715762ab43a7752e3a3ac0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118621336"
---
# <a name="inapenforcementclientconnection2setinstalledshvs-method"></a>Metodo INapEnforcementClientConnection2::SetInstalledShvs

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo SetInstalledShvs** viene usato dall'agente protezione accesso alla rete per impostare i validator dell'integrità del sistema installati nel client.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetInstalledShvs(
  [in] SystemHealthEntityCount count,
  [in] SystemHealthEntityId    *ids
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*count* \[ Pollici\]
</dt> <dd>

Valore [SystemHealthEntityCount](nap-datatypes.md) che specifica il numero di shv da installare negli *ID*.

</dd> <dt>

*ID* \[ Pollici\]
</dt> <dd>

Puntatore a un [valore SystemHealthEntityId](nap-datatypes.md) che contiene un elenco di ID SHV da installare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Possono essere restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                  | Descrizione                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>        | Il metodo è stato eseguito correttamente.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Il *parametro count* è 0 (zero).<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                      |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





