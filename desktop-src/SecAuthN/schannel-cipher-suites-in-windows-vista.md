---
description: Set di algoritmi di crittografia. I protocolli Schannel usano gli algoritmi di un pacchetto di crittografia per creare chiavi e crittografare informazioni.
ms.assetid: 380452e2-a9c8-4380-a3bf-9c7942a0c0c2
title: Pacchetti di crittografia TLS in Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80cf270f0608666b7d766e3f063f24ea39204fd1
ms.sourcegitcommit: b022a50bc0d11975dad6337b8f399c47234dffcf
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "106320201"
---
# <a name="tls-cipher-suites-in-windows-vista"></a>Pacchetti di crittografia TLS in Windows Vista

Un pacchetto di crittografia è un set di algoritmi di crittografia. I protocolli Schannel usano gli algoritmi di un pacchetto di crittografia per creare chiavi e crittografare informazioni. Un pacchetto di crittografia specifica un algoritmo per ognuna delle attività seguenti:

-   Scambio di chiave
-   Crittografia di massa
-   Autenticazione dei messaggi

Gli [*algoritmi di scambio di chiave*](../secgloss/k-gly.md) proteggono le informazioni necessarie per creare chiavi condivise. Questi algoritmi sono asimmetrici ([*algoritmi a chiave pubblica*](../secgloss/p-gly.md)) ed eseguono prestazioni ottimali per quantità di dati relativamente ridotte.

Gli algoritmi di crittografia bulk crittografano i messaggi scambiati tra client e server. Questi algoritmi sono [*simmetrici*](../secgloss/s-gly.md) ed eseguono prestazioni ottimali per grandi quantità di dati.

Gli algoritmi di [autenticazione dei messaggi](message-authentication-codes-in-schannel.md) generano [*hash*](../secgloss/h-gly.md) e firme dei messaggi che assicurano l' [*integrità*](../secgloss/i-gly.md) di un messaggio.

Gli sviluppatori specificano questi elementi usando i tipi di dati di [**\_ ID ALG**](../seccrypto/alg-id.md) . Per altre informazioni, vedere [specifica delle crittografie Schannel e dei punti di forza di crittografia](specifying-schannel-ciphers-and-cipher-strengths.md).

Schannel supporta i pacchetti di crittografia seguenti. I gruppi sono elencati nell'ordine predefinito in cui vengono scelti dal provider Microsoft Schannel.

> [!IMPORTANT]
> I servizi Web HTTP/2 hanno esito negativo con pacchetti di crittografia compatibili con non HTTP/2. Per garantire la funzione dei servizi Web con client e browser HTTP/2, vedere [How to deploy Custom Cipher Suite ordering](https://support.microsoft.com/help/4032720/how-to-deploy-custom-cipher-suite-ordering-in-windows-server-2016).

 



| Pacchetto di crittografia                                                 | Modalità FIPS abilitata | Exchange              | Crittografia      | Hash            | Protocolli                   |
|--------------------------------------------------------------|-------------------|-----------------------|-----------------|-----------------|-----------------------------|
| TLS \_ RSA \_ con \_ \_ SHA AES 128 \_ CBC \_<br/>                | Sì<br/>    | RSA<br/>        | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ RSA \_ con \_ \_ SHA AES 256 \_ CBC \_<br/>                | Sì<br/>    | RSA<br/>        | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ RSA \_ con \_ l' \_ Sha 128 RC4 \_<br/>                     | No<br/>     | RSA<br/>        | RC4<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ con \_ \_ Sha Ede per la \_ CBC \_<br/>               | Sì<br/>    | RSA<br/>        | 3DES<br/> | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 128 \_ CBC \_ Sha \_ P256<br/> | Sì<br/>    | \_P256 ECDH<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 128 \_ CBC \_ Sha \_ p384<br/> | Sì<br/>    | \_P384 ECDH<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 128 \_ CBC \_ Sha \_ P521<br/> | Sì<br/>    | \_P521 ECDH<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 256 \_ CBC \_ Sha \_ P256<br/> | Sì<br/>    | \_P256 ECDH<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 256 \_ CBC \_ Sha \_ p384<br/> | Sì<br/>    | \_P384 ECDH<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 256 \_ CBC \_ Sha \_ P521<br/> | Sì<br/>    | \_P521 ECDH<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 128 \_ CBC \_ Sha \_ P256<br/>   | Sì<br/>    | \_P256 ECDH<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 128 \_ CBC \_ Sha \_ p384<br/>   | Sì<br/>    | \_P384 ECDH<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 128 \_ CBC \_ Sha \_ P521<br/>   | Sì<br/>    | \_P521 ECDH<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 256 \_ CBC \_ Sha \_ P256<br/>   | Sì<br/>    | \_P256 ECDH<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 256 \_ CBC \_ Sha \_ p384<br/>   | Sì<br/>    | \_P384 ECDH<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 256 \_ CBC \_ Sha \_ P521<br/>   | Sì<br/>    | \_P521 ECDH<br/> | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ dhe \_ DSS \_ con \_ AES \_ 128 \_ CBC \_ Sha<br/>           | Sì<br/>    | DH<br/>         | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ dhe \_ DSS \_ con \_ AES \_ 256 \_ CBC \_ Sha<br/>           | Sì<br/>    | DH<br/>         | AES<br/>  | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ dhe \_ DSS \_ with \_ 3DES \_ Ede \_ CBC \_ Sha<br/>          | Sì<br/>    | DH<br/>         | 3DES<br/> | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ con \_ RC4 \_ 128 \_ MD5<br/>                     | No<br/>     | RSA<br/>        | RC4<br/>  | MD5<br/>  | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| SSL \_ CK \_ RC4 \_ 128 \_ con \_ MD5<br/>                      | No<br/>     | RSA<br/>        | RC4<br/>  | MD5<br/>  | SSL 2.0<br/>          |
| SSL \_ CK \_ des \_ 192 \_ EDE3 \_ CBC \_ con \_ MD5<br/>           | No<br/>     | RSA<br/>        | 3DES<br/> | MD5<br/>  | SSL 2.0<br/>          |
| \_RSA TLS \_ con \_ \_ MD5 null<br/>                         | No<br/>     | RSA<br/>        |                 | MD5<br/>  | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ con \_ \_ Sha null<br/>                         | No<br/>     | RSA<br/>        |                 | SHA1<br/> | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |



 

I pacchetti di crittografia seguenti sono supportati da Schannel; Tuttavia, non sono presenti per impostazione predefinita. È necessario aggiungerli se necessario. Per informazioni su come aggiungere i pacchetti di crittografia al provider Schannel, vedere priorità dei pacchetti di [crittografia Schannel](prioritizing-schannel-cipher-suites.md).

-   \_Esportazione RSA \_ TLS \_ con \_ RC4 \_ 40 \_ MD5
-   TLS \_ RSA \_ EXPORT1024 \_ con la versione \_ RC4 \_ 56 \_ Sha
-   TLS \_ RSA \_ EXPORT1024 \_ con \_ des \_ CBC \_ Sha
-   SSL \_ CK \_ RC4 \_ 128 \_ EXPORT40 \_ MD5
-   SSL \_ CK \_ des \_ 64 \_ CBC \_ con \_ MD5
-   TLS \_ RSA \_ con \_ \_ Sha des CBC \_
-   \_RSA TLS \_ con \_ \_ MD5 null
-   TLS \_ RSA \_ con \_ \_ Sha null
-   TLS \_ dhe \_ DSS \_ EXPORT1024 \_ con \_ des \_ CBC \_ Sha
-   TLS \_ dhe \_ DSS \_ con \_ des \_ CBC \_ Sha

**Windows Server 2003 e Windows XP:** Per informazioni sui pacchetti di crittografia supportati, vedere gli argomenti seguenti.

| Argomento                                                                         | Descrizione                                                                                                                        |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [Pacchetti di crittografia TLS](tls-cipher-suites.md)<br/>                         | Informazioni sui pacchetti di crittografia disponibili con il protocollo TLS in Windows Server 2003 e Windows XP.<br/>              |
| [Protocollo Secure Sockets Layer](secure-sockets-layer-protocol.md)<br/> | Informazioni generali su SSL 2,0 e 3,0, inclusi i pacchetti di crittografia disponibili in Windows Server 2003 e Windows XP.<br/> |



 

 

 
