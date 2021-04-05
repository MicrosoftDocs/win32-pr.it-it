---
title: UrlPrefix Strings (Stringhe UrlPrefix)
description: Nell'API del server HTTP, un UrlPrefix è una stringa Unicode a caratteri wide (UTF-16) con una forma canonica che specifica una sezione dello spazio dei nomi URL.
ms.assetid: 4f317bf6-ee6a-47a8-a531-78534217109d
keywords:
- API server HTTP UrlPrefix Strings
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bddc484f26bc1b3de5d20196dadec9201d3ea272
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "103734738"
---
# <a name="urlprefix-strings"></a>UrlPrefix Strings (Stringhe UrlPrefix)

Nell'API del server HTTP, un *URLPrefix* è una stringa Unicode a caratteri wide (UTF-16) con una forma canonica che specifica una sezione dello spazio dei nomi URL. Viene usato per riservare una sezione dello spazio dei nomi URL per un account utente o per registrare una sezione dello spazio dei nomi URL per un processo.

## <a name="urlprefix-format"></a>Formato UrlPrefix

Un UrlPrefix ha la sintassi seguente:

"Scheme://host: Port/relativeURI"

Gli elementi schema, host e Port di un UrlPrefix devono essere presenti e non vuoti e devono rispettare le regole seguenti:

<dl> <dt>

<span id="scheme"></span><span id="SCHEME"></span>Schema
</dt> <dd>

Deve essere http o HTTPS, tutto in minuscolo.

</dd> <dt>

<span id="host"></span><span id="HOST"></span>host
</dt> <dd>

Deve essere un nome di dominio completo, una stringa letterale IPv4 o IPv6 o un carattere jolly. A differenza dello schema, che deve essere minuscolo, la parte host non fa distinzione tra maiuscole e minuscole. A seconda di come viene specificata la relativa porzione host, un UrlPrefix rientra in una delle quattro categorie di routing seguenti, descritte in modo più dettagliato di seguito:

<dl> <dd>Carattere jolly sicuro</dd> <dd>Esplicita</dd> <dd>Carattere jolly vulnerabile associato a IP</dd> <dd>Carattere jolly vulnerabile</dd> </dl> </dd> <dt>

<span id="port"></span><span id="PORT"></span>porta
</dt> <dd>

Stringa numerica decimale che non inizia con zero e che rappresenta un numero di porta TCP valido (da 1 a 65.535). Questo valore non può essere un carattere jolly.

</dd> <dt>

<span id="relativeURI"></span><span id="relativeuri"></span><span id="RELATIVEURI"></span>relativeURI
</dt> <dd>

L'elemento relativeURI è facoltativo, ma se è presente deve essere sempre seguito da un carattere barra ("/"). Si tratta di una stringa di prefisso che indica un sottoalbero nello spazio dei nomi del computer specificato rispetto ai valori di schema, host e porta. A differenza dello schema, che deve essere minuscolo, la parte relativeURI non fa distinzione tra maiuscole e minuscole.

</dd> </dl>

Esempi di prefissi URL correttamente formati sono:

-   `https://www.adatum.com:80/vroot/`
-   `https://adatum.com:443/secure/database/`
-   `https://+:80/vroot/`

## <a name="host-specifier-categories"></a>Categorie di Host-Specifier

Per flessibilità e semplicità d'uso, l'API server HTTP supporta quattro diversi modi per specificare gli host. Le quattro categorie host-specifier sono elencate di seguito in ordine di precedenza:

<dl> <dt>

<span id="Strong_wildcard__Plus_Sign_"></span><span id="strong_wildcard__plus_sign_"></span><span id="STRONG_WILDCARD__PLUS_SIGN_"></span>Carattere jolly forte (segno più)
</dt> <dd>

Quando l'elemento host di un UrlPrefix è costituito da un singolo segno più (+), il UrlPrefix corrisponde a tutti i nomi host possibili nel contesto dello schema, della porta e degli elementi relativeURI e rientra nella categoria con caratteri jolly forti.

Un carattere jolly complesso è utile quando un'applicazione deve gestire le richieste destinate a uno o più relativeURIs, indipendentemente dal modo in cui tali richieste vengono ricevute nel computer o nel sito specificato nelle rispettive intestazioni host. In questa situazione, l'utilizzo di un carattere jolly complesso evita la necessità di specificare un elenco completo di indirizzi IP e/o host.

</dd> <dt>

<span id="Explicit"></span><span id="explicit"></span><span id="EXPLICIT"></span>Esplicita
</dt> <dd>

Un nome host esplicito, ad esempio un nome di dominio completo nell'elemento host, inserisce un UrlPrefix nella categoria Explicit. Questo tipo di elemento host viene associato direttamente alle intestazioni host delle richieste in ingresso.

Le specifiche host esplicite sono utili per le applicazioni multisito, ad esempio i server Web che forniscono contenuti diversi a seconda del sito a cui è stata indirizzata la richiesta.

</dd> <dt>

<span id="IP-bound_weak_wildcard"></span><span id="ip-bound_weak_wildcard"></span><span id="IP-BOUND_WEAK_WILDCARD"></span>Carattere jolly vulnerabile associato a IP
</dt> <dd>

Quando un indirizzo IP viene visualizzato come elemento host, il UrlPrefix rientra nella categoria con carattere jolly vulnerabile associato a IP. Questo tipo di UrlPrefix corrisponde a qualsiasi nome host per l'interfaccia IP specificata con lo schema, la porta e il relativeURI specificati e che non è già stato trovato come corrispondenza con un carattere jolly sicuro o un UrlPrefix esplicito. L'indirizzo IP accetta uno dei due formati seguenti nell'elemento host:

<dl> <dt>

<span id="IPv4_Literal_String"></span><span id="ipv4_literal_string"></span><span id="IPV4_LITERAL_STRING"></span>Stringa letterale IPv4
</dt> <dd>

Un valore letterale IPv4 è costituito da quattro numeri decimali punteggiati, ognuno nell'intervallo 0-255, ad esempio 192.168.0.0.

</dd> <dt>

<span id="IPv6_Literal_String"></span><span id="ipv6_literal_string"></span><span id="IPV6_LITERAL_STRING"></span>Stringa letterale IPv6
</dt> <dd>

Una stringa letterale IPv6 è racchiusa tra parentesi quadre e contiene numeri esadecimali separati da due punti; ad esempio::: \[ 1 \] o \[ 3FFE: ffff:: 6ECB: 0101 \] .

</dd> </dl>

Gli identificatori host con caratteri jolly vulnerabili con binding IP sono destinati ad applicazioni che variano il contenuto che viene utilizzato in base alla route eseguita dalle richieste in ingresso. Non fare affidamento sugli identificatori host con caratteri jolly vulnerabili con binding IP per applicare la sicurezza.

</dd> <dt>

<span id="Weak_wildcard__asterisk_"></span><span id="weak_wildcard__asterisk_"></span><span id="WEAK_WILDCARD__ASTERISK_"></span>Carattere jolly debole (asterisco)
</dt> <dd>

Quando un asterisco ( \* ) viene visualizzato come elemento host, il URLPrefix rientra nella categoria con carattere jolly debole. Questo tipo di UrlPrefix corrisponde a qualsiasi nome host associato allo schema, alla porta e al relativeURI specificati che non sono già stati confrontati da un carattere jolly sicuro, esplicito o con carattere jolly debole associato a IP.

Questa specifica host può essere usata come catch-all predefinito in alcune circostanze oppure può essere usata per specificare una sezione di grandi dimensioni dello spazio dei nomi URL senza dover usare molti prefissi URL.

</dd> </dl>

## <a name="urlprefix-conflict-detection-during-reservation-and-registration"></a>Rilevamento dei conflitti di UrlPrefix durante la prenotazione e la registrazione

Ai fini della prenotazione e della registrazione, le quattro categorie diverse di UrlPrefix vengono gestite separatamente, senza riferimento l'una all'altra. È possibile registrare prefissi URL in conflitto, purché si trovino in categorie diverse. Solo all'interno della stessa categoria si verifica un conflitto perché un tentativo di prenotazione non riesce.

Ad esempio, è possibile riservare sia il UrlPrefix esplicito `https://www.adatum.com:80/vroot/` che il carattere jolly URLPrefix `https://+:80/vroot/` in conflitto, perché appartengono a categorie diverse. Tuttavia, un tentativo successivo di riservare https://+:80/vroot/ a un utente diverso avrà esito negativo perché potrebbe essere in conflitto con una prenotazione esistente nella relativa categoria.

## <a name="routing-behavior"></a>Comportamento del routing

Quando si esegue il routing di una richiesta HTTP in ingresso, l'API del server HTTP inizia con la categoria con carattere jolly sicuro e confronta l'URL in ingresso con prefissi URL registrati e riservati in tale categoria.

Se l'URL in ingresso corrisponde a una prenotazione ma non a una registrazione, l'API del server HTTP ha esito negativo per la richiesta. In questo modo si impedisce che le registrazioni con priorità inferiore siano in grado di prelevare richieste non desiderate. Lo stato in caso di errore è 400 ("richiesta non valida") anziché 503 ("servizio non disponibile"), perché un ritorno 503 viene talvolta interpretato erroneamente dai gateway di bilanciamento del carico come indicato che il server è stato sottoposto a overload.

Se viene rilevata una registrazione corrispondente all'interno della categoria, la richiesta viene instradata alla coda di richieste associata a tale registrazione. La richiesta viene sempre indirizzata alla coda associata alla UrlPrefix corrispondente più estesa all'interno di una categoria.

Se non viene trovata alcuna corrispondenza nella categoria, l'API server HTTP passa alla categoria esplicita e ripete la stessa procedura. Per riepilogare, l'ordine in cui vengono esaminate le categorie è il seguente:

1.  Carattere jolly sicuro
2.  Esplicita
3.  Carattere jolly IP-Bound vulnerabile
4.  Carattere jolly vulnerabile

Se non viene trovata alcuna corrispondenza in nessuna delle categorie, l'API del server HTTP invia una risposta con un codice di stato 400 per indicare che non è possibile indirizzare la richiesta.

## <a name="longest-match-rule"></a>Regola di corrispondenza più lungo

All'interno di ogni categoria UrlPrefix, l'API server HTTP instrada una richiesta alla coda associata al UrlPrefix più lungo corrispondente. Si supponga, ad esempio, che i due prefissi URL seguenti siano registrati in code diverse:

- `Queue1 https://www.adatum.com:80/`
- `Queue2 https://www.adatum.com:80/dir/sna/`

L'API server HTTP instrada una richiesta di `https://www.adatum.com:80/default.htm` a Queue1 e una richiesta di `https://www.adatum.com:80/dir/sna/snadefault.htm` a Queue2. Instrada una richiesta di `https://www.adatum.com:80/dir/app.htm` a Queue1 poiché la corrispondenza completa più estesa è con `https://www.adatum.com:80/` URLPrefix, non con `https://www.adatum.com:80/dir/sna` URLPrefix.

 

 




