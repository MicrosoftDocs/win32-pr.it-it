---
title: Struttura RAS_PORT_1 (rassapi. h)
description: La \_ struttura della porta RAS \_ 1 contiene informazioni su una porta RAS.
ms.assetid: f226ef16-feb4-41e0-ba60-ddb2f0acd305
keywords:
- RAS struttura RAS_PORT_1
- RAS puntatore alla struttura PRAS_PORT_1
topic_type:
- apiref
api_name:
- RAS_PORT_1
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d73fe450e5ea5f8ceee48436dbbe05570d0d818a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301755"
---
# <a name="ras_port_1-structure"></a>\_Struttura porta RAS \_ 1

\[Questa versione della struttura **della \_ porta RAS \_ 1** non è supportata a partire da Windows Vista. Usare invece la [**\_ porta RAS \_ 1**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_1) più recente definita in mprapi. h.\]

La struttura della **\_ porta RAS \_ 1** contiene informazioni su una porta RAS.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _RAS_PORT_1 {
  RAS_PORT_0                rasport0;
  DWORD                     LineCondition;
  DWORD                     HardwareCondition;
  DWORD                     LineSpeed;
  WORD                      NumStatistics;
  WORD                      NumMediaParms;
  DWORD                     SizeMediaParms;
  RAS_PPP_PROJECTION_RESULT ProjResult;
} RAS_PORT_1, *PRAS_PORT_1;
```



## <a name="members"></a>Members

<dl> <dt>

**rasport0**
</dt> <dd>

Specifica una struttura di [**\_ porta RAS \_ 0**](ras-port-0-str.md) che contiene informazioni sulla porta, ad esempio il nome della porta, il nome dell'utente remoto connesso alla porta e così via.

</dd> <dt>

**LineCondition**
</dt> <dd>

Specifica lo stato della porta. Il membro può essere uno dei valori seguenti.



| Valore                                                                                                                                                                                            | Significato                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RAS_PORT_NON_OPERATIONAL"></span><span id="ras_port_non_operational"></span><dl> <dt>**\_porta RAS \_ non \_ operativa**</dt> </dl> | La porta non è operativa. Controllare se nel registro eventi sono presenti errori segnalati dal server.<br/>                                                                         |
| <span id="RAS_PORT_DISCONNECTED"></span><span id="ras_port_disconnected"></span><dl> <dt>**\_porta RAS \_ disconnessa**</dt> </dl>           | La porta è attualmente disconnessa.<br/>                                                                                                                         |
| <span id="RAS_PORT_CALLING_BACK"></span><span id="ras_port_calling_back"></span><dl> <dt>**\_chiamata della porta RAS \_ \_**</dt> </dl>          | Il server RAS sta richiamando il client RAS.<br/>                                                                                                              |
| <span id="RAS_PORT_LISTENING"></span><span id="ras_port_listening"></span><dl> <dt>**\_ascolto porta \_ RAS**</dt> </dl>                    | La porta è in attesa che un client chiami.<br/>                                                                                                                |
| <span id="RAS_PORT_AUTHENTICATING"></span><span id="ras_port_authenticating"></span><dl> <dt>**\_autenticazione porta \_ RAS**</dt> </dl>     | Il server è in fase di autenticazione del client remoto.<br/>                                                                                           |
| <span id="RAS_PORT_AUTHENTICATED"></span><span id="ras_port_authenticated"></span><dl> <dt>**\_porta RAS \_ autenticata**</dt> </dl>        | Il client remoto è ora autenticato.<br/>                                                                                                                     |
| <span id="RAS_PORT_INITIALIZING"></span><span id="ras_port_initializing"></span><dl> <dt>**\_ \_ inizializzazione porta RAS**</dt> </dl>           | Il dispositivo collegato alla porta verrà inizializzato. Lo stato della porta passerà alla porta RAS \_ in \_ ascolto quando l'inizializzazione è stata completata.<br/> |



 

</dd> <dt>

**HardwareCondition**
</dt> <dd>

Specifica uno dei valori seguenti per indicare lo stato del dispositivo collegato alla porta.



| Valore                                                                                                                                                                                                  | Significato                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="RAS_MODEM_OPERATIONAL"></span><span id="ras_modem_operational"></span><dl> <dt>**\_modem RAS \_ operativo**</dt> </dl>                 | Il modem collegato a questa porta è operativo ed è pronto per ricevere le chiamate del client.<br/> |
| <span id="RAS_MODEM_HARDWARE_FAILURE"></span><span id="ras_modem_hardware_failure"></span><dl> <dt>**\_ \_ errore hardware del modem RAS \_**</dt> </dl> | Il modem collegato a questa porta presenta un problema hardware.<br/>                              |



 

</dd> <dt>

**LineSpeed**
</dt> <dd>

Specifica la velocità, in bit al secondo, con cui il computer può comunicare con la porta.

</dd> <dt>

**NumStatistics**
</dt> <dd>

Questo membro non viene utilizzato. Le funzioni di amministrazione RAS, ad esempio la funzione [**RasAdminPortGetInfo**](rasadminportgetinfo.md) , utilizzano la struttura delle [**\_ \_ statistiche della porta RAS**](ras-port-statistics-str.md) per restituire le statistiche sulle porte.

</dd> <dt>

**NumMediaParms**
</dt> <dd>

Specifica il numero di parametri specifici del supporto per questa porta. Per i supporti seriali si tratta in genere del numero di valori visualizzati nel file di SERIAL.INI.

</dd> <dt>

**SizeMediaParms**
</dt> <dd>

Specifica la dimensione, in byte, del buffer necessario per tutti i parametri specifici del supporto. La funzione [**RasAdminPortGetInfo**](rasadminportgetinfo.md) restituisce un buffer che contiene una matrice di strutture di [**\_ parametri RAS**](ras-parameters-str.md) con i parametri e i valori del supporto per la porta.

</dd> <dt>

**ProjResult**
</dt> <dd>

Struttura [**di \_ \_ \_ Risultati della proiezione PPP RAS**](ras-ppp-projection-result-str.md) che specifica le informazioni sulla proiezione PPP per questa porta. Questa struttura fornisce informazioni per ogni protocollo negoziato quando un client RAS si connette a un server.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Rassapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica del servizio di accesso remoto (RAS)](about-remote-access-service.md)
</dt> <dt>

[Strutture di amministrazione del server RAS](ras-server-administration-structures.md)
</dt> <dt>

[**\_parametri RAS**](ras-parameters-str.md)
</dt> <dt>

[**\_Porta RAS \_ 0**](ras-port-0-str.md)
</dt> <dt>

[**\_statistiche porta \_ RAS**](ras-port-statistics-str.md)
</dt> <dt>

[**\_risultato della \_ proiezione \_ PPP RAS**](ras-ppp-projection-result-str.md)
</dt> <dt>

[**RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md)
</dt> <dt>

[**RasAdminConnectionHangupNotification**](rasadminconnectionhangupnotification.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

 





