---
description: I client NLA possono registrare le informazioni di configurazione di rete a livello di sistema, consentendo alle query future di restituire le informazioni di configurazione specificate indipendentemente dal fatto che la rete sia attiva.
ms.assetid: 7e92dd8f-d3a1-4e53-885c-ebc9626fd5dc
title: Registrazione di un'istanza del servizio con NLA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae2e73e638e4bf0152c2c6c5a4f5ab87dda7312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310454"
---
# <a name="registering-a-service-instance-with-nla"></a>Registrazione di un'istanza del servizio con NLA

I client NLA possono registrare le informazioni di configurazione di rete a livello di sistema, consentendo alle query future di restituire le informazioni di configurazione specificate indipendentemente dal fatto che la rete sia attiva. Questa funzionalità consente ai client NLA di influenzare un'esperienza utente di informazioni di rete coerente in più applicazioni.

## <a name="parameters"></a>Parametri

Per registrare un'istanza del servizio con il provider del servizio di riconoscimento del percorso di rete, usare la funzione [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea) . Per registrare correttamente un'istanza del servizio, è necessario impostare determinati parametri della funzione **WSASetService** con le informazioni appropriate, come illustrato in questa sezione. Per riferimento rapido, la funzione **WSASetService** presenta la sintassi seguente:

``` syntax
INT WSASetService(
  LPWSAQUERYSET lpqsRegInfo,
  WSAESETSERVICEOP essOperation,
  DWORD dwControlFlags
);
```

Per il parametro *lpqsRegInfo* , fornire una struttura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) da un risultato della query NLA SP o costruita rispettando i requisiti di una query NLA SP, come specificato in [query NLA](querying-nla-2.md).

Di seguito sono riportate le operazioni supportate per il parametro *essOperation* :

<dl> <dt>

<span id="RNRSERVICE_REGISTER"></span><span id="rnrservice_register"></span>\_Registro RNRSERVICE
</dt> <dd>

La rete definita nella struttura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) fornita in *lpqsRegInfo* viene resa persistente per l'utente attivo archiviando l'istanza di rete nell'hive del registro di sistema per l'utente corrente, che consente la rappresentazione.

</dd> <dt>

<span id="RNRSERVICE_DELETE"></span><span id="rnrservice_delete"></span>eliminazione di RNRSERVICE \_
</dt> <dd>

Se la rete definita nella struttura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) fornita in *lpqsRegInfo* è persistente, verrà rimossa.

</dd> </dl>

L'operazione specificata nel parametro *essOperation* può essere modificata dalle opzioni seguenti, che è possibile specificare con la logica o binario:

<dl> <dt>

<span id="NLA_FRIENDLY_NAME"></span><span id="nla_friendly_name"></span>\_nome descrittivo NLA \_
</dt> <dd>

Quando viene usato con \_ il registro RNRSERVICE, viene verificata la validità del campo *lpszComment* della rete definito in *lpqsRegInfo* , che viene archiviato in modo permanente. Se usato con RNRSERVICE \_ Delete e la rete definita ha un nome descrittivo, il nome descrittivo viene rimosso, ma la voce di rete rimane intatta.

</dd> <dt>

<span id="NLA_ALLUSERS_NETWORK"></span><span id="nla_allusers_network"></span>\_rete ALLUSERS \_ NLA
</dt> <dd>

Quando viene usato con \_ il registro RNRSERVICE, la voce viene archiviata in modo permanente in HKEY \_ \_ computer locale, rendendola disponibile durante le query a tutti gli utenti nel computer locale. Se usato con RNRSERVICE \_ Delete, la rete specificata viene rimossa dal \_ computer locale HKEY \_ . Se la rete specificata non è presente, viene restituito un errore. Per eliminare una rete dall'hive del registro di sistema dell'utente corrente, questo flag non deve essere specificato. Questo flag è valido solo nel contesto di sicurezza di un amministratore di sistema locale.

</dd> </dl>

NLA supporta i codici di errore seguenti per le chiamate di funzione [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea) :

| Errore             | Significato                                                                                                                                                                    |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WSANOTINITIALISED | Una chiamata riuscita alla funzione [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) per inizializzare NLA non è stata eseguita.                                                                  |
| WSAEACCESS        | \_ \_ La rete ALLUSERS NLA è stata specificata in *dwControlFlags* mentre non è presente nel contesto di sicurezza di un amministratore di sistema locale.                                                |
| WSAEALREADY       | La rete specificata è già archiviata in modo permanente nella modalità richiesta e non è stato specificato alcun flag in *dwControlFlags* per indicare un aggiornamento alla voce esistente. |
| WSAEAFNOSUPPORT   | È stata specificata una famiglia di protocolli per la quale non è disponibile alcun supporto. In NLA sono supportate solo le famiglie di protocolli IP.                                                             |
| WSAEPFNOSUPPORT   | È stato specificato un protocollo per il quale non è disponibile alcun supporto. In NLA è supportato solo il protocollo IP.                                                                              |



 

 

 



