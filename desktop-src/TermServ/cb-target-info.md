---
title: CB_TARGET_INFO (Cbclient.h)
description: Contiene informazioni sul computer di destinazione e sugli indirizzi IP in cui devono essere reindirizzate le connessioni in ingresso.
ms.assetid: 60612E10-9D82-4F38-87F7-B24F51E6EBDA
ms.tgt_platform: multiple
keywords:
- CB_TARGET_INFO struttura Servizi Desktop remoto
- PCB_TARGET_INFO puntatore alla struttura Servizi Desktop remoto
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
ms.openlocfilehash: 1e7c00e1997ee36b42b21b833942597d9b43f393b2bcdfcee1aa0ee18e3a4548
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001609"
---
# <a name="cb_target_info-structure"></a>Struttura CB \_ TARGET \_ INFO

Contiene informazioni sul computer di destinazione e sugli indirizzi IP in cui devono essere reindirizzate le connessioni in ingresso. Questa struttura viene usata con il [**metodo IConnectionBrokerClient::GetTargetInfo.**](iconnectionbrokerclient-gettargetinfo.md)

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

Rappresenta il nome di dominio completo del server di destinazione. Per uno scenario Desktop remoto virtualizzazione dei dati (RDV), questo membro è **NULL.** Per uno scenario Desktop remoto host sessione Desktop remoto, questo membro contiene il nome del server in cui viene reindirizzata la connessione in ingresso.

</dd> <dt>

**AddressCount**
</dt> <dd>

Numero di voci valide nella **matrice Addresses.**

</dd> <dt>

**Indirizzi**
</dt> <dd>

Matrice di stringhe che contengono gli indirizzi IP in cui vengono reindirizzate le connessioni in ingresso. Il numero di elementi validi in questa matrice viene specificato nel **membro AddressCount.**

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                  |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                        |
| Intestazione<br/>                   | <dl> <dt>Cbclient.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md)
</dt> </dl>

 

 





