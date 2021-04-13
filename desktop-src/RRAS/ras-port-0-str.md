---
title: Struttura RAS_PORT_0 (rassapi. h)
description: La \_ struttura della porta \_ 0 RAS contiene informazioni che descrivono una porta RAS.
ms.assetid: 750fc705-0770-427b-b7d6-7876b8b9118a
keywords:
- RAS struttura RAS_PORT_0
- RAS puntatore alla struttura PRAS_PORT_0
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
ms.openlocfilehash: 80d66725415d86aea44138f23fb3748e3187820f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517883"
---
# <a name="ras_port_0-structure"></a>\_Struttura porta RAS \_ 0

\[Questa versione della struttura **della \_ porta RAS \_ 0** non è supportata a partire da Windows Vista. Usare invece la [**\_ porta RAS \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) più recente definita in mprapi. h.\]

La struttura della **\_ porta \_ 0 RAS** contiene informazioni che descrivono una porta RAS.

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

Stringa Unicode con terminazione null che specifica il nome della porta, ad esempio "COM1".

</dd> <dt>

**wszDeviceType**
</dt> <dd>

Stringa Unicode con terminazione null che specifica il tipo del dispositivo in cui è stata effettuata la connessione, ad esempio modem o ISDN. L'elenco dei tipi di dispositivo che potrebbero essere specificati in questo membro include tutti i tipi di dispositivo installati nel server, inclusi i dispositivi di terze parti.

</dd> <dt>

**wszDeviceName**
</dt> <dd>

Stringa Unicode con terminazione null che specifica il nome del dispositivo in cui è stata effettuata la connessione, ad esempio "Hayes 9600" o "PCIMACISDN1".

</dd> <dt>

**wszMediaName**
</dt> <dd>

Specifica una stringa Unicode con terminazione null che specifica il nome del supporto usato per la connessione, ad esempio *rasser* o *RASTAPI*.

</dd> <dt>

**riservati**
</dt> <dd>

Riservato.

</dd> <dt>

**Flag**
</dt> <dd>

Specifica un set di flag di bit che specificano la natura della connessione effettuata su questa porta. Questo membro può essere una combinazione dei flag seguenti.



| Valore                                                                                                                                                                        | Significato                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GATEWAY_ACTIVE"></span><span id="gateway_active"></span><dl> <dt>**GATEWAY \_ attivo**</dt> </dl>             | Se questo flag è impostato, il gateway NetBIOS è attivo sul server.<br/>                                                                                                                                                                                                                                                                                                               |
| <span id="MESSENGER_PRESENT"></span><span id="messenger_present"></span><dl> <dt>**MESSENGER \_ presente**</dt> </dl>    | Se questo flag è impostato, il servizio Messenger viene eseguito sul client remoto.<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="PORT_MULTILINKED"></span><span id="port_multilinked"></span><dl> <dt>**PORTA \_ MULTIlinked**</dt> </dl>       | Se questo flag è impostato, la porta viene collegata a più porte. Utilizzare queste informazioni per visualizzare lo stato di connessione come porta con collegamento multiplo. <br/> Per una porta con collegamento multiplo, la struttura delle [**\_ \_ statistiche della porta RAS**](ras-port-statistics-str.md) contiene due set di statistiche: uno solo per la porta e un altro per le porte combinate nella connessione multicollegamento.<br/> |
| <span id="PPP_CLIENT"></span><span id="ppp_client"></span><dl> <dt>**\_client PPP**</dt> </dl>                         | Se questo flag è impostato, il client remoto si connette utilizzando PPP. Se questo flag non è impostato, il client remoto si è connesso usando il protocollo AMB.<br/>                                                                                                                                                                                                                                        |
| <span id="REMOTE_LISTEN"></span><span id="remote_listen"></span><dl> <dt>**\_ascolto remoto**</dt> </dl>                | Se questo flag è impostato, il parametro RemoteListen del gateway NetBIOS viene impostato su 1 sul server.<br/>                                                                                                                                                                                                                                                                               |
| <span id="USER_AUTHENTICATED"></span><span id="user_authenticated"></span><dl> <dt>**UTENTE \_ autenticato**</dt> </dl> | Se questo flag è impostato, un client remoto è connesso al server e l'utente è stato autenticato. Selezionare questo flag per verificare che un client sia effettivamente connesso a una porta.<br/>                                                                                                                                                                                                   |



 

Se il MESSENGER \_ è presente, i \_ flag Active gateway e \_ ascolto remoto sono impostati, usare il servizio Messenger per inviare un messaggio amministrativo al client remoto. Se \_ sono impostati Messenger e \_ l'ascolto remoto, ma \_ il gateway attivo non lo è, inviare i messaggi al client solo dal server RAS a cui è connesso il client.

</dd> <dt>

**wszUserName**
</dt> <dd>

Stringa Unicode con terminazione null che specifica il nome dell'utente remoto connesso a questa porta.

</dd> <dt>

**wszComputer**
</dt> <dd>

Stringa Unicode con terminazione null che specifica il nome del computer client remoto.

</dd> <dt>

**dwStartSessionTime**
</dt> <dd>

Specifica il tempo, in secondi, dal 1 gennaio 1970, che il client si è connesso al server RAS su questa porta. Usare le funzioni temporali standard per formattare questo valore per la visualizzazione.

</dd> <dt>

**wszLogonDomain**
</dt> <dd>

Specifica una stringa Unicode con terminazione null che specifica il nome del dominio in cui è stato autenticato l'utente remoto. Questa stringa è solo il nome di dominio, senza \\ \\ prefisso "".

</dd> <dt>

**fAdvancedServer**
</dt> <dd>

Specifica un flag che è diverso da zero se il server RAS associato a questa porta è un server avanzato, ad esempio Windows 2000 Advanced Server. Utilizzare queste informazioni per determinare il nome del server in cui è presente il database degli account utente. Se il server RAS è un server avanzato, ottenere il nome del server dell'account utente concatenando il prefisso " \\ \\ " con il nome restituito nel membro **wszLogonDomain** . Questo è dovuto al fatto che per un server avanzato il nome di dominio di accesso locale corrisponde al nome del server. Se il server RAS è una workstation, utilizzare la funzione [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) per ottenere il nome del server dell'account utente.

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

[**\_Porta RAS \_ 1**](ras-port-1-str.md)
</dt> <dt>

[**\_statistiche porta \_ RAS**](ras-port-statistics-str.md)
</dt> <dt>

[**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md)
</dt> <dt>

[**RasAdminPortEnum**](rasadminportenum.md)
</dt> </dl>

 

 





