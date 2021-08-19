---
description: specifica un prefisso che è in collegamento all'interfaccia \# 4.
ms.assetid: cc3aa99d-cf45-460c-bdc1-3e9a19806fe4
title: Prefissi del sito IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dd37370aa14bd6883f83e93d661f10b96d804dc3b85cf47173da4b1f0ee0f90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118111295"
---
# <a name="ipv6-site-prefixes"></a>Prefissi del sito IPv6

Il comando ipv6 rtu consente la configurazione dei prefissi on-link pubblicati con una lunghezza del prefisso del sito. Se specificato, la lunghezza del prefisso del sito viene inserita in un'opzione di informazioni sul prefisso negli annunci router. Esempio:

``` syntax
ipv6 rtu 2002:836b:9820:2::/64 4 pub life 1800 spl 48
```

specifica un prefisso che è in collegamento all'interfaccia \# 4. Il prefisso viene pubblicato, ovvero è incluso negli annunci del router se \# l'interfaccia 4 è un'interfaccia pubblicitaria. La durata nell'opzione relativa alle informazioni sul prefisso è di 1800 secondi (30 minuti). La lunghezza del prefisso del sito nell'opzione informazioni sul prefisso è 48.

La ricezione di un'opzione di informazioni sul prefisso che specifica un prefisso del sito determina la creazione di una voce nella tabella del prefisso del sito, che può essere visualizzata usando il comando ipv6 spt. La tabella del prefisso del sito viene usata per rimuovere gli indirizzi locali del sito non appropriati da quelli restituiti da [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) e dalle funzioni correlate.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Indirizzi IPv6 link-local e site-local](link-local-and-site-local-addresses-2.md)
</dt> <dt>

[Netsh.exe](netsh-exe.md)
</dt> </dl>

 

 



