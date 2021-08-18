---
title: RAS_PORT_1 struttura (Rassapi.h)
description: La struttura \_ RAS PORT \_ 1 contiene informazioni su una porta RAS.
ms.assetid: f226ef16-feb4-41e0-ba60-ddb2f0acd305
keywords:
- RAS_PORT_1 struttura RAS
- PRAS_PORT_1 ras del puntatore della struttura
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
ms.openlocfilehash: 5c73677b10743434bb9548c8d6add95100c4cf017d25bb44d7436e2f68b9ca4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673111"
---
# <a name="ras_port_1-structure"></a>Struttura \_ RAS PORT \_ 1

\[Questa versione della **struttura RAS \_ PORT \_ 1** non è supportata a Windows Vista. Usare invece la porta [**\_ RAS \_ 1 più**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_1) recente definita in mprapi.h.\]

La **struttura RAS PORT \_ \_ 1** contiene informazioni su una porta RAS.

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

Specifica una [**struttura RAS PORT \_ \_ 0**](ras-port-0-str.md) che contiene informazioni sulla porta, ad esempio il nome della porta, il nome dell'utente remoto connesso alla porta e così via.

</dd> <dt>

**LineCondition**
</dt> <dd>

Specifica lo stato della porta. Questo membro può essere uno dei valori seguenti.



| Valore                                                                                                                                                                                            | Significato                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RAS_PORT_NON_OPERATIONAL"></span><span id="ras_port_non_operational"></span><dl> <dt>**PORTA RAS \_ \_ NON \_ OPERATIVA**</dt> </dl> | La porta non è operativa. Controllare nel registro eventi gli errori segnalati dal server.<br/>                                                                         |
| <span id="RAS_PORT_DISCONNECTED"></span><span id="ras_port_disconnected"></span><dl> <dt>**PORTA RAS \_ \_ DISCONNESSA**</dt> </dl>           | La porta è attualmente disconnessa.<br/>                                                                                                                         |
| <span id="RAS_PORT_CALLING_BACK"></span><span id="ras_port_calling_back"></span><dl> <dt>**CHIAMATA DELLA PORTA RAS \_ \_ \_**</dt> </dl>          | Il server RAS sta richiamando il client RAS.<br/>                                                                                                              |
| <span id="RAS_PORT_LISTENING"></span><span id="ras_port_listening"></span><dl> <dt>**PORTA RAS \_ IN \_ ASCOLTO**</dt> </dl>                    | La porta è in attesa della chiamata da parte di un client.<br/>                                                                                                                |
| <span id="RAS_PORT_AUTHENTICATING"></span><span id="ras_port_authenticating"></span><dl> <dt>**AUTENTICAZIONE \_ DELLA PORTA RAS \_**</dt> </dl>     | Il server è in corso di autenticazione del client remoto.<br/>                                                                                           |
| <span id="RAS_PORT_AUTHENTICATED"></span><span id="ras_port_authenticated"></span><dl> <dt>**PORTA RAS \_ \_ AUTENTICATA**</dt> </dl>        | Il client remoto è ora autenticato.<br/>                                                                                                                     |
| <span id="RAS_PORT_INITIALIZING"></span><span id="ras_port_initializing"></span><dl> <dt>**\_INIZIALIZZAZIONE DELLA PORTA RAS \_**</dt> </dl>           | È in corso l'inizializzazione del dispositivo collegato alla porta. Lo stato della porta verrà modificato in RAS \_ PORT LISTENING al termine \_ dell'inizializzazione.<br/> |



 

</dd> <dt>

**HardwareCondition**
</dt> <dd>

Specifica uno dei valori seguenti per indicare lo stato del dispositivo collegato alla porta.



| Valore                                                                                                                                                                                                  | Significato                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="RAS_MODEM_OPERATIONAL"></span><span id="ras_modem_operational"></span><dl> <dt>**RAS \_ MODEM \_ OPERATIVO**</dt> </dl>                 | Il modem collegato a questa porta è operativo ed è pronto per ricevere chiamate client.<br/> |
| <span id="RAS_MODEM_HARDWARE_FAILURE"></span><span id="ras_modem_hardware_failure"></span><dl> <dt>**ERRORE \_ \_ HARDWARE MODEM \_ RAS**</dt> </dl> | Il modem collegato a questa porta presenta un problema hardware.<br/>                              |



 

</dd> <dt>

**LineSpeed**
</dt> <dd>

Specifica la velocità, in bit al secondo, con cui il computer può comunicare con la porta.

</dd> <dt>

**NumStatistics**
</dt> <dd>

Questo membro non viene utilizzato. Le funzioni di amministrazione RAS, ad esempio [**la funzione RasAdminPortGetInfo,**](rasadminportgetinfo.md) usano la [**struttura RAS PORT \_ \_ STATISTICS**](ras-port-statistics-str.md) per restituire le statistiche sulle porte.

</dd> <dt>

**NumMediaParms**
</dt> <dd>

Specifica il numero di parametri specifici del supporto per questa porta. Per i supporti seriali si tratta in genere del numero di valori visualizzati nel file SERIAL.INI.

</dd> <dt>

**SizeMediaParms**
</dt> <dd>

Specifica la dimensione, in byte, del buffer necessario per tutti i parametri specifici dei supporti. La [**funzione RasAdminPortGetInfo**](rasadminportgetinfo.md) restituisce un buffer che contiene una matrice di strutture [**\_ PARAMETERS RAS**](ras-parameters-str.md) con i parametri e i valori dei supporti per la porta.

</dd> <dt>

**ProjResult**
</dt> <dd>

Struttura [**RAS \_ PPP PROJECTION \_ \_ RESULT**](ras-ppp-projection-result-str.md) che specifica le informazioni di proiezione PPP per questa porta. Questa struttura fornisce informazioni per ogni protocollo negoziato quando un client RAS si connette a un server.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Rassapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica del servizio di accesso remoto (RAS)](about-remote-access-service.md)
</dt> <dt>

[Strutture di amministrazione del server RAS](ras-server-administration-structures.md)
</dt> <dt>

[**PARAMETRI \_ RAS**](ras-parameters-str.md)
</dt> <dt>

[**PORTA \_ RAS \_ 0**](ras-port-0-str.md)
</dt> <dt>

[**STATISTICHE \_ PORTA \_ RAS**](ras-port-statistics-str.md)
</dt> <dt>

[**RISULTATO \_ DELLA \_ PROIEZIONE RAS PPP \_**](ras-ppp-projection-result-str.md)
</dt> <dt>

[**RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md)
</dt> <dt>

[**RasAdminConnectionHangupNotification**](rasadminconnectionhangupnotification.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

 





