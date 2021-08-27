---
title: UrlPrefix Strings (Stringhe UrlPrefix)
description: Nell'API del server HTTP, UrlPrefix è una stringa Unicode a caratteri wide (UTF-16) con un formato canonico che specifica una sezione dello spazio dei nomi DELL'URL.
ms.assetid: 4f317bf6-ee6a-47a8-a531-78534217109d
keywords:
- API server HTTP per stringhe UrlPrefix
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3fad89bf7abd52ee3681beaa8069a7f5e4ee25b482cd065f880263852690fce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047041"
---
# <a name="urlprefix-strings"></a>UrlPrefix Strings (Stringhe UrlPrefix)

Nell'API del server HTTP, *UrlPrefix* è una stringa Unicode a caratteri wide (UTF-16) con un formato canonico che specifica una sezione dello spazio dei nomi DELL'URL. Viene usato per riservare una sezione dello spazio dei nomi URL per un account utente o per registrare una sezione dello spazio dei nomi URL per un processo.

## <a name="urlprefix-format"></a>Formato UrlPrefix

UrlPrefix ha la sintassi seguente:

"scheme://host:port/relativeURI"

Gli elementi schema, host e porta di urlPrefix devono essere presenti e non vuoti e devono rispettare le regole seguenti:

<dl> <dt>

<span id="scheme"></span><span id="SCHEME"></span>Schema
</dt> <dd>

Deve essere http o https, tutto in minuscolo.

</dd> <dt>

<span id="host"></span><span id="HOST"></span>Host
</dt> <dd>

Deve essere un nome di dominio completo, una stringa letterale IPv4 o IPv6 o un carattere jolly. A differenza dello schema, che deve essere minuscolo, la parte host non fa distinzione tra maiuscole e minuscole. A seconda di come viene specificata la parte host, un UrlPrefix rientra in una delle quattro categorie di routing seguenti, descritte più dettagliatamente di seguito:

<dl> <dd>Carattere jolly sicuro</dd> <dd>Esplicita</dd> <dd>Carattere jolly debole associato a IP</dd> <dd>Carattere jolly debole</dd> </dl> </dd> <dt>

<span id="port"></span><span id="PORT"></span>Porta
</dt> <dd>

Stringa numerica decimale che non inizia con zero e rappresenta un numero di porta TCP valido (da 1 a 65.535). Questo valore non può essere un carattere jolly.

</dd> <dt>

<span id="relativeURI"></span><span id="relativeuri"></span><span id="RELATIVEURI"></span>Relativeuri
</dt> <dd>

L'elemento relativeURI è facoltativo, ma se presente deve essere sempre seguito da una barra ("/"). Si tratta di una stringa di prefisso che indica un sottoalbero all'interno dello spazio dei nomi del computer specificato in relazione ai valori di schema, host e porta. A differenza dello schema, che deve essere minuscolo, la parte relativeURI non fa distinzione tra maiuscole e minuscole.

</dd> </dl>

Di seguito sono riportati alcuni esempi di UrlPrefix correttamente formati:

-   `https://www.adatum.com:80/vroot/`
-   `https://adatum.com:443/secure/database/`
-   `https://+:80/vroot/`

## <a name="host-specifier-categories"></a>Host-Specifier categorie

Per flessibilità e facilità d'uso, l'API del server HTTP supporta quattro modi diversi per specificare gli host. Le quattro categorie di identificatori host sono elencate di seguito in ordine di precedenza:

<dl> <dt>

<span id="Strong_wildcard__Plus_Sign_"></span><span id="strong_wildcard__plus_sign_"></span><span id="STRONG_WILDCARD__PLUS_SIGN_"></span>Carattere jolly sicuro (segno più)
</dt> <dd>

Quando l'elemento host di un UrlPrefix è costituito da un singolo segno più (+), UrlPrefix corrisponde a tutti i nomi host possibili nel contesto degli elementi scheme, port e relativeURI e rientra nella categoria dei caratteri jolly sicuri.

Un carattere jolly sicuro è utile quando un'applicazione deve gestire le richieste indirizzate a uno o più URI relativi, indipendentemente dal modo in cui tali richieste arrivano nel computer o dal sito specificato nelle intestazioni host. L'uso di un carattere jolly sicuro in questa situazione evita la necessità di specificare un elenco completo di host e/o indirizzi IP.

</dd> <dt>

<span id="Explicit"></span><span id="explicit"></span><span id="EXPLICIT"></span>Esplicito
</dt> <dd>

Un nome host esplicito, ad esempio un nome di dominio completo nell'elemento host, inserisce urlPrefix nella categoria esplicita. Questo tipo di elemento host viene abbinato direttamente alle intestazioni Host delle richieste in ingresso.

Specifiche host esplicite sono utili per le applicazioni multisnodato, ad esempio i server Web che forniscono contenuto diverso a seconda del sito a cui è stata indirizzata la richiesta.

</dd> <dt>

<span id="IP-bound_weak_wildcard"></span><span id="ip-bound_weak_wildcard"></span><span id="IP-BOUND_WEAK_WILDCARD"></span>Carattere jolly debole associato a IP
</dt> <dd>

Quando un indirizzo IP viene visualizzato come elemento host, UrlPrefix rientra nella categoria Carattere jolly debole associato all'INDIRIZZO IP. Questo tipo di UrlPrefix corrisponde a qualsiasi nome host per l'interfaccia IP specificata con lo schema, la porta e l'URI relativo specificati e che non è già stato abbinato da un carattere jolly sicuro o da urlPrefix esplicito. L'indirizzo IP assume una delle due forme seguenti nell'elemento host:

<dl> <dt>

<span id="IPv4_Literal_String"></span><span id="ipv4_literal_string"></span><span id="IPV4_LITERAL_STRING"></span>Stringa letterale IPv4
</dt> <dd>

Un valore letterale IPv4 è costituito da quattro numeri decimali punteggiati, ognuno nell'intervallo 0-255, ad esempio 192.168.0.0.

</dd> <dt>

<span id="IPv6_Literal_String"></span><span id="ipv6_literal_string"></span><span id="IPV6_LITERAL_STRING"></span>Stringa letterale IPv6
</dt> <dd>

Una stringa letterale IPv6 è racchiusa tra parentesi quadre e contiene numeri esadecimali separati da due punti. ad esempio: \[ ::1 \] o \[ 3ffe:ffff::6ECB:0101 \] .

</dd> </dl>

Gli identificatori host con caratteri jolly deboli associati a IP sono destinati alle applicazioni che variano il contenuto che servono in base alla route intrapresa dalle richieste in ingresso. Non fare affidamento sugli identificatori host con caratteri jolly deboli associati a IP per applicare la sicurezza.

</dd> <dt>

<span id="Weak_wildcard__asterisk_"></span><span id="weak_wildcard__asterisk_"></span><span id="WEAK_WILDCARD__ASTERISK_"></span>Carattere jolly debole (asterisco)
</dt> <dd>

Quando viene visualizzato un asterisco ( \* ) come elemento host, UrlPrefix rientra nella categoria di caratteri jolly deboli. Questo tipo di UrlPrefix corrisponde a qualsiasi nome host associato allo schema, alla porta e all'URI relativi specificati a cui non è già stata trovata una corrispondenza con un carattere jolly sicuro, esplicito o con carattere jolly debole associato a IP.

Questa specifica host può essere usata come catch-all predefinito in alcune circostanze oppure può essere usata per specificare una sezione di grandi dimensioni dello spazio dei nomi URL senza dover usare molti UrlPrefix.

</dd> </dl>

## <a name="urlprefix-conflict-detection-during-reservation-and-registration"></a>Rilevamento dei conflitti UrlPrefix durante la prenotazione e la registrazione

Ai fini della prenotazione e della registrazione, le quattro diverse categorie di UrlPrefix vengono trattate separatamente, senza riferimenti l'una all'altra. È possibile registrare urlPrefix in conflitto, purché siano in categorie diverse. Solo all'interno della stessa categoria un conflitto causa l'esito negativo di un tentativo di prenotazione.

Ad esempio, sarebbe possibile riservare sia urlPrefix esplicito che urlPrefix con carattere jolly sicuro in conflitto, poiché appartengono `https://www.adatum.com:80/vroot/` `https://+:80/vroot/` a categorie diverse. Tuttavia, un tentativo successivo di riservare a un utente diverso avrà esito negativo perché è in conflitto con una prenotazione https://+:80/vroot/ esistente nella propria categoria.

## <a name="routing-behavior"></a>Comportamento di routing

Quando si instrada una richiesta HTTP in ingresso, l'API del server HTTP inizia con la categoria con caratteri jolly forte e confronta l'URL in ingresso con urlPrefix registrati e riservati in tale categoria.

Se l'URL in ingresso corrisponde a una prenotazione ma non a una registrazione, l'API del server HTTP ha esito negativo della richiesta. In questo modo si impedisce alle registrazioni con priorità più bassa di essere in grado di prelevare le richieste non destinate. Lo stato in caso di errore è 400 ("Richiesta non valida") anziché 503 ("Servizio non disponibile"), perché un ritorno a 503 viene talvolta interpretato erroneamente dai gateway di bilanciamento del carico come indica che il server è sovraccarico.

Se viene trovata una registrazione corrispondente all'interno della categoria, la richiesta viene indirizzata alla coda di richieste associata alla registrazione. La richiesta viene sempre indirizzata alla coda associata all'urlPrefix corrispondente più lungo all'interno di una categoria.

Se nella categoria non viene trovata alcuna corrispondenza, l'API del server HTTP passa alla categoria esplicita e ripete la stessa procedura. Per riepilogare, l'ordine in cui vengono esaminate le categorie è il seguente:

1.  Carattere jolly sicuro
2.  Esplicita
3.  IP-Bound carattere jolly debole
4.  Carattere jolly debole

Se non viene trovata alcuna corrispondenza in nessuna delle categorie, l'API del server HTTP invia una risposta con codice di stato 400 per indicare che la richiesta non può essere indirizzata.

## <a name="longest-match-rule"></a>Regola di corrispondenza più lunga

All'interno di ogni categoria UrlPrefix, l'API del server HTTP instrada una richiesta alla coda associata all'UrlPrefix corrispondente più lungo. Si supponga, ad esempio, che i due UrlPrefix seguenti siano registrati in code diverse:

- `Queue1 https://www.adatum.com:80/`
- `Queue2 https://www.adatum.com:80/dir/sna/`

L'API del server HTTP instrada una richiesta per `https://www.adatum.com:80/default.htm` a Queue1 e una richiesta per `https://www.adatum.com:80/dir/sna/snadefault.htm` a Queue2. Instrada una richiesta per a Queue1 perché la corrispondenza completa più lunga è con `https://www.adatum.com:80/dir/app.htm` `https://www.adatum.com:80/` UrlPrefix, non con `https://www.adatum.com:80/dir/sna` UrlPrefix.

 

 




