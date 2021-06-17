---
description: Informazioni sulle suite di crittografia TLS in Windows 8. Le suite di crittografia possono essere negoziate solo per le versioni TLS che le supportano.
ms.assetid: F37C3596-E273-4144-87B9-D589EBB82C0B
title: Pacchetti di crittografia TLS in Windows 8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a204fabb91ddafc6b4d55c10b58503b4b81ca45
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262353"
---
# <a name="tls-cipher-suites-in-windows-8"></a>Pacchetti di crittografia TLS in Windows 8

Le suite di crittografia possono essere negoziate solo per le versioni TLS che le supportano. La versione TLS più alta supportata è sempre preferibile nell'handshake TLS. Ad esempio, SSL CK RC4 128 WITH MD5 può essere usato solo quando il client e il server non supportano \_ \_ TLS \_ \_ \_ 1.2, 1.1 & 1.0 o SSL 3.0 perché è supportato solo con SSL 2.0.

La disponibilità dei pacchetti di crittografia deve essere controllata in uno dei due modi seguenti:

-   L'ordine di priorità predefinito viene sostituito quando viene configurato un elenco di priorità. I pacchetti di crittografia non presenti nell'elenco di priorità non verranno usati.
-   Consentito quando l'applicazione passa SCH USE STRONG CRYPTO: il provider Microsoft Schannel filtra i pacchetti di crittografia deboli noti quando l'applicazione usa il \_ flag SCH USE STRONG \_ \_ \_ \_ \_ CRYPTO. In Windows 8, le suite di crittografia RC4 vengono filtrate.

> [!IMPORTANT]
> I servizi Web HTTP/2 hanno esito negativo con suite di crittografia non compatibili con HTTP/2. Per assicurarsi che i servizi Web funzionino con client e browser HTTP/2, vedere Come distribuire l'ordinamento dei [pacchetti di crittografia personalizzati.](https://support.microsoft.com/help/4032720/how-to-deploy-custom-cipher-suite-ordering-in-windows-server-2016)

 

La conformità FIPS è diventata più complessa con l'aggiunta di curve ellittiche che rende fuorviante la colonna abilitata per la modalità FIPS nelle versioni precedenti di questa tabella. Ad esempio, una suite di crittografia come TLS \_ ECDHE \_ RSA \_ WITH \_ AES \_ 128 \_ CBC \_ SHA256 è solo un reclamo FIPS quando si usano curve ellittiche NIST. Per scoprire quali combinazioni di curve ellittiche e suite di crittografia verranno abilitate in modalità FIPS, vedere la sezione 3.3.1 delle linee guida per la selezione, la configurazione e l'uso delle implementazioni [TLS.]( https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-52r1.pdf)

Windows 7, Windows 8 e Windows Server 2012 vengono aggiornati dal Windows Update dall'aggiornamento 3042058 che modifica l'ordine di priorità. Per altre informazioni, vedere l'advisory microsoft sulla sicurezza [3042058.](/security-updates/SecurityAdvisories/2015/3042058) Le suite di crittografia seguenti sono abilitate e in questo ordine di priorità per impostazione predefinita dal provider Microsoft Schannel:



| Stringa della suite di crittografia                                                                                            | Consentito da SCH \_ USE \_ STRONG \_ CRYPTO | Versioni del protocollo TLS/SSL                     |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------|-----------------------------------------------|
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 256 \_ CBC \_ SHA384 \_ P256<br/>                                                  | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 256 \_ CBC \_ SHA384 \_ P384<br/>                                                  | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 128 \_ CBC \_ SHA256 \_ P256<br/>                                                  | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 128 \_ CBC \_ SHA256 \_ P384<br/>                                                  | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 256 \_ CBC SHA \_ \_ P256<br/>                                                     | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 256 \_ CBC SHA \_ \_ P384<br/>                                                     | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 128 \_ CBC SHA \_ \_ P256<br/>                                                     | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 128 \_ CBC SHA \_ \_ P384<br/>                                                     | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ RSA CON \_ \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                                          | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ RSA CON \_ \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                                          | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ CON \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                                               | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ CON \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                                               | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ CON \_ AES \_ 256 \_ CBC \_ SHA256<br/>                                                               | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ CON \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                                               | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ CON \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                                  | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ RSA \_ CON \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                                  | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ CON \_ AES \_ 256 \_ GCM \_ SHA384 \_ P384<br/>                                                | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ CON \_ AES \_ 128 \_ GCM \_ SHA256 \_ P256<br/>                                                | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ CON \_ AES \_ 128 \_ GCM \_ SHA256 \_ P384<br/>                                                | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ CON \_ AES \_ 256 \_ CBC \_ SHA384 \_ P384<br/>                                                | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ CON \_ AES \_ 128 \_ CBC \_ SHA256 \_ P256<br/>                                                | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ CON \_ AES \_ 128 \_ CBC \_ SHA256 \_ P384<br/>                                                | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ CON \_ AES \_ 256 \_ CBC SHA \_ \_ P256<br/>                                                   | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ CON \_ AES \_ 256 \_ CBC SHA \_ \_ P384<br/>                                                   | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ CON \_ AES \_ 128 \_ CBC SHA \_ \_ P256<br/>                                                   | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ CON \_ AES \_ 128 \_ CBC SHA \_ \_ P384<br/>                                                   | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| \_ \_ DSS TLS DHE CON \_ \_ AES \_ 256 \_ CBC \_ SHA256<br/>                                                          | Sì<br/>                      | TLS 1.2<br/>                            |
| \_ \_ DSS TLS DHE CON \_ \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                                          | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ DSS \_ CON \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                             | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ DSS \_ CON \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                             | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ RSA \_ CON \_ 3DES \_ EDE \_ CBC \_ SHA<br/>                                                                 | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ DSS \_ CON \_ 3DES \_ EDE \_ CBC \_ SHA<br/>                                                            | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ CON \_ RC4 \_ 128 \_ SHA<br/>                                                                       | No<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ CON \_ RC4 \_ 128 \_ MD5<br/>                                                                       | No<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ CON \_ \_ SHA256 NULL <br/> Usato solo quando l'applicazione richiede in modo esplicito.<br/>            | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA CON SHA \_ \_ \_ NULL <br/> Usato solo quando l'applicazione richiede in modo esplicito.<br/>               | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| SSL \_ CK \_ RC4 \_ 128 \_ CON \_ MD5 <br/> Usato solo quando l'applicazione richiede in modo esplicito.<br/>            | No<br/>                       | SSL 2.0<br/>                            |
| SSL \_ CK \_ DES \_ 192 \_ EDE3 \_ CBC CON \_ \_ MD5 <br/> Usato solo quando l'applicazione richiede in modo esplicito.<br/> | Sì<br/>                      | SSL 2.0<br/>                            |



 

Le suite di crittografia seguenti sono supportate dal provider Microsoft Schannel, ma non abilitate per impostazione predefinita:



| Stringa della suite di crittografia                                             | Consentito da SCH \_ USE \_ STRONG \_ CRYPTO | Versioni del protocollo TLS/SSL                     |
|-----------------------------------------------------------------|-------------------------------------|-----------------------------------------------|
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 256 \_ CBC \_ SHA384 \_ P521<br/>   | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 128 \_ CBC \_ SHA256 \_ P521<br/>   | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 256 \_ CBC SHA \_ \_ P521<br/>      | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 128 \_ CBC SHA \_ \_ P521<br/>      | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ CON \_ AES \_ 256 \_ GCM \_ SHA384 \_ P521<br/> | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ CON \_ AES \_ 128 \_ GCM \_ SHA256 \_ P521<br/> | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ CON \_ AES \_ 256 \_ CBC \_ SHA384 \_ P521<br/> | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ CON \_ AES \_ 128 \_ CBC \_ SHA256 \_ P521<br/> | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ CON \_ AES \_ 256 \_ CBC SHA \_ \_ P521<br/>    | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ CON \_ AES \_ 128 \_ CBC SHA \_ \_ P521<br/>    | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ RSA CON DES \_ \_ \_ CBC \_ SHA<br/>                        | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ EXPORT1024 \_ CON \_ RC4 \_ 56 \_ SHA<br/>             | No<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ EXPORT1024 \_ CON DES \_ \_ CBC \_ SHA<br/>            | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| ESPORTAZIONE \_ RSA TLS CON \_ \_ \_ RC4 \_ 40 \_ MD5<br/>                 | No<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ CON \_ \_ MD5 NULL<br/>                            | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| \_ \_ DSS TLS DHE CON DES \_ \_ \_ CBC \_ SHA<br/>                   | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ \_ DSS \_ EXPORT1024 \_ CON DES \_ \_ CBC \_ SHA<br/>       | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| SSL \_ CK \_ DES \_ 64 \_ CBC CON \_ \_ MD5<br/>                     | Sì<br/>                      | SSL 2.0<br/>                            |
| SSL \_ CK \_ RC4 \_ 128 \_ EXPORT40 \_ CON \_ MD5<br/>               | No<br/>                       | SSL 2.0<br/>                            |



 

Per aggiungere pacchetti di crittografia, usare l'impostazione di criteri di gruppo SSL Cipher Suite Order in Configurazione computer > Modelli amministrativi > Rete > Impostazioni di configurazione SSL per configurare un elenco di priorità per tutti i pacchetti di crittografia che si desidera sia abilitato.

 

 
