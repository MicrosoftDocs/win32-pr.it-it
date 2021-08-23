---
title: Metodo INapServerInfo GetNapServerInfo (NapServerManagement.h)
description: Recupera informazioni sul server protezione accesso alla rete.
ms.assetid: 02f7ce40-3443-4263-86b2-4276cbc7b694
keywords:
- Metodo GetNapServerInfo NAP
- Metodo GetNapServerInfo NAP, interfaccia INapServerInfo
- Interfaccia INapServerInfo NAP, metodo GetNapServerInfo
topic_type:
- apiref
api_name:
- INapServerInfo.GetNapServerInfo
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5eec9926e1a0bf94a1e3dac38c01a169d596c1c00bf032b8f6954f6331d5a4d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626131"
---
# <a name="inapserverinfogetnapserverinfo-method"></a>Metodo INapServerInfo::GetNapServerInfo

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo INapServerInfo::GetNapServerInfo** recupera informazioni sul server nap.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetNapServerInfo(
  [out] CountedString **serverName,
  [out] CountedString **serverDescription,
  [out] CountedString **protocolVersion
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*serverName* \[ Cambio\]
</dt> <dd>

Puntatore a un puntatore a [**una struttura CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) che contiene il nome del server.

</dd> <dt>

*serverDescription* \[ Cambio\]
</dt> <dd>

Puntatore a un puntatore a una [**struttura CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) contenente la descrizione del server.

</dd> <dt>

*protocolVersion* \[ Cambio\]
</dt> <dd>

Puntatore a un puntatore a [**una struttura CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) che contiene la versione del protocollo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Possono essere restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Operazione riuscita.<br/>                                    |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl> | Errore di autorizzazione, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                               |
| Intestazione<br/>                   | <dl> <dt>NapServerManagement.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapServerManagement.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qsvrmgmt.dll</dt> </dl>            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapServerInfo**](inapserverinfo.md)
</dt> <dt>

[**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring)
</dt> </dl>

 

 





