---
title: Confronto tra WinINet e WinHTTP
description: Informazioni su come scegliere tra WinInet e WinHTTP. Leggere un confronto delle funzionalità ed esaminare gli argomenti correlati.
ms.assetid: 77386b54-2c86-4a30-8c4c-88d5f15313d7
keywords:
- Confronto tra WinINet e WinHTTP
ms.topic: article
ms.date: 02/22/2019
ms.openlocfilehash: 8ced80dd048559fee483e8cf121918eed75fc462
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118796"
---
# <a name="wininet-vs-winhttp"></a>Confronto tra WinINet e WinHTTP

Con alcune eccezioni, [WinINet](portal.md) è un superset di [WinHTTP.](/windows/desktop/WinHttp/winhttp-start-page) Quando si seleziona tra i due, è consigliabile usare WinINet, a meno che non si prevede di eseguire all'interno di un servizio o di un processo simile a un servizio che richiede la rappresentazione e l'isolamento della sessione.

## <a name="comparison-of-features"></a>Confronto delle funzionalità

| Funzionalità | Wininet | WinHTTP |
|-|-|-|
| **Cache delle credenziali** Consente a tutte le applicazioni incorporate in Windows Internet Explorer di ottenere automaticamente le credenziali. Consente inoltre a un'applicazione in esecuzione all'Internet Explorer di richiedere o specificare le credenziali per il server una sola volta. Da questo punto in poi le richieste sono automatiche. | sì | No |
| **Richiesta di credenziali** Fornisce un'API che consente al codice chiamante di richiedere le credenziali all'utente. | sì | No |
| **FTP** | sì | No |
| **Supporto automatico/RAS** Si tratta di funzionalità legacy. Usare [invece Accesso](/windows/desktop/RRAS/portal) remoto. | sì | No |
| **Zone** Integrazione automatica con le Internet Explorer di sicurezza. | sì | No |
| **Supporto IDNA** Supporto integrato per IDNA RFC/Punycode. | Sì | Sì |
| **API Cookie Jar** Sono supportati cookie persistenti e non persistenti. Qualsiasi applicazione o script può usarlo per visualizzare gli stessi cookie del browser. | sì | No |
| **Supporto di IE in modalità protetta** | sì | No |
| **Supporto della decompressione** Supporto per gzip e schema di compressione deflate. | Sì | Sì |
| **Supporto per il caricamento in blocchi** Il codice client deve eseguire la suddivisione in blocchi. | No | sì |
| **Supporto di SOCKS v4** Non include v4a o v5. | sì | No |
| **Invio e ricezione bidirezionale** | No | No |
| **I/O sovrapposto** | No | No |
| **Supporto dello schema di file** Utile per gli script proxy con uno schema di file. | sì | No |
| **InternetOpenUrl** Codice semplificato per aprire un URL. | sì | No |
| **Supporto dei servizi** Può essere eseguito da un servizio o da un account del servizio. | No | sì |
| **Isolamento sessione** Le sessioni separate non influiscono l'una sull'altra. | No | sì |
| **Rappresentazione** Supporta la chiamata mentre il thread rappresenta un utente diverso. | No | sì |

## <a name="related-topics"></a>Argomenti correlati

* [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page)
* [Wininet](/windows/desktop/WinInet/about-wininet)