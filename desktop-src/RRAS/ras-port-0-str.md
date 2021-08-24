---
title: RAS_PORT_0 struttura (Rassapi.h)
description: La struttura \_ RAS PORT \_ 0 contiene informazioni che descrivono una porta RAS.
ms.assetid: 750fc705-0770-427b-b7d6-7876b8b9118a
keywords:
- RAS_PORT_0 ras struttura
- PRAS_PORT_0 del puntatore della struttura RAS
topic_type:
- apiref
api_name:
- RAS_PORT_0
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67891ccd65aaa56fc41dd077ae46bd4bf61f816cdc02afeb65964886cbaf9562
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673131"
---
# <a name="ras_port_0-structure"></a>Struttura \_ RAS PORT \_ 0

\[Questa versione della **struttura \_ RAS PORT \_ 0** non è supportata a Windows Vista. Usare invece la porta [**\_ RAS \_ 0 più**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) recente definita in mprapi.h.\]

La **struttura RAS PORT \_ \_ 0** contiene informazioni che descrivono una porta RAS.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _RAS_PORT_0 {
  WCHAR wszPortName[RASSAPI_MAX_PORT_NAME];
  WCHAR wszDeviceType[RASSAPI_MAX_DEVICETYPE_NAME];
  WCHAR wszDeviceName[RASSAPI_MAX_DEVICE_NAME];
  WCHAR wszMediaName[RASSAPI_MAX_MEDIA_NAME];
  DWORD reserved;
  DWORD Flags;
  WCHAR wszUserName[UNLEN + 1];
  WCHAR wszComputer[NETBIOS_NAME_LEN];
  DWORD dwStartSessionTime;
  WCHAR wszLogonDomain[DNLEN + 1];
  BOOL  fAdvancedServer;
} RAS_PORT_0, *PRAS_PORT_0;
```



## <a name="members"></a>Members

<dl> <dt>

**wszPortName**
</dt> <dd>

Stringa Unicode con terminazione Null che specifica il nome della porta, ad esempio "COM1".

</dd> <dt>

**wszDeviceType**
</dt> <dd>

Stringa Unicode con terminazione Null che specifica il tipo di dispositivo in cui è stata stabilita la connessione, ad esempio Modem o ISDN. L'elenco dei tipi di dispositivi che possono essere specificati in questo membro include tutti i tipi di dispositivi installati nel server, inclusi i dispositivi di terze parti.

</dd> <dt>

**wszDeviceName**
</dt> <dd>

Stringa Unicode con terminazione Null che specifica il nome del dispositivo in cui è stata stabilita la connessione, ad esempio "Bluetoothes 9600" o "PCIMACISDN1".

</dd> <dt>

**wszMediaName**
</dt> <dd>

Specifica una stringa Unicode con terminazione Null che specifica il nome del supporto utilizzato per la connessione, ad esempio *rasser* o *rastapi.*

</dd> <dt>

**Riservati**
</dt> <dd>

Riservato.

</dd> <dt>

**Flag**
</dt> <dd>

Specifica un set di flag di bit che specificano la natura della connessione effettuata su questa porta. Questo membro può essere una combinazione dei flag seguenti.



| Valore                                                                                                                                                                        | Significato                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GATEWAY_ACTIVE"></span><span id="gateway_active"></span><dl> <dt>**GATEWAY \_ ATTIVO**</dt> </dl>             | Se questo flag è impostato, il gateway NetBIOS è attivo nel server.<br/>                                                                                                                                                                                                                                                                                                               |
| <span id="MESSENGER_PRESENT"></span><span id="messenger_present"></span><dl> <dt>**MESSENGER \_ PRESENT**</dt> </dl>    | Se questo flag è impostato, il servizio Messenger è in esecuzione nel client remoto.<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="PORT_MULTILINKED"></span><span id="port_multilinked"></span><dl> <dt>**PORTA \_ MULTILINKED**</dt> </dl>       | Se questo flag è impostato, la porta è multilink con altre porte. Usare queste informazioni per visualizzare lo stato della connessione come porta multilink. <br/> Per una porta multilink, la struttura [**RAS \_ PORT \_ STATISTICS**](ras-port-statistics-str.md) contiene due set di statistiche: uno solo per la porta e l'altro per le porte combinate nella connessione multilink.<br/> |
| <span id="PPP_CLIENT"></span><span id="ppp_client"></span><dl> <dt>**PPP \_ CLIENT**</dt> </dl>                         | Se questo flag è impostato, il client remoto si è connesso tramite PPP. Se questo flag non è impostato, il client remoto si è connesso tramite il protocollo AMB.<br/>                                                                                                                                                                                                                                        |
| <span id="REMOTE_LISTEN"></span><span id="remote_listen"></span><dl> <dt>**REMOTE \_ LISTEN**</dt> </dl>                | Se questo flag è impostato, il parametro RemoteListen del gateway NetBIOS viene impostato su 1 nel server.<br/>                                                                                                                                                                                                                                                                               |
| <span id="USER_AUTHENTICATED"></span><span id="user_authenticated"></span><dl> <dt>**UTENTE \_ AUTENTICATO**</dt> </dl> | Se questo flag è impostato, un client remoto è connesso al server e l'utente è stato autenticato. Selezionare questo flag per assicurarsi che un client sia effettivamente connesso a una porta.<br/>                                                                                                                                                                                                   |



 

Se i flag MESSENGER PRESENT, GATEWAY ACTIVE e REMOTE LISTEN sono impostati, usare il servizio Messenger per inviare un messaggio \_ \_ \_ amministrativo al client remoto. Se MESSENGER PRESENT e REMOTE LISTEN sono impostati, ma GATEWAY ACTIVE non lo è, inviare messaggi al client solo dal server RAS a cui il \_ \_ client è \_ connesso.

</dd> <dt>

**wszUserName**
</dt> <dd>

Stringa Unicode con terminazione Null che specifica il nome dell'utente remoto connesso a questa porta.

</dd> <dt>

**wszComputer**
</dt> <dd>

Stringa Unicode con terminazione Null che specifica il nome del computer client remoto.

</dd> <dt>

**dwStartSessionTime**
</dt> <dd>

Specifica il tempo, in secondi dal 1 gennaio 1970, in cui il client si è connesso al server RAS su questa porta. Usare le funzioni dell'ora solare per formattare questo valore per la visualizzazione.

</dd> <dt>

**wszLogonDomain**
</dt> <dd>

Specifica una stringa Unicode con terminazione Null che specifica il nome del dominio in cui è stato autenticato l'utente remoto. Questa stringa è solo il nome di dominio, senza prefisso \\ \\ " ".

</dd> <dt>

**fAdvancedServer**
</dt> <dd>

Specifica un flag diverso da zero se il server RAS associato a questa porta è un server avanzato, ad esempio Windows 2000 Advanced Server. Utilizzare queste informazioni per determinare il nome del server con il database dell'account utente. Se il server RAS è un server avanzato, ottenere il nome del server dell'account utente concatenando il prefisso " " al nome restituito nel \\ \\ **membro wszLogonDomain.** Ciò è dovuto al fatto che per un server avanzato il nome di dominio di accesso locale corrisponde al nome del server. Se il server RAS è una workstation, usare la [**funzione RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) per ottenere il nome del server dell'account utente.

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

[**PORTA \_ RAS \_ 1**](ras-port-1-str.md)
</dt> <dt>

[**STATISTICHE \_ PORTA \_ RAS**](ras-port-statistics-str.md)
</dt> <dt>

[**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md)
</dt> <dt>

[**RasAdminPortEnum**](rasadminportenum.md)
</dt> </dl>

 

 





