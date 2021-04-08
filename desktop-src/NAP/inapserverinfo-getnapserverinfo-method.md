---
title: Metodo INapServerInfo GetNapServerInfo (NapServerManagement. h)
description: Recupera le informazioni sul server NAP.
ms.assetid: 02f7ce40-3443-4263-86b2-4276cbc7b694
keywords:
- NAP metodo GetNapServerInfo
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
ms.openlocfilehash: 5b182b9e1a5c8d7974128b062fd284c5af3f060f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743887"
---
# <a name="inapserverinfogetnapserverinfo-method"></a>Metodo INapServerInfo:: GetNapServerInfo

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapServerInfo:: GetNapServerInfo** recupera le informazioni sul server NAP.

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

*nomeserver* \[ out\]
</dt> <dd>

Puntatore a un puntatore a una struttura [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) contenente il nome del server.

</dd> <dt>

*Descrizione* \[ out\]
</dt> <dd>

Puntatore a un puntatore a una struttura [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) contenente la descrizione del server.

</dd> <dt>

*protocolVersion* \[ out\]
</dt> <dd>

Puntatore a un puntatore a una struttura [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) contenente la versione del protocollo.

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
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                               |
| Intestazione<br/>                   | <dl> <dt>NapServerManagement. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapServerManagement. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qsvrmgmt.dll</dt> </dl>            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapServerInfo**](inapserverinfo.md)
</dt> <dt>

[**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring)
</dt> </dl>

 

 





