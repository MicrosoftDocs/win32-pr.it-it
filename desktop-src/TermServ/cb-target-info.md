---
title: Struttura CB_TARGET_INFO (Cbclient. h)
description: Contiene informazioni sul computer di destinazione e sugli indirizzi IP in cui devono essere reindirizzate le connessioni in ingresso.
ms.assetid: 60612E10-9D82-4F38-87F7-B24F51E6EBDA
ms.tgt_platform: multiple
keywords:
- Struttura CB_TARGET_INFO Servizi Desktop remoto
- Puntatore alla struttura PCB_TARGET_INFO Servizi Desktop remoto
topic_type:
- apiref
api_name:
- CB_TARGET_INFO
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9bbb982636449075b758ac61178f5e97da47ce7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400400"
---
# <a name="cb_target_info-structure"></a>Struttura delle informazioni di \_ destinazione CB \_

Contiene informazioni sul computer di destinazione e sugli indirizzi IP in cui devono essere reindirizzate le connessioni in ingresso. Questa struttura viene utilizzata con il metodo [**IConnectionBrokerClient:: GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) .

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  WCHAR ServerName[128];
  DWORD AddressCount;
  WCHAR Addresses[CB_MAX_ADDRESSES][CB_IPADDRESS_LEN];
} CB_TARGET_INFO, *PCB_TARGET_INFO;
```



## <a name="members"></a>Members

<dl> <dt>

**ServerName**
</dt> <dd>

Rappresenta il nome di dominio completo del server di destinazione. Per uno scenario di RDV (Desktop remoto Virtualization), questo membro è **null**. Per uno scenario RDSH (Desktop remoto Session Host), questo membro contiene il nome del server in cui viene reindirizzata la connessione in ingresso.

</dd> <dt>

**AddressCount**
</dt> <dd>

Numero di voci valide nella matrice di **indirizzi** .

</dd> <dt>

**Indirizzi**
</dt> <dd>

Matrice di stringhe che contengono gli indirizzi IP in cui vengono reindirizzate le connessioni in ingresso. Il numero di elementi validi in questa matrice è specificato nel membro **AddressCount** .

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                  |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                        |
| Intestazione<br/>                   | <dl> <dt>Cbclient. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md)
</dt> </dl>

 

 





