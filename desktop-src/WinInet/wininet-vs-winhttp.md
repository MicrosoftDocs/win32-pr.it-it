---
title: Confronto tra WinINet e WinHTTP
description: Informazioni su come scegliere tra WinInet e WinHTTP. Leggere un confronto delle funzionalità ed esaminare gli argomenti correlati.
ms.assetid: 77386b54-2c86-4a30-8c4c-88d5f15313d7
keywords:
- Confronto tra WinINet e WinHTTP
ms.topic: article
ms.date: 02/22/2019
ms.openlocfilehash: 20bd0ced1d0ea897dba05680258cae4a2b1a248b204824ded7d2ec5be30ff00b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899091"
---
# <a name="wininet-vs-winhttp"></a>Confronto tra WinINet e WinHTTP

Con alcune eccezioni, [WinINet](portal.md) è un superset di [WinHTTP.](/windows/desktop/WinHttp/winhttp-start-page) Quando si seleziona tra i due, è consigliabile usare WinINet, a meno che non si prevede di eseguire all'interno di un servizio o di un processo simile a un servizio che richiede la rappresentazione e l'isolamento della sessione.

## <a name="comparison-of-features"></a>Confronto delle funzionalità

| Funzionalità | Wininet | WinHTTP |
|-|-|-|
| **Cache delle credenziali** Consente a tutte le applicazioni incorporate Windows Internet Explorer ottenere automaticamente le credenziali. Consente inoltre a un'applicazione in esecuzione all'Internet Explorer di richiedere o specificare le credenziali per il server una sola volta. Da questo punto in poi le richieste sono automatiche. | sì | no |
| **Richiesta di credenziali** Fornisce un'API che consente al codice chiamante di richiedere le credenziali all'utente. | sì | no |
| **FTP** | sì | no |
| **Supporto automatico/RAS** Si tratta di funzionalità legacy. Usare [invece Accesso](/windows/desktop/RRAS/portal) remoto. | sì | no |
| **Zone** Integrazione automatica con le Internet Explorer di sicurezza. | sì | no |
| **Supporto IDNA** Supporto integrato per IDNA RFC/Punycode. | sì | sì |
| **API Cookie Jar** Sono supportati cookie persistenti e non persistenti. Qualsiasi applicazione o script può usarlo per visualizzare gli stessi cookie del browser. | sì | no |
| **Supporto di IE in modalità protetta** | sì | no |
| **Supporto della decompressione** Supporto per gzip e schema di compressione deflate. | sì | sì |
| **Supporto Upload blocchi** Il codice client deve eseguire la suddivisione in blocchi. | no | sì |
| **Supporto di SOCKS v4** Non include v4a o v5. | sì | no |
| **Invio e ricezione bidirezionale** | no | no |
| **I/O sovrapposto** | no | no |
| **Supporto dello schema di file** Utile per gli script proxy con uno schema di file. | sì | no |
| **InternetOpenUrl** Codice semplificato per aprire un URL. | sì | no |
| **Supporto dei servizi** Può essere eseguito da un servizio o da un account del servizio. | no | sì |
| **Isolamento sessione** Le sessioni separate non influiscono l'una sull'altra. | no | sì |
| **Rappresentazione** Supporta la chiamata mentre il thread rappresenta un utente diverso. | no | sì |

## <a name="related-topics"></a>Argomenti correlati

* [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page)
* [Wininet](/windows/desktop/WinInet/about-wininet)