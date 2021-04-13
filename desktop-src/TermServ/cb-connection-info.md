---
title: Struttura CB_CONNECTION_INFO (Cbclient. h)
description: Contiene informazioni su una richiesta di connessione in ingresso.
ms.assetid: BA908425-3B68-40AA-B1E3-153D6873EF2C
ms.tgt_platform: multiple
keywords:
- Struttura CB_CONNECTION_INFO Servizi Desktop remoto
- Puntatore alla struttura PCB_CONNECTION_INFO Servizi Desktop remoto
topic_type:
- apiref
api_name:
- CB_CONNECTION_INFO
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36370a4faa823f509d1f3356768add0ece9a6904
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400401"
---
# <a name="cb_connection_info-structure"></a>Struttura delle informazioni di \_ connessione CB \_

Contiene informazioni su una richiesta di connessione in ingresso. Questa struttura viene utilizzata con il metodo [**IConnectionBrokerClient:: GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) .

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  WCHAR            UserName[CB_USERNAME_LENGTH];
  WCHAR            Domain[CB_DOMAINNAME_LENGTH];
  WCHAR            InitialProgram[CB_INITAPP_LENGTH];
  CB_RESOURCE_TYPE Resource;
  WCHAR            PluginName[CB_PLUGINNAME_LENGTH];
  WCHAR            FarmName[CB_FARMNAME_LENGTH];
  DWORD            dwVendorInfoLength;
  PBYTE            pVendorSpecificInfo;
} CB_CONNECTION_INFO, *PCB_CONNECTION_INFO;
```



## <a name="members"></a>Members

<dl> <dt>

**UserName**
</dt> <dd>

Nome dell'utente che richiede una sessione.

</dd> <dt>

**Dominio**
</dt> <dd>

Nome del dominio di cui è membro il nome **utente** .

</dd> <dt>

**InitialProgram**
</dt> <dd>

Percorso completo e nome file del programma iniziale avviato all'avvio della sessione. Impostare questo membro su una stringa vuota se non è necessario avviare alcun programma iniziale.

</dd> <dt>

**Risorsa**
</dt> <dd>

Valore dell'enumerazione del [**\_ \_ tipo di risorsa CB**](cb-resource-type.md) che specifica il tipo di risorsa a cui si connette la connessione in ingresso. Se il membro **pluginName** è **null**, questo membro viene usato da connessione Desktop remoto broker per determinare il plug-in da richiamare per determinare il computer di destinazione.

</dd> <dt>

**PluginName**
</dt> <dd>

Nome del plug-in da richiamare per determinare il computer di destinazione. Se questo parametro è **null**, viene usato il membro della **risorsa** per determinare il plug-in da richiamare.

</dd> <dt>

**Farmname**
</dt> <dd>

Nome della farm che contiene i computer, uno dei quali sarà il computer di destinazione in cui verrà reindirizzata la connessione.

</dd> <dt>

**dwVendorInfoLength**
</dt> <dd>

Questo membro è riservato per usi futuri.

</dd> <dt>

**pVendorSpecificInfo**
</dt> <dd>

Questo membro è riservato per usi futuri.

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

 

 





