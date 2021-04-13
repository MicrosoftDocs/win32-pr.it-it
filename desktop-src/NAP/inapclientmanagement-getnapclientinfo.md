---
title: Metodo INapClientManagement GetNapClientInfo (NapManagement. h)
description: Recupera le informazioni sul client di protezione accesso alla rete.
ms.assetid: c0b57cab-729b-40b2-81d2-32a961e377a5
keywords:
- NAP metodo GetNapClientInfo
- Metodo GetNapClientInfo NAP, interfaccia INapClientManagement
- Interfaccia INapClientManagement NAP, metodo GetNapClientInfo
topic_type:
- apiref
api_name:
- INapClientManagement.GetNapClientInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a11fc496374f2a7f0b7842e22212013149f44f22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518244"
---
# <a name="inapclientmanagementgetnapclientinfo-method"></a>Metodo INapClientManagement:: GetNapClientInfo

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **GetNapClientInfo** recupera le informazioni sul client di protezione accesso alla rete.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetNapClientInfo(
  [out] BOOL          *isNapEnabled,
  [out] CountedString **clientName,
  [out] CountedString **clientDescription,
  [out] CountedString **protocolVersion
) const;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*isNapEnabled* \[ out\]
</dt> <dd>

Puntatore a un BOOL che è impostato su **true** se NAP è abilitato; in caso contrario, è impostato su **false**.

</dd> <dt>

*clientname* \[ out\]
</dt> <dd>

Puntatore a un puntatore a una struttura [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) contenente il nome del client.

</dd> <dt>

*clientDescription* \[ out\]
</dt> <dd>

Puntatore a un puntatore a una struttura [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) contenente la descrizione del client.

</dd> <dt>

*protocolVersion* \[ out\]
</dt> <dd>

Puntatore a un puntatore a una struttura [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) contenente la versione del protocollo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un codice di stato HRESULT incluso ma non limitato a uno dei valori seguenti.



| Codice restituito                                                                                         | Descrizione                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                | Operazione riuscita.<br/>                                   |
| <dl> <dt>**E \_ AccessDenied**</dt> </dl>      | Errore delle autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl>       | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |
| <dl> <dt>**RPC \_ E \_ disconnessa**</dt> </dl> | NapAgent non è in esecuzione.<br/>                            |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                               |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                         |
| Intestazione<br/>                   | <dl> <dt>NapManagement. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapManagement. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapClientManagement**](inapclientmanagement.md)
</dt> </dl>

 

 





