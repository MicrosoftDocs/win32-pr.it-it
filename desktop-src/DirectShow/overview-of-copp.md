---
description: Panoramica di COPP
ms.assetid: 4421ab65-e44a-4d1f-8d9b-b187227429c6
title: Panoramica di COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41fc83293c1914ed69700cabb9507841d03a7ad3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303963"
---
# <a name="overview-of-copp"></a>Panoramica di COPP

Di seguito sono riportati i passaggi di base che un'applicazione deve eseguire per usare il protocollo COPP (Certified Output Protection Protocol).

**Ottenere la catena di certificati del driver**

1.  Creare un grafico di riproduzione DirectShow che esegua il rendering dei video usando il renderer di mixaggio video (VMR-7 o VMR-9) o il filtro [**renderer video avanzato**](enhanced-video-renderer-filter.md) (EVR).
2.  Eseguire una query su VMR per l'interfaccia [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) .
3.  Chiamare [**IAMCertifiedOutputProtection:: backexchange**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-keyexchange). Questo metodo restituisce un numero casuale a 128 bit dal driver, insieme a una catena di certificati che contiene la chiave pubblica RSA a 2048 bit del driver.

**Convalidare la catena di certificati**

1.  Convalidare la catena di certificati. Se la catena di certificati non è valida, arrestare.
2.  Controllare l'elenco di revoche di certificati (CRL). Se uno dei certificati nella catena di certificati viene visualizzato nell'elenco di revoche, arrestare.
3.  Ottenere la chiave pubblica RSA dalla catena di certificati.

**Inizializzare la sessione COPP**

1.  Generare una chiave di sessione AES a 128 bit. Questa chiave viene utilizzata per firmare i dati e verificare che i dati firmati non siano stati manomessi.
2.  Genera due numeri casuali a 32 bit a crittografia sicura. Il primo è un numero di sequenza di stato, il secondo è un numero di sequenza di comandi. Ogni volta che l'applicazione invia una richiesta di comando o di stato, incrementa il numero di sequenza corrispondente e include questo numero nel comando COPP o nei dati della richiesta.
3.  Concatenare il numero casuale a 128 bit dal driver della grafica, la chiave della sessione AES, il numero di sequenza dello stato e il numero di sequenza del comando. Crittografare questa matrice di byte utilizzando la chiave pubblica del driver e passare il risultato a [**IAMCertifiedOutputProtection:: SessionSequenceStart**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-sessionsequencestart).

**Inviare comandi di COPP e richieste di stato**

1.  Eseguire una query per i tipi di protezione disponibili e altre informazioni chiamando [**IAMCertifiedOutputProtection::P rotectionstatus**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectionstatus).
2.  Impostare i livelli di protezione desiderati chiamando [**IAMCertifiedOutputProtection::P rotectioncommand**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectioncommand).
3.  Eseguire periodicamente una query per il livello di protezione locale corrente. Arrestare la riproduzione se il livello di protezione locale cambia in modo imprevisto o se viene rilevato un problema.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di COPP (Certified Output Protocol)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



