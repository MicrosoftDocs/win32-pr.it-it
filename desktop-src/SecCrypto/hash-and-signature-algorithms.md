---
description: Gli algoritmi seguenti consentono di calcolare hash e firme digitali. Ognuno di questi algoritmi è supportato nei provider di crittografia Microsoft base, Strong e Enhanced.
ms.assetid: 91bf898d-658a-4e45-aa6e-eded46657563
title: Algoritmi hash e di firma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc1ca0819aebc01bba342410eda20b626349f1b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319360"
---
# <a name="hash-and-signature-algorithms"></a>Algoritmi hash e di firma

Gli algoritmi seguenti consentono di calcolare [*hash*](../secgloss/h-gly.md) e [*firme digitali*](../secgloss/d-gly.md). Ognuno di questi algoritmi è supportato nei provider di crittografia Microsoft base, Strong e Enhanced. I dettagli interni di questi algoritmi esulano dall'ambito di questa documentazione. Per un elenco di origini aggiuntive, vedere la [documentazione aggiuntiva su crittografia](additional-documentation-on-cryptography.md).



| Algoritmi                                     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MAC CBC (Cipher Block Chaining)<br/>     | Uno degli algoritmi (CALG \_ Mac) implementato dai provider Microsoft è una crittografia a [*blocchi*](../secgloss/b-gly.md) [*Message Authentication Code*](../secgloss/m-gly.md) (Mac). Questo metodo crittografa i dati di base con una crittografia a blocchi, quindi usa l'ultimo blocco crittografato come valore [*hash*](../secgloss/h-gly.md) . L'algoritmo di crittografia usato per compilare il MAC è quello specificato al momento della creazione della chiave di sessione. <br/>                                                                            |
| HMAC<br/>                                | Algoritmo (CALG \_ HMAC) implementato dai provider Microsoft. Questo algoritmo usa inoltre una [*chiave simmetrica*](../secgloss/s-gly.md) per creare l' [*hash*](../secgloss/h-gly.md), ma è più complesso rispetto all'algoritmo MAC CBC (Simple [*Cipher Block Chaining*](../secgloss/c-gly.md) ). Può essere usato con qualsiasi algoritmo hash crittografico iterato, ad esempio MD5 o SHA-1. Per informazioni dettagliate, vedere [creazione di un HMAC](creating-an-hmac.md).<br/>                                                                                       |
| MD2, MD4 e MD5<br/>                   | Questi algoritmi di hashing sono stati tutti sviluppati da RSA Data Security, Inc. Questi algoritmi sono stati sviluppati in ordine sequenziale. Tutti e tre generano valori hash a 128 bit. Tutti e tre sono noti per avere debolezze e devono essere usati solo se necessario per motivi di compatibilità. Per il nuovo codice, è consigliabile usare la famiglia SHA-2 di hash.<br/> Questi algoritmi sono ben noti e possono essere esaminati in dettaglio in qualsiasi riferimento alla [*crittografia*](../secgloss/c-gly.md).<br/>                                                                                                                                                           |
| Message Authentication Code (MAC)<br/>   | Gli algoritmi MAC sono simili agli algoritmi [*hash*](../secgloss/h-gly.md) , ma vengono calcolati usando una chiave [*simmetrica*](../secgloss/s-gly.md) (sessione). Per ricalcolare il valore hash è necessaria la [*chiave della sessione*](../secgloss/s-gly.md) originale. Il valore hash ricalcolato viene utilizzato per verificare che i dati di base non siano stati modificati. Questi algoritmi sono talvolta denominati algoritmi hash con chiave. Per vedere quali provider Microsoft supportano MAC, vedere [provider del servizio di crittografia Microsoft](microsoft-cryptographic-service-providers.md).<br/>    |
| Algoritmo Secure Hash Algorithm (SHA-1)<br/>       | Questo algoritmo di hash è stato sviluppato dal [*National Institute of Standards and Technology*](../secgloss/n-gly.md) (NIST) e dalla National Security Agency (NSA). Questo algoritmo è stato sviluppato per l'uso con DSA (Digital Signature Algorithm) o DSS (Digital Signature Standard). Questo algoritmo genera un valore [*hash*](../secgloss/h-gly.md) a 160 bit. SHA-1 è noto che presenta debolezze e deve essere usato solo se richiesto per motivi di compatibilità. Per il nuovo codice, è consigliabile usare la famiglia SHA-2 di hash.<br/> |
| Algoritmo Secure Hash Algorithm-2 (SHA-2)<br/>   | Questo algoritmo di hashing è stato sviluppato come successore di SHA-1 dal [*National Institute of Standards and Technology*](../secgloss/n-gly.md) (NIST) e National Security Agency (NSA). Sono disponibili quattro varianti: SHA-224, SHA-256, SHA-384 e SHA-512, denominate in base al numero di bit nei rispettivi output. Di questi, SHA-256, SHA-384 e SHA-512 sono implementati in Microsoft AES Cryptographic Provider.<br/>                                                                                                                                |
| Algoritmo di autorizzazione client di SSL3<br/> | Questo algoritmo viene usato per l'autenticazione del client SSL3. Nel protocollo SSL3, una concatenazione di un hash MD5 e di un hash SHA viene firmata con una [*chiave privata*](../secgloss/p-gly.md)RSA. CryptoAPI 2.0 e Microsoft base e i provider di servizi di crittografia avanzati supportano questo tipo di [*hash*](../secgloss/h-gly.md) CALG \_ SSL3 \_ SHAMD5. Per altre informazioni, vedere [creazione di un \_ hash CALG SSL3 \_ SHAMD5](creating-a-calg-ssl3-shamd5-hash.md).<br/>                                                                                                                                               |



 

 

 
