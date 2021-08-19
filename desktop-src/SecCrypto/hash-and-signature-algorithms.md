---
description: Gli algoritmi seguenti calcolano hash e firme digitali. Ognuno di questi algoritmi è supportato nei provider di crittografia Microsoft Base, Strong e Enhanced.
ms.assetid: 91bf898d-658a-4e45-aa6e-eded46657563
title: Algoritmi hash e di firma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7c176b3a21ac5793f249f9aa7aceda897d53ea209f3e8e6bd260dc5ec529c92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006609"
---
# <a name="hash-and-signature-algorithms"></a>Algoritmi hash e di firma

Gli algoritmi seguenti calcolano [*hash e*](../secgloss/h-gly.md) [*firme digitali*](../secgloss/d-gly.md). Ognuno di questi algoritmi è supportato nei provider di crittografia Microsoft Base, Strong e Enhanced. I dettagli interni di questi algoritmi non sono nell'ambito di questa documentazione. Per un elenco di origini aggiuntive, vedere [Documentazione aggiuntiva sulla crittografia](additional-documentation-on-cryptography.md).



| Algoritmi                                     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cipher Block Chaining (CBC) MAC<br/>     | Uno degli algoritmi (MAC CALG) implementati dai provider Microsoft è una crittografia \_ a blocchi [](../secgloss/b-gly.md) [*Message Authentication Code*](../secgloss/m-gly.md) (MAC). Questo metodo crittografa i dati di base con una crittografia a blocchi e quindi usa l'ultimo blocco crittografato come [*valore hash.*](../secgloss/h-gly.md) L'algoritmo di crittografia usato per compilare il MAC è quello specificato al momento della creazione della chiave di sessione. <br/>                                                                            |
| HMAC<br/>                                | Algoritmo (CALG \_ HMAC) implementato dai provider Microsoft. Questo algoritmo usa anche una chiave [*simmetrica*](../secgloss/s-gly.md) per creare [*l'hash*](../secgloss/h-gly.md), ma è più complesso del semplice algoritmo MAC [*Cipher Block Chaining*](../secgloss/c-gly.md) (CBC). Può essere usato con qualsiasi algoritmo hash crittografico iterato, ad esempio MD5 o SHA-1. Per informazioni dettagliate, vedere [Creazione di un HMAC.](creating-an-hmac.md)<br/>                                                                                       |
| MD2, MD4 e MD5<br/>                   | Questi algoritmi di hash sono stati tutti sviluppati da RSA Data Security, Inc. Questi algoritmi sono stati sviluppati in ordine sequenziale. Tutti e tre generano valori hash a 128 bit. Tutti e tre sono noti per avere punti deboli e devono essere usati solo dove necessario per motivi di compatibilità. Per il nuovo codice, è consigliabile usare la famiglia di hash SHA-2.<br/> Questi algoritmi sono noti e possono essere esaminati in dettaglio in qualsiasi riferimento sulla [*crittografia.*](../secgloss/c-gly.md)<br/>                                                                                                                                                           |
| Message Authentication Code (MAC)<br/>   | Gli algoritmi MAC sono simili agli [*algoritmi hash,*](../secgloss/h-gly.md) ma vengono calcolati usando una chiave [*simmetrica*](../secgloss/s-gly.md) (sessione). La chiave [*di sessione originale*](../secgloss/s-gly.md) è necessaria per ricalcolare il valore hash. Il valore hash ricalcolato viene usato per verificare che i dati di base non siano stati modificati. Questi algoritmi sono talvolta denominati algoritmi con chiave hash. Per vedere quali provider Microsoft supportano MAC, vedere [Provider del servizio di crittografia Microsoft](microsoft-cryptographic-service-providers.md).<br/>    |
| Algoritmo hash sicuro (SHA-1)<br/>       | Questo algoritmo hash è stato sviluppato dal [*National Institute of Standards and Technology*](../secgloss/n-gly.md) (NIST) e dalla National Security Agency (NSA). Questo algoritmo è stato sviluppato per l'uso con DSA (Digital Signature Algorithm) o DSS (Digital Signature Standard). Questo algoritmo genera un valore [*hash*](../secgloss/h-gly.md) a 160 bit. SHA-1 è noto per avere punti deboli e deve essere usato solo quando necessario per motivi di compatibilità. Per il nuovo codice, è consigliabile usare la famiglia di hash SHA-2.<br/> |
| Algoritmo hash sicuro - 2 (SHA-2)<br/>   | Questo algoritmo hash è stato sviluppato come successore di SHA-1 dal [*National Institute of Standards and Technology*](../secgloss/n-gly.md) (NIST) e dalla National Security Agency (NSA). Ha quattro varianti, SHA-224, SHA-256, SHA-384 e SHA-512, denominate in base al numero di bit nei rispettivi output. Di questi, SHA-256, SHA-384 e SHA-512 vengono implementati nel provider di crittografia Microsoft AES.<br/>                                                                                                                                |
| Algoritmo di autorizzazione client SSL3<br/> | Questo algoritmo viene usato per l'autenticazione client SSL3. Nel protocollo SSL3, una concatenazione di un hash MD5 e di un hash SHA viene firmata con una chiave [*privata*](../secgloss/p-gly.md)RSA. CryptoAPI 2.0 e microsoft Base e i provider di crittografia avanzata supportano questo tipo di [*hash*](../secgloss/h-gly.md) CALG \_ SSL3 \_ SHAMD5. Per altre informazioni, vedere [Creazione di un hash \_ CALG SSL3 \_ SHAMD5.](creating-a-calg-ssl3-shamd5-hash.md)<br/>                                                                                                                                               |



 

 

 
