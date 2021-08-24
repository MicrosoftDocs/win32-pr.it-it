---
title: CB_CONNECTION_INFO struttura (Cbclient.h)
description: Contiene informazioni su una richiesta di connessione in ingresso.
ms.assetid: BA908425-3B68-40AA-B1E3-153D6873EF2C
ms.tgt_platform: multiple
keywords:
- CB_CONNECTION_INFO struttura Servizi Desktop remoto
- PCB_CONNECTION_INFO puntatore alla struttura Servizi Desktop remoto
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
ms.openlocfilehash: 6fd433f668c178973a4e3690ea130d01d75fab79e739610f77ac00619b9e326c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575041"
---
# <a name="cb_connection_info-structure"></a>Struttura CB \_ CONNECTION \_ INFO

Contiene informazioni su una richiesta di connessione in ingresso. Questa struttura viene usata con il [**metodo IConnectionBrokerClient::GetTargetInfo.**](iconnectionbrokerclient-gettargetinfo.md)

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

Nome del dominio di cui **UserName** è membro.

</dd> <dt>

**InitialProgram**
</dt> <dd>

Percorso completo e nome file del programma iniziale avviato all'avvio della sessione. Impostare questo membro su una stringa vuota se non deve essere avviato alcun programma iniziale.

</dd> <dt>

**Risorsa**
</dt> <dd>

Valore dell'enumerazione [**CB \_ RESOURCE \_ TYPE**](cb-resource-type.md) che specifica il tipo di risorsa a cui si connette la connessione in ingresso. Se il **membro PluginName** è **NULL,** questo membro viene usato da Connessione Desktop remoto Broker per determinare quale plug-in richiamare per determinare il computer di destinazione.

</dd> <dt>

**PluginName**
</dt> <dd>

Nome del plug-in da richiamare per determinare il computer di destinazione. Se questo parametro è **NULL,** il **membro Resource** viene usato per determinare quale plug-in richiamare.

</dd> <dt>

**FarmName**
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
| Intestazione<br/>                   | <dl> <dt>Cbclient.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md)
</dt> </dl>

 

 





