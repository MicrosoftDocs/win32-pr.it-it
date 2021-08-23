---
description: Informazioni sui pacchetti di crittografia TLS in Windows 10 v1703. I pacchetti di crittografia possono essere negoziati solo per le versioni TLS che le supportano.
ms.assetid: 2933DE68-E14B-48F9-8F31-49529BC883D6
title: Pacchetti di crittografia TLS in Windows 10 v1703
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfa0b3760006b4f960be99d9d840a62d82dc68adf669d855ea3d6fbb3ea49470
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118916170"
---
# <a name="tls-cipher-suites-in-windows-10-v1703"></a>Pacchetti di crittografia TLS in Windows 10 v1703

I pacchetti di crittografia possono essere negoziati solo per le versioni TLS che le supportano. La versione più recente supportata di TLS è sempre preferibile nell'handshake TLS.

La disponibilità dei pacchetti di crittografia deve essere controllata in uno dei due modi seguenti:

-   L'ordine di priorità predefinito viene sostituito quando viene configurato un elenco di priorità. I pacchetti di crittografia non presenti nell'elenco di priorità non verranno usati.
-   Consentito quando l'applicazione supera SCH USE STRONG CRYPTO: il provider Microsoft Schannel filtra i pacchetti di crittografia deboli noti quando l'applicazione usa il \_ flag SCH USE STRONG \_ \_ \_ \_ \_ CRYPTO. In Windows 10, la versione 1703, oltre alla versione RC4, i pacchetti di crittografia DES, export e Null vengono filtrati.

> [!IMPORTANT]
> I servizi Web HTTP/2 hanno esito negativo con pacchetti di crittografia non compatibili con HTTP/2. Per assicurarsi che i servizi Web funzionino con client e browser HTTP/2, vedere Come distribuire l'ordinamento dei [pacchetti di crittografia personalizzati.](https://support.microsoft.com/help/4032720/how-to-deploy-custom-cipher-suite-ordering-in-windows-server-2016)

 

La conformità FIPS è diventata più complessa con l'aggiunta di curve ellittiche che rende fuorviante la colonna abilitata per la modalità FIPS nelle versioni precedenti di questa tabella. Ad esempio, un pacchetto di crittografia come TLS \_ ECDHE \_ RSA \_ WITH \_ AES \_ 128 \_ CBC SHA256 è solo \_ fips-complaint quando si usano curve ellittiche NIST. Per scoprire quali combinazioni di curve ellittiche e pacchetti di crittografia verranno abilitati in modalità FIPS, vedere la sezione 3.3.1 di Linee guida per la selezione, la configurazione e l'uso delle implementazioni [TLS.]( https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-52r1.pdf)

Per Windows 10 versione 1703, i pacchetti di crittografia seguenti sono abilitati e in questo ordine di priorità per impostazione predefinita tramite il provider Microsoft Schannel:



| Stringa della suite di crittografia                                                                                 | Consentito da SCH \_ USE \_ STRONG \_ CRYPTO | Versioni del protocollo TLS/SSL                     |
|-----------------------------------------------------------------------------------------------------|-------------------------------------|-----------------------------------------------|
| TLS \_ ECDHE \_ ECDSA \_ CON \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                           | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ \_ ECDSA \_ CON \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                           | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                             | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                             | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ RSA CON \_ \_ \_ \_ \_ SHA384 AES 256 GCM<br/>                                               | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ RSA CON \_ \_ \_ SHA256 AES 128 \_ GCM \_<br/>                                               | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ CON \_ AES \_ 256 \_ CBC \_ SHA384<br/>                                           | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ CON \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                           | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 256 \_ CBC \_ SHA384<br/>                                             | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                             | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ CON \_ AES \_ 256 \_ CBC \_ SHA<br/>                                              | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ CON \_ AES \_ 128 \_ CBC \_ SHA<br/>                                              | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ RSA \_ CON \_ \_ \_ \_ SHA384 AES 256 GCM<br/>                                                    | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ CON \_ SHA256 AES \_ 128 \_ GCM \_<br/>                                                    | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ CON \_ AES \_ 256 \_ CBC \_ SHA256<br/>                                                    | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ CON \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                                    | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ CON \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                       | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ RSA \_ CON \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                       | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ RSA \_ CON \_ 3DES \_ EDE \_ CBC \_ SHA<br/>                                                      | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ RSA \_ CON \_ RC4 \_ 128 \_ SHA<br/>                                                            | No<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ CON \_ RC4 \_ 128 \_ MD5<br/>                                                            | No<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ CON \_ \_ SHA256 NULL <br/> Usato solo quando l'applicazione richiede in modo esplicito.<br/> | No<br/>                       | TLS 1.2<br/>                            |
| TLS \_ RSA CON SHA \_ \_ \_ NULL <br/> Usato solo quando l'applicazione richiede in modo esplicito.<br/>    | No<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |



 

I pacchetti di crittografia seguenti sono supportati dal provider Microsoft Schannel, ma non sono abilitati per impostazione predefinita:



| Stringa della suite di crittografia                                                                               | Consentito da SCH \_ USE \_ STRONG \_ CRYPTO | Versioni del protocollo TLS/SSL                     |
|---------------------------------------------------------------------------------------------------|-------------------------------------|-----------------------------------------------|
| TLS \_ DHE \_ RSA CON \_ \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ RSA CON \_ \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| \_ \_ DSS TLS DHE CON \_ \_ AES \_ 256 \_ CBC \_ SHA256<br/>                                             | Sì<br/>                      | TLS 1.2<br/>                            |
| \_ \_ DSS TLS DHE CON \_ \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                             | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ DSS \_ CON \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ DSS \_ CON \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ DSS \_ CON \_ 3DES \_ EDE \_ CBC \_ SHA<br/>                                               | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA CON DES \_ \_ \_ CBC \_ SHA<br/>                                                          | No<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| \_ \_ DSS TLS DHE CON DES \_ \_ \_ CBC \_ SHA<br/>                                                     | No<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ \_ DSS \_ EXPORT1024 \_ WITH DES \_ \_ CBC SHA No TLS \_ 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/>   | No<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ CON \_ \_ MD5 NULL <br/> Usato solo quando l'applicazione richiede in modo esplicito. <br/> | No<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ EXPORT1024 \_ CON \_ RC4 \_ 56 \_ SHA<br/>                                               | No<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| ESPORTAZIONE \_ RSA TLS CON \_ \_ \_ RC4 \_ 40 \_ MD5<br/>                                                   | No<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ EXPORT1024 \_ CON DES \_ \_ CBC \_ SHA<br/>                                              | No<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |



 

Le suite di crittografia PSK seguenti sono abilitate e in questo ordine di priorità per impostazione predefinita tramite il provider Microsoft Schannel:



| Stringa della suite di crittografia                              | Consentito da SCH \_ USE \_ STRONG \_ CRYPTO | Versioni del protocollo TLS/SSL |
|--------------------------------------------------|-------------------------------------|---------------------------|
| TLS \_ PSK \_ CON \_ AES \_ 256 \_ GCM \_ SHA384<br/> | Sì<br/>                      | TLS 1.2<br/>        |
| TLS \_ PSK \_ CON \_ AES \_ 128 \_ GCM \_ SHA256<br/> | Sì<br/>                      | TLS 1.2<br/>        |
| TLS \_ PSK \_ CON \_ AES \_ 256 \_ CBC \_ SHA384<br/> | Sì<br/>                      | TLS 1.2<br/>        |
| TLS \_ PSK \_ CON \_ AES \_ 128 \_ CBC \_ SHA256<br/> | Sì<br/>                      | TLS 1.2<br/>        |
| TLS \_ PSK \_ CON \_ \_ SHA384 NULL<br/>          | No<br/>                       | TLS 1.2<br/>        |
| TLS \_ PSK \_ CON \_ \_ SHA256 NULL<br/>          | No<br/>                       | TLS 1.2<br/>        |



 

> [!Note]  
> Nessuna suite di crittografia PSK è abilitata per impostazione predefinita. Le applicazioni devono richiedere PSK usando SCH \_ USE \_ PRESHAREDKEY \_ ONLY. Per altre informazioni sui flag Schannel, vedere [**SCHANNEL \_ CRED**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred).

 

Per aggiungere suite di crittografia, distribuire criteri di gruppo o usare i cmdlet TLS:

-   Per usare i criteri di gruppo, configurare SSL Cipher Suite Order in Configurazione computer > Modelli amministrativi > Rete > Configurazione SSL Impostazioni con l'elenco di priorità per tutte le suite di crittografia che si desidera sia abilitato.
-   Per usare PowerShell, vedere [Cmdlet TLS](/powershell/module/tls/?view=win10-ps).

> [!Note]  
> Prima di Windows 10, le stringhe del gruppo di crittografia venivano aggiunte con la curva ellittica per determinare la priorità della curva. Windows 10 supporta un'impostazione dell'ordine di priorità della curva ellittica in modo che il suffisso della curva ellittica non sia obbligatorio e venga sostituito dal nuovo ordine di priorità della curva ellittica, se specificato, per consentire alle organizzazioni di usare criteri di gruppo per configurare versioni diverse di Windows con gli stessi gruppi di crittografia.

 

 

 
