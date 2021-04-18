---
description: Per sfruttare i vantaggi delle funzioni abilitate per IPv6, gli amministratori IT devono definire all'interno del proprio script WPAD una funzione denominata FindProxyForURLEx (URL, host) che sostituisce la funzione FindProxyForUrl (URL, host) legacy.
ms.assetid: e531a66d-5c50-4065-a12a-783fd4d1d310
title: IPv6-Aware definizioni API helper proxy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79b1ff5a0c287327593e65e29a0b03cfb59269f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317019"
---
# <a name="ipv6-aware-proxy-helper-api-definitions"></a>IPv6-Aware definizioni API helper proxy

Per sfruttare i vantaggi delle funzioni abilitate per IPv6, gli amministratori IT devono definire all'interno del proprio script WPAD una funzione denominata FindProxyForURLEx (URL, host) che sostituisce la funzione FindProxyForUrl (URL, host) legacy. Solo dalla nuova funzione FindProxyForURLEx gli amministratori saranno in grado di eseguire le nuove funzioni.

Si è tentato anche di semplificare il lavoro per gli sviluppatori, allineando le funzioni in modo da restituire tipi diversi di indirizzi IP nello stesso ordine di preferenza degli altri componenti di rete, in particolare gli indirizzi IPv6 seguiti dagli indirizzi IPv4 (ovvero il comportamento corrente per la funzione funzione getaddrinfo (..) di Winsock.

Le funzioni seguenti sono estensioni per la [specifica del formato di file di Navigator proxy auto-config (PAC)](https://web.archive.org/web/20060424005037/wp.netscape.com/eng/mozilla/2.0/relnotes/demo/proxy-live.html) per consentire agli script WPAD di gestire le reti compatibili con IPv6.

## <a name="predefined-functions-and-environment-for-the-javascript-function-findproxyforurlex"></a>Funzioni e ambiente predefiniti per la funzione JavaScript FindProxyforURLEx

Condizioni basate sul nome host

<dl> <dt>

[**isResolvableEx**](isresolvableex.md)
</dt> <dd>

Determina se una determinata stringa host può essere risolta in un indirizzo IP.

</dd> <dt>

[**isInNetEx**](isinnetex.md)
</dt> <dd>

Determina se un indirizzo IP si trova in una subnet specifica.

</dd> </dl>

Funzioni di utilità correlate

<dl> <dt>

[**dnsResolveEx**](dnsresolveex.md)
</dt> <dd>

Risolvere una stringa host nel relativo indirizzo IP.

</dd> <dt>

[**myIPAddressEx**](myipaddressex.md)
</dt> <dd>

Trova tutti gli indirizzi IP per localhost.

</dd> <dt>

[**sortIpAddressList**](sortipaddresslist.md)
</dt> <dd>

Ordina un elenco di indirizzi IP.

</dd> <dt>

[**getClientVersion**](getclientversion.md)
</dt> <dd>

Ottiene la versione del motore di elaborazione WPAD.

</dd> </dl>

> [!Note]  
> Questa funzionalità richiede Windows Internet Explorer 7 o versione successiva.

 

 

 



