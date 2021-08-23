---
description: I client NLA possono registrare le informazioni di configurazione di rete a livello di sistema, consentendo alle query future di restituire le informazioni di configurazione specificate indipendentemente dal fatto che la rete sia attiva.
ms.assetid: 7e92dd8f-d3a1-4e53-885c-ebc9626fd5dc
title: Registrazione di un'istanza del servizio con NLA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a623f28d30d02cd3a1266e173dbe28270f377a55c3f59f8ff095cf3d023a80eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641681"
---
# <a name="registering-a-service-instance-with-nla"></a>Registrazione di un'istanza del servizio con NLA

I client NLA possono registrare le informazioni di configurazione di rete a livello di sistema, consentendo alle query future di restituire le informazioni di configurazione specificate indipendentemente dal fatto che la rete sia attiva. Questa funzionalità consente ai client NLA di influire su un'esperienza utente coerente per le informazioni di rete tra più applicazioni.

## <a name="parameters"></a>Parametri

Per registrare un'istanza del servizio con il provider di servizi di riconoscimento del percorso di rete, usare la [**funzione WSASetService.**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea) Per registrare correttamente un'istanza del servizio, alcuni parametri della **funzione WSASetService** devono essere impostati con le informazioni appropriate, come illustrato in questa sezione. Per riferimento rapido, la **funzione WSASetService** ha la sintassi seguente:

``` syntax
INT WSASetService(
  LPWSAQUERYSET lpqsRegInfo,
  WSAESETSERVICEOP essOperation,
  DWORD dwControlFlags
);
```

Per il parametro *lpqsRegInfo,* specificare una struttura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) dal risultato di una query NLA SP o costruita rispettando i requisiti di una query NLA SP, come specificato in [Querying NLA](querying-nla-2.md).

Le operazioni supportate per *il parametro essOperation* sono le seguenti:

<dl> <dt>

<span id="RNRSERVICE_REGISTER"></span><span id="rnrservice_register"></span>REGISTRO RNRSERVICE \_
</dt> <dd>

La rete definita nella struttura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) fornita in *lpqsRegInfo* viene resa persistente per l'utente attivo archiviando l'istanza di rete nell'hive del Registro di sistema per l'utente corrente, che consente la rappresentazione.

</dd> <dt>

<span id="RNRSERVICE_DELETE"></span><span id="rnrservice_delete"></span>RNRSERVICE \_ DELETE
</dt> <dd>

Se la rete definita nella struttura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) fornita in *lpqsRegInfo* è persistente, verrà rimossa.

</dd> </dl>

L'operazione specificata nel *parametro essOperation* può essere modificata con le opzioni seguenti, che possono essere specificate con la logica OR binaria:

<dl> <dt>

<span id="NLA_FRIENDLY_NAME"></span><span id="nla_friendly_name"></span>NOME \_ DESCRITTIVO \_ NLA
</dt> <dd>

Se usato con RNRSERVICE REGISTER, il campo \_ *lpszComment* della rete definito in *lpqsRegInfo* viene verificato e archiviato in modo permanente. Se usato con RNRSERVICE DELETE e la rete definita ha un nome descrittivo, il nome descrittivo viene rimosso, ma la voce di rete \_ rimane intatta.

</dd> <dt>

<span id="NLA_ALLUSERS_NETWORK"></span><span id="nla_allusers_network"></span>NLA \_ ALLUSERS \_ NETWORK
</dt> <dd>

Se usata con RNRSERVICE REGISTER, la voce viene archiviata in modo permanente in HKEY LOCAL MACHINE, rendendola disponibile durante le query a tutti gli utenti \_ \_ nel computer \_ locale. Se usata con RNRSERVICE \_ DELETE, la rete specificata viene rimossa da HKEY \_ LOCAL \_ MACHINE. Se la rete specificata non è presente, viene restituito un errore. Per eliminare una rete dall'hive del Registro di sistema dell'utente corrente, questo flag non deve essere specificato. Questo flag è valido solo nel contesto di sicurezza di un amministratore di sistema locale.

</dd> </dl>

NLA supporta i codici di errore seguenti per le chiamate di funzione [**WSASetService:**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea)

| Errore             | Significato                                                                                                                                                                    |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WSANOTINITIALISED | Non è stata eseguita una chiamata riuscita [**alla funzione WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) per inizializzare NLA.                                                                  |
| WSAEACCESS        | NLA \_ ALLUSERS \_ NETWORK è stato specificato in *dwControlFlags* mentre non è nel contesto di sicurezza di un amministratore di sistema locale.                                                |
| WSAEALREADY       | La rete specificata è già archiviata in modo permanente nel modo richiesto e non è stato specificato alcun flag in *dwControlFlags* per indicare un aggiornamento alla voce esistente. |
| WSAEAFNOSUPPORT   | È stata specificata una famiglia di protocolli per la quale non è disponibile alcun supporto. In NLA sono supportate solo le famiglie di protocolli IP.                                                             |
| WSAEPFNOSUPPORT   | È stato specificato un protocollo per il quale non è disponibile alcun supporto. In NLA è supportato solo il protocollo IP.                                                                              |



 

 

 



