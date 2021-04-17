---
title: WinINet rispetto a WinHTTP
description: Con alcune eccezioni, WinINet è un superset di WinHTTP. Quando si sceglie tra i due, è necessario usare WinINet, a meno che non si preveda di eseguire un servizio o un processo simile a un servizio che richiede la rappresentazione e l'isolamento della sessione.
ms.assetid: 77386b54-2c86-4a30-8c4c-88d5f15313d7
keywords:
- WinINet rispetto a WinHTTP
ms.topic: article
ms.date: 02/22/2019
ms.openlocfilehash: c4d161992c2202505e8c84c660ca1edc92cc7993
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300180"
---
# <a name="wininet-vs-winhttp"></a>WinINet rispetto a WinHTTP

Con alcune eccezioni, [WinInet](portal.md) è un superset di [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page). Quando si sceglie tra i due, è necessario usare WinINet, a meno che non si preveda di eseguire un servizio o un processo simile a un servizio che richiede la rappresentazione e l'isolamento della sessione.

## <a name="comparison-of-features"></a>Confronto delle funzionalità

| Funzionalità | WinINet | WinHTTP |
|-|-|-|
| **Cache delle credenziali** Consente a tutte le applicazioni predefinite in Windows Internet Explorer di ottenere automaticamente le credenziali. Consente inoltre a un'applicazione in esecuzione all'esterno di Internet Explorer di richiedere o specificare le credenziali per il server una sola volta. Da quel punto in poi, le richieste sono automatiche. | sì | no |
| **Richiesta di credenziali** Fornisce un'API che consente al codice chiamante di richiedere le credenziali all'utente. | sì | no |
| **FTP** | sì | no |
| **Supporto della connessione automatica/RAS** Si tratta di una funzionalità legacy. In alternativa, usare [accesso remoto](/windows/desktop/RRAS/portal) . | sì | no |
| **Zone** Integrazione automatica con le aree di sicurezza di Internet Explorer. | sì | no |
| **Supporto di IDNA** Supporto integrato per IDNA RFC/Punycode. | sì | sì |
| **API jar cookie** Sono supportati i cookie persistenti e non permanenti. Qualsiasi applicazione o script può utilizzarlo per visualizzare gli stessi cookie del browser. | sì | no |
| **Supporto di IE per la modalità protetta** | sì | no |
| **Supporto della decompressione** Supporto per lo schema di compressione gzip e Deflate. | sì | sì |
| **Supporto** per il caricamento in blocchi Il codice client deve eseguire la suddivisione in blocchi. | no | sì |
| **Supporto per Socks V4** Non include V4A o V5. | sì | no |
| **Invio e ricezione bidirezionali** | no | no |
| **I/O sovrapposti** | no | no |
| **Supporto dello schema di file** Utile per gli script proxy con uno schema di file. | sì | no |
| **InternetOpenUrl** Codice semplificato per aprire un URL. | sì | no |
| **Supporto dei servizi** Può essere eseguito da un servizio o da un account del servizio. | no | sì |
| **Isolamento della sessione** Le sessioni separate non hanno alcun effetto. | no | sì |
| **Rappresentazione** Supporta la chiamata di mentre il thread rappresenta un utente diverso. | no | sì |

## <a name="related-topics"></a>Argomenti correlati

* [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page)
* [WinINet](/windows/desktop/WinInet/about-wininet)