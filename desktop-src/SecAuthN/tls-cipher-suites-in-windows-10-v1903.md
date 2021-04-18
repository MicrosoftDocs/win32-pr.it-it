---
description: I pacchetti di crittografia possono essere negoziati solo per le versioni TLS che li supportano. La versione più elevata supportata di TLS è sempre preferita nell'handshake TLS.
title: Pacchetti di crittografia TLS in Windows 10 V1903, v1909 e v2004
ms.topic: article
ms.date: 10/09/2018
ms.openlocfilehash: 40694a961d9b7b97377037cb38be1b85a05f8a63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305859"
---
# <a name="tls-cipher-suites-in-windows-10-v1903-v1909-and-v2004"></a>Pacchetti di crittografia TLS in Windows 10 V1903, v1909 e v2004

I pacchetti di crittografia possono essere negoziati solo per le versioni TLS che li supportano. La versione più elevata supportata di TLS è sempre preferita nell'handshake TLS.

La disponibilità dei pacchetti di crittografia deve essere controllata in uno dei due modi seguenti:

-   L'ordine di priorità predefinito viene sostituito quando viene configurato un elenco di priorità. I pacchetti di crittografia non presenti nell'elenco di priorità non verranno utilizzati.
-   Consentito quando l'applicazione passa SCH \_ Usa \_ \_ crittografia avanzata: il provider Microsoft Schannel filtra i pacchetti di crittografia vulnerabili noti quando l'applicazione usa il \_ flag di \_ crittografia con utilizzo sicuro SCH \_ . I pacchetti RC4, DES, export e null sono esclusi.

> [!IMPORTANT]
> I servizi Web HTTP/2 hanno esito negativo con pacchetti di crittografia compatibili con non HTTP/2. Per garantire la funzione dei servizi Web con client e browser HTTP/2, vedere [How to deploy Custom Cipher Suite ordering](https://support.microsoft.com/help/4032720/how-to-deploy-custom-cipher-suite-ordering-in-windows-server-2016).

 

FIPS-Compliance è diventato più complesso con l'aggiunta di curve ellittiche che rendono la colonna abilitata per la modalità FIPS nelle versioni precedenti di questa tabella fuorviante. Ad esempio, un pacchetto di crittografia come TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 128 \_ CBC \_ SHA256 è solo un reclamo FIPS quando si usano le curve ellittiche del NIST. Per individuare le combinazioni di curve ellittiche e di pacchetti di crittografia che verranno abilitate in modalità FIPS, vedere la sezione 3.3.1 delle [linee guida per la selezione, la configurazione e l'uso delle implementazioni di TLS]( https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-52r2.pdf).

Per Windows 10, versione 1903, 1909 e 2004, i pacchetti di crittografia seguenti sono abilitati e in questo ordine di priorità per impostazione predefinita tramite il provider Microsoft Schannel:



| Stringa del pacchetto di crittografia                                                                                 | Consentito da SCH \_ usare \_ la \_ crittografia avanzata | Versioni del protocollo TLS/SSL                     |
|-----------------------------------------------------------------------------------------------------|-------------------------------------|-----------------------------------------------|
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                           | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                           | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                             | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                             | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ dhe \_ RSA \_ con \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                               | No<br/>                      | TLS 1.2<br/>                            |
| TLS \_ dhe \_ RSA \_ con \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                               | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 256 \_ CBC \_ SHA384<br/>                                           | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                           | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 256 \_ CBC \_ SHA384<br/>                                             | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                             | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 256 \_ CBC \_ Sha<br/>                                              | Sì<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ con \_ AES \_ 128 \_ CBC \_ Sha<br/>                                              | Sì<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 256 \_ CBC \_ Sha<br/>                                                | Sì<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ ECDHE \_ RSA \_ con \_ AES \_ 128 \_ CBC \_ Sha<br/>                                                | Sì<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ RSA \_ con \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                                    | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ con \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                                    | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ con \_ AES \_ 256 \_ CBC \_ SHA256<br/>                                                    | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ con \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                                    | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ con \_ \_ SHA AES 256 \_ CBC \_<br/>                                                       | Sì<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ RSA \_ con \_ \_ SHA AES 128 \_ CBC \_<br/>                                                       | Sì<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ RSA \_ con \_ \_ Sha Ede per la \_ CBC \_<br/>                                                      | Sì<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ RSA \_ con \_ \_ SHA256 null <br/> Usato solo quando l'applicazione richiede in modo esplicito.<br/> | No<br/>                       | TLS 1.2<br/>                            |
| TLS \_ RSA \_ con \_ \_ Sha null <br/> Usato solo quando l'applicazione richiede in modo esplicito.<br/>    | No<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |



 

I pacchetti di crittografia seguenti sono supportati dal provider Microsoft Schannel, ma non sono abilitati per impostazione predefinita:



| Stringa del pacchetto di crittografia                                                                               | Consentito da SCH \_ usare \_ la \_ crittografia avanzata | Versioni del protocollo TLS/SSL                     |
|---------------------------------------------------------------------------------------------------|-------------------------------------|-----------------------------------------------|
| TLS \_ dhe \_ RSA \_ con \_ AES \_ 256 \_ CBC \_ Sha<br/>                                                | Sì<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ dhe \_ RSA \_ con \_ AES \_ 128 \_ CBC \_ Sha<br/>                                                | Sì<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ dhe \_ DSS \_ con \_ AES \_ 256 \_ CBC \_ SHA256<br/>                                             | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ dhe \_ DSS \_ con \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                             | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ dhe \_ DSS \_ con \_ AES \_ 256 \_ CBC \_ Sha<br/>                                                | Sì<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ dhe \_ DSS \_ con \_ AES \_ 128 \_ CBC \_ Sha<br/>                                                | Sì<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0<br/>          |
| TLS \_ dhe \_ DSS \_ with \_ 3DES \_ Ede \_ CBC \_ Sha<br/>                                               | Sì<br/>                      | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ con \_ l' \_ Sha 128 RC4 \_<br/>                                                          | No<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ con \_ RC4 \_ 128 \_ MD5<br/>                                                          | No<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ con \_ \_ Sha des CBC \_<br/>                                                          | No<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ dhe \_ DSS \_ con \_ des \_ CBC \_ Sha<br/>                                                     | No<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ dhe \_ DSS \_ EXPORT1024 \_ con \_ DES \_ CBC \_ Sha no tls 1,2, tls 1,1, TLS 1,0, SSL 3,0<br/>   | No<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| \_RSA TLS \_ con \_ \_ MD5 null <br/> Usato solo quando l'applicazione richiede in modo esplicito. <br/> | No<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ EXPORT1024 \_ con la versione \_ RC4 \_ 56 \_ Sha<br/>                                               | No<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| \_Esportazione RSA \_ TLS \_ con \_ RC4 \_ 40 \_ MD5<br/>                                                   | No<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |
| TLS \_ RSA \_ EXPORT1024 \_ con \_ des \_ CBC \_ Sha<br/>                                              | No<br/>                       | TLS 1,2, TLS 1,1, TLS 1,0, SSL 3,0<br/> |



 

Per impostazione predefinita, i pacchetti di crittografia PSK seguenti sono abilitati e in questo ordine di priorità utilizzando il provider Microsoft Schannel:



| Stringa del pacchetto di crittografia                              | Consentito da SCH \_ usare \_ la \_ crittografia avanzata | Versioni del protocollo TLS/SSL |
|--------------------------------------------------|-------------------------------------|---------------------------|
| TLS \_ PSK \_ con \_ AES \_ 256 \_ GCM \_ SHA384<br/> | Sì<br/>                      | TLS 1.2<br/>        |
| TLS \_ PSK \_ con \_ AES \_ 128 \_ GCM \_ SHA256<br/> | Sì<br/>                      | TLS 1.2<br/>        |
| TLS \_ PSK \_ con \_ AES \_ 256 \_ CBC \_ SHA384<br/> | Sì<br/>                      | TLS 1.2<br/>        |
| TLS \_ PSK \_ con \_ AES \_ 128 \_ CBC \_ SHA256<br/> | Sì<br/>                      | TLS 1.2<br/>        |
| \_PSK TLS \_ con \_ \_ SHA384 null<br/>          | No<br/>                       | TLS 1.2<br/>        |
| \_PSK TLS \_ con \_ \_ SHA256 null<br/>          | No<br/>                       | TLS 1.2<br/>        |



 

> [!Note]  
> Nessun pacchetto di crittografia PSK è abilitato per impostazione predefinita. Le applicazioni devono richiedere la PSK usando \_ sch \_ usare \_ solo PRESHAREDKEY. Per ulteriori informazioni sui flag Schannel, vedere [**Schannel \_ cred**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred).

 

Per aggiungere pacchetti di crittografia, distribuire un criterio di gruppo o usare i cmdlet di TLS:

-   Per usare criteri di gruppo, configurare l'ordine dei pacchetti di crittografia SSL in configurazione computer > Modelli amministrativi > rete > impostazioni di configurazione SSL con l'elenco di priorità per tutti i pacchetti di crittografia che si vuole abilitare.
-   Per usare PowerShell, vedere [cmdlet TLS](/powershell/module/tls/?view=win10-ps).

> [!Note]  
> Prima di Windows 10, le stringhe del pacchetto di crittografia venivano aggiunte con la curva ellittica per determinare la priorità della curva. Windows 10 supporta un'impostazione dell'ordine di priorità a curva ellittica, quindi il suffisso della curva ellittica non è obbligatorio e viene sostituito dal nuovo ordine di priorità della curva ellittica, se specificato, per consentire alle organizzazioni di utilizzare criteri di gruppo per configurare versioni diverse di Windows con gli stessi pacchetti di crittografia.
