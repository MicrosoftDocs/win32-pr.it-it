---
description: Specifica un prefisso collegato all'interfaccia \# 4.
ms.assetid: cc3aa99d-cf45-460c-bdc1-3e9a19806fe4
title: Prefissi di sito IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bed8a21c59f9b6727c98ccb7fdacf4e9ec6ea5cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306900"
---
# <a name="ipv6-site-prefixes"></a>Prefissi di sito IPv6

Il comando RTU IPv6 consente la configurazione dei prefissi di collegamento pubblicati con una lunghezza del prefisso del sito. Se specificato, la lunghezza del prefisso del sito viene inserita in un'opzione di informazioni sul prefisso negli annunci router. Ad esempio:

``` syntax
ipv6 rtu 2002:836b:9820:2::/64 4 pub life 1800 spl 48
```

Specifica un prefisso collegato all'interfaccia \# 4. Il prefisso viene pubblicato, vale a dire che è incluso negli annunci router se l'interfaccia \# 4 è un'interfaccia pubblicitaria. La durata nell'opzione informazioni sul prefisso è di 1800 secondi (30 minuti). La lunghezza del prefisso del sito nell'opzione informazioni sul prefisso è 48.

La ricezione di un'opzione di informazioni sul prefisso che specifica un prefisso del sito determina la creazione di una voce nella tabella dei prefissi del sito, che può essere visualizzata tramite il comando IPv6 SPT. La tabella dei prefissi del sito viene usata per rimuovere gli indirizzi locali del sito non appropriati da quelli restituiti da [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) e dalle funzioni correlate.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Collegamento IPv6-indirizzi locali e locali del sito](link-local-and-site-local-addresses-2.md)
</dt> <dt>

[Netsh.exe](netsh-exe.md)
</dt> </dl>

 

 



