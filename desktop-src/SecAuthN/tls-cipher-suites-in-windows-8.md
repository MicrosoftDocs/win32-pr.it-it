---
description: I pacchetti di crittografia possono essere negoziati solo per le versioni TLS che li supportano.
ms.assetid: F37C3596-E273-4144-87B9-D589EBB82C0B
title: Pacchetti di crittografia TLS in Windows 8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8613c018857525f7877e883f21b1eea7bd53e55a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884093"
---
# <a name="tls-cipher-suites-in-windows-8"></a>Pacchetti di crittografia TLS in Windows 8

I pacchetti di crittografia possono essere negoziati solo per le versioni TLS che li supportano. La versione più elevata supportata di TLS è sempre preferita nell'handshake TLS. Ad esempio, SSL \_ CK \_ RC4 \_ 128 \_ con \_ MD5 può essere usato solo quando il client e il server non supportano TLS 1,2, 1,1 & 1,0 o SSL 3,0 perché è supportato solo con SSL 2,0.

La disponibilità dei pacchetti di crittografia deve essere controllata in uno dei due modi seguenti:

-   L'ordine di priorità predefinito viene sostituito quando viene configurato un elenco di priorità. I pacchetti di crittografia non presenti nell'elenco di priorità non verranno utilizzati.
-   Consentito quando l'applicazione passa \_ sch \_ Usa \_ crittografia avanzata: il provider Microsoft Schannel filtra i pacchetti di crittografia vulnerabili noti quando l'applicazione usa il flag di crittografia per l'uso di SCH \_ \_ \_ . In Windows 8, i pacchetti di crittografia RC4 vengono esclusi.

> [!IMPORTANT]
> I servizi Web HTTP/2 hanno esito negativo con pacchetti di crittografia compatibili con non HTTP/2. Per garantire la funzione dei servizi Web con client e browser HTTP/2, vedere [How to deploy Custom Cipher Suite ordering](https://support.microsoft.com/help/4032720/how-to-deploy-custom-cipher-suite-ordering-in-windows-server-2016).

 

FIPS-Compliance è diventato più complesso con l'aggiunta di curve ellittiche che rendono la colonna abilitata per la modalità FIPS nelle versioni precedenti di questa tabella fuorviante. Ad esempio, un pacchetto di crittografia come TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 128 \_ CBC \_ SHA256 è solo un reclamo FIPS quando si usano le curve ellittiche del NIST. Per individuare le combinazioni di curve ellittiche e di pacchetti di crittografia che verranno abilitate in modalità FIPS, vedere la sezione 3.3.1 delle [linee guida per la selezione, la configurazione e l'uso delle implementazioni di TLS]( https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-52r1.pdf).

Windows 7, Windows 8 e Windows Server 2012 vengono aggiornati dal Windows Update dall'aggiornamento 3042058 che modifica l'ordine di priorità. Per ulteriori informazioni, vedere l' [avviso di sicurezza Microsoft 3042058](/security-updates/SecurityAdvisories/2015/3042058) . Per impostazione predefinita, i pacchetti di crittografia seguenti sono abilitati e in questo ordine di priorità dal provider Microsoft Schannel:



| Stringa del pacchetto di crittografia                                                                                            | Consentito da SCH \_ usare \_ la \_ crittografia avanzata | Versioni del protocollo TLS/SSL                     |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------|-----------------------------------------------|
| TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 256 \_ CBC \_ SHA384 \_ P256<br/>                                                  | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 256 \_ CBC \_ SHA384 \_ p384<br/>                                                  | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 128 \_ CBC \_ SHA256 \_ P256<br/>                                                  | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 128 \_ CBC \_ SHA256 \_ p384<br/>                                                  | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 256 \_ CBC \_ Sha \_ P256<br/>                                                     | Sì<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 256 \_ CBC \_ Sha \_ p384<br/>                                                     | Sì<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 128 \_ CBC \_ Sha \_ P256<br/>                                                     | Sì<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 128 \_ CBC \_ Sha \_ p384<br/>                                                     | Sì<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ dhe \_ RSA \_ con \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                                          | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ dhe \_ RSA \_ con \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                                          | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ con \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                                               | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ con \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                                               | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ con \_ AES \_ 256 \_ CBC \_ SHA256<br/>                                                               | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ con \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                                               | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ con \_ \_ SHA AES 256 \_ CBC \_<br/>                                                                  | Sì<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ RSA \_ con \_ \_ SHA AES 128 \_ CBC \_<br/>                                                                  | Sì<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 256 \_ GCM \_ SHA384 \_ p384<br/>                                                | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 128 \_ GCM \_ SHA256 \_ P256<br/>                                                | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 128 \_ GCM \_ SHA256 \_ p384<br/>                                                | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 256 \_ CBC \_ SHA384 \_ p384<br/>                                                | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 128 \_ CBC \_ SHA256 \_ P256<br/>                                                | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 128 \_ CBC \_ SHA256 \_ p384<br/>                                                | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 256 \_ CBC \_ Sha \_ P256<br/>                                                   | Sì<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 256 \_ CBC \_ Sha \_ p384<br/>                                                   | Sì<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 128 \_ CBC \_ Sha \_ P256<br/>                                                   | Sì<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 128 \_ CBC \_ Sha \_ p384<br/>                                                   | Sì<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ dhe \_ DSS \_ con \_ AES \_ 256 \_ CBC \_ SHA256<br/>                                                          | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ dhe \_ DSS \_ con \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                                          | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ dhe \_ DSS \_ con \_ AES \_ 256 \_ CBC \_ Sha<br/>                                                             | Sì<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ dhe \_ DSS \_ con \_ AES \_ 128 \_ CBC \_ Sha<br/>                                                             | Sì<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ RSA \_ con \_ \_ Sha Ede per la \_ CBC \_<br/>                                                                 | Sì<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ dhe \_ DSS \_ with \_ 3DES \_ Ede \_ CBC \_ Sha<br/>                                                            | Sì<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ con \_ l' \_ Sha 128 RC4 \_<br/>                                                                       | No<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ con \_ RC4 \_ 128 \_ MD5<br/>                                                                       | No<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ con \_ \_ SHA256 null <br/> Usato solo quando l'applicazione richiede in modo esplicito.<br/>            | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ con \_ \_ Sha null <br/> Usato solo quando l'applicazione richiede in modo esplicito.<br/>               | Sì<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| SSL \_ CK \_ RC4 \_ 128 \_ con \_ MD5 <br/> Usato solo quando l'applicazione richiede in modo esplicito.<br/>            | No<br/>                       | SSL 2.0<br/>                            |
| SSL \_ CK \_ des \_ 192 \_ EDE3 \_ CBC \_ con \_ MD5 <br/> Usato solo quando l'applicazione richiede in modo esplicito.<br/> | Sì<br/>                      | SSL 2.0<br/>                            |



 

I pacchetti di crittografia seguenti sono supportati dal provider Microsoft Schannel, ma non sono abilitati per impostazione predefinita:



| Stringa del pacchetto di crittografia                                             | Consentito da SCH \_ usare \_ la \_ crittografia avanzata | Versioni del protocollo TLS/SSL                     |
|-----------------------------------------------------------------|-------------------------------------|-----------------------------------------------|
| TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 256 \_ CBC \_ SHA384 \_ P521<br/>   | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 128 \_ CBC \_ SHA256 \_ P521<br/>   | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 256 \_ CBC \_ Sha \_ P521<br/>      | Sì<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 128 \_ CBC \_ Sha \_ P521<br/>      | Sì<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 256 \_ GCM \_ SHA384 \_ P521<br/> | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 128 \_ GCM \_ SHA256 \_ P521<br/> | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 256 \_ CBC \_ SHA384 \_ P521<br/> | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 128 \_ CBC \_ SHA256 \_ P521<br/> | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 256 \_ CBC \_ Sha \_ P521<br/>    | Sì<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 128 \_ CBC \_ Sha \_ P521<br/>    | Sì<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ RSA \_ con \_ \_ Sha des CBC \_<br/>                        | Sì<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ EXPORT1024 \_ con la versione \_ RC4 \_ 56 \_ Sha<br/>             | No<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ EXPORT1024 \_ con \_ des \_ CBC \_ Sha<br/>            | Sì<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| \_Esportazione RSA \_ TLS \_ con \_ RC4 \_ 40 \_ MD5<br/>                 | No<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| \_RSA TLS \_ con \_ \_ MD5 null<br/>                            | Sì<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ dhe \_ DSS \_ con \_ des \_ CBC \_ Sha<br/>                   | Sì<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ dhe \_ DSS \_ EXPORT1024 \_ con \_ des \_ CBC \_ Sha<br/>       | Sì<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| SSL \_ CK \_ des \_ 64 \_ CBC \_ con \_ MD5<br/>                     | Sì<br/>                      | SSL 2.0<br/>                            |
| SSL \_ CK \_ RC4 \_ 128 \_ EXPORT40 \_ con \_ MD5<br/>               | No<br/>                       | SSL 2.0<br/>                            |



 

Per aggiungere pacchetti di crittografia, usare l'impostazione di criteri di gruppo ordine di crittografia SSL in configurazione computer > Modelli amministrativi > rete > impostazioni di configurazione SSL per configurare un elenco di priorità per tutti i pacchetti di crittografia che si vuole abilitare.

 

 
