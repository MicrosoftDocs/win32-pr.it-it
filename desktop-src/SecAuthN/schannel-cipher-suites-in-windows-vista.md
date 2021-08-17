---
description: Set di algoritmi di crittografia. I protocolli Schannel usano gli algoritmi di un pacchetto di crittografia per creare chiavi e crittografare informazioni.
ms.assetid: 380452e2-a9c8-4380-a3bf-9c7942a0c0c2
title: Pacchetti di crittografia TLS in Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbf77d821612093e3015a0f8dee4cf51ae5bd9b95c653b61fe7a36271ba81ba5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918654"
---
# <a name="tls-cipher-suites-in-windows-vista"></a>Pacchetti di crittografia TLS in Windows Vista

Un pacchetto di crittografia è un set di algoritmi di crittografia. I protocolli Schannel usano gli algoritmi di un pacchetto di crittografia per creare chiavi e crittografare informazioni. Un pacchetto di crittografia specifica un algoritmo per ognuna delle attività seguenti:

-   Scambio di chiave
-   Crittografia di massa
-   Autenticazione dei messaggi

[*Gli algoritmi di scambio di chiavi*](../secgloss/k-gly.md) proteggono le informazioni necessarie per creare chiavi condivise. Questi algoritmi sono asimmetrici ([*algoritmi a chiave pubblica*](../secgloss/p-gly.md)) e sono molto validi per quantità relativamente ridotte di dati.

Gli algoritmi di crittografia bulk crittografano i messaggi s scambiati tra client e server. Questi algoritmi sono [*simmetrici e*](../secgloss/s-gly.md) sono molto validi per grandi quantità di dati.

[Gli algoritmi](message-authentication-codes-in-schannel.md) di autenticazione dei messaggi generano [*hash e*](../secgloss/h-gly.md) firme dei messaggi che garantiscono [*l'integrità*](../secgloss/i-gly.md) di un messaggio.

Gli sviluppatori specificano questi elementi usando i [**tipi di dati \_ ID ALG.**](../seccrypto/alg-id.md) Per altre informazioni, vedere [Specifying Schannel Ciphers and Cipher Strengths](specifying-schannel-ciphers-and-cipher-strengths.md).

Schannel supporta le suite di crittografia seguenti. Le suite sono elencate nell'ordine predefinito in cui vengono scelte dal provider Microsoft Schannel.

> [!IMPORTANT]
> I servizi Web HTTP/2 hanno esito negativo con suite di crittografia non compatibili con HTTP/2. Per assicurarsi che i servizi Web funzionino con client e browser HTTP/2, vedere Come distribuire l'ordinamento dei [pacchetti di crittografia personalizzati.](https://support.microsoft.com/help/4032720/how-to-deploy-custom-cipher-suite-ordering-in-windows-server-2016)

 



| Suite di crittografia                                                 | Modalità FIPS abilitata | Exchange              | Crittografia      | Hash            | Protocolli                   |
|--------------------------------------------------------------|-------------------|-----------------------|-----------------|-----------------|-----------------------------|
| TLS \_ RSA \_ CON \_ AES \_ 128 \_ CBC \_ SHA<br/>                | Sì<br/>    | RSA<br/>        | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ RSA \_ CON \_ AES \_ 256 \_ CBC \_ SHA<br/>                | Sì<br/>    | RSA<br/>        | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ RSA \_ CON \_ RC4 \_ 128 \_ SHA<br/>                     | No<br/>     | RSA<br/>        | RC4<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ CON \_ 3DES \_ EDE \_ CBC \_ SHA<br/>               | Sì<br/>    | RSA<br/>        | 3DES<br/> | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ CON \_ AES \_ 128 \_ CBC SHA \_ \_ P256<br/> | Sì<br/>    | ECDH \_ P256<br/> | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ CON \_ AES \_ 128 \_ CBC SHA \_ \_ P384<br/> | Sì<br/>    | ECDH \_ P384<br/> | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ CON \_ AES \_ 128 \_ CBC SHA \_ \_ P521<br/> | Sì<br/>    | ECDH \_ P521<br/> | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ CON \_ AES \_ 256 \_ CBC SHA \_ \_ P256<br/> | Sì<br/>    | ECDH \_ P256<br/> | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ CON \_ AES \_ 256 \_ CBC SHA \_ \_ P384<br/> | Sì<br/>    | ECDH \_ P384<br/> | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ CON \_ AES \_ 256 \_ CBC SHA \_ \_ P521<br/> | Sì<br/>    | ECDH \_ P521<br/> | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 128 \_ CBC SHA \_ \_ P256<br/>   | Sì<br/>    | ECDH \_ P256<br/> | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 128 \_ CBC SHA \_ \_ P384<br/>   | Sì<br/>    | ECDH \_ P384<br/> | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 128 \_ CBC SHA \_ \_ P521<br/>   | Sì<br/>    | ECDH \_ P521<br/> | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 256 \_ CBC SHA \_ \_ P256<br/>   | Sì<br/>    | ECDH \_ P256<br/> | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 256 \_ CBC SHA \_ \_ P384<br/>   | Sì<br/>    | ECDH \_ P384<br/> | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 256 \_ CBC SHA \_ \_ P521<br/>   | Sì<br/>    | ECDH \_ P521<br/> | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ DSS \_ CON \_ AES \_ 128 \_ CBC \_ SHA<br/>           | Sì<br/>    | Dh<br/>         | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ DSS \_ CON \_ AES \_ 256 \_ CBC \_ SHA<br/>           | Sì<br/>    | Dh<br/>         | AES<br/>  | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ DSS \_ CON \_ 3DES \_ EDE \_ CBC \_ SHA<br/>          | Sì<br/>    | Dh<br/>         | 3DES<br/> | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ CON \_ RC4 \_ 128 \_ MD5<br/>                     | No<br/>     | RSA<br/>        | RC4<br/>  | MD5<br/>  | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| SSL \_ CK \_ RC4 \_ 128 \_ CON \_ MD5<br/>                      | No<br/>     | RSA<br/>        | RC4<br/>  | MD5<br/>  | SSL 2.0<br/>          |
| SSL \_ CK \_ DES \_ 192 \_ EDE3 \_ CBC CON \_ \_ MD5<br/>           | No<br/>     | RSA<br/>        | 3DES<br/> | MD5<br/>  | SSL 2.0<br/>          |
| TLS \_ RSA \_ CON \_ \_ MD5 NULL<br/>                         | No<br/>     | RSA<br/>        |                 | MD5<br/>  | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA CON SHA \_ \_ \_ NULL<br/>                         | No<br/>     | RSA<br/>        |                 | SHA1<br/> | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |



 

Le suite di crittografia seguenti sono supportate da Schannel. tuttavia, non sono presenti per impostazione predefinita. Devono essere aggiunti in base alle esigenze. Per informazioni su come aggiungere suite di crittografia al provider Schannel, vedere [Prioritizing Schannel Cipher Suites](prioritizing-schannel-cipher-suites.md).

-   ESPORTAZIONE \_ RSA TLS CON \_ \_ \_ RC4 \_ 40 \_ MD5
-   TLS \_ RSA \_ EXPORT1024 \_ CON \_ RC4 \_ 56 \_ SHA
-   TLS \_ RSA \_ EXPORT1024 \_ CON DES \_ \_ CBC \_ SHA
-   SSL \_ CK \_ RC4 \_ 128 \_ EXPORT40 \_ MD5
-   SSL \_ CK \_ DES \_ 64 \_ CBC CON \_ \_ MD5
-   TLS \_ RSA CON DES \_ \_ \_ CBC \_ SHA
-   TLS \_ RSA \_ CON \_ \_ MD5 NULL
-   TLS \_ RSA CON SHA \_ \_ \_ NULL
-   TLS \_ \_ DSS \_ EXPORT1024 \_ CON DES \_ \_ CBC \_ SHA
-   \_ \_ DSS TLS DHE CON DES \_ \_ \_ CBC \_ SHA

**Windows Server 2003 e Windows XP:** Per informazioni sui pacchetti di crittografia supportati, vedere gli argomenti seguenti.

| Argomento                                                                         | Descrizione                                                                                                                        |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [Pacchetti di crittografia TLS](tls-cipher-suites.md)<br/>                         | Informazioni sulle suite di crittografia disponibili con il protocollo TLS in Windows Server 2003 e Windows XP.<br/>              |
| [Secure Sockets Layer protocollo](secure-sockets-layer-protocol.md)<br/> | Informazioni generali su SSL 2.0 e 3.0, incluse le suite di crittografia disponibili in Windows Server 2003 e Windows XP.<br/> |



 

 

 
