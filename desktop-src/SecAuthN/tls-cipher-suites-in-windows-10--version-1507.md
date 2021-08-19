---
description: Informazioni sulle suite di crittografia TLS in Windows 10 v1507. Le suite di crittografia possono essere negoziate solo per le versioni TLS che le supportano.
ms.assetid: 58A47273-D2D3-449D-891C-C9502012C557
title: Pacchetti di crittografia TLS in Windows 10 v1507
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8557647e09b1bd2cadf30472a87aac23ceefbc5c70c3a4ddbf094eacc4404871
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117786237"
---
# <a name="tls-cipher-suites-in-windows-10-v1507"></a>Pacchetti di crittografia TLS in Windows 10 v1507

Le suite di crittografia possono essere negoziate solo per le versioni TLS che le supportano. La versione TLS più alta supportata è sempre preferibile nell'handshake TLS. Ad esempio, SSL CK RC4 128 WITH MD5 può essere usato solo quando il client e il server non supportano \_ \_ TLS \_ \_ \_ 1.2, 1.1 & 1.0 o SSL 3.0 perché è supportato solo con SSL 2.0.

La disponibilità dei pacchetti di crittografia deve essere controllata in uno dei due modi seguenti:

-   L'ordine di priorità predefinito viene sostituito quando viene configurato un elenco di priorità. I pacchetti di crittografia non presenti nell'elenco di priorità non verranno usati.
-   Consentito quando l'applicazione passa SCH USE STRONG CRYPTO: il provider Microsoft Schannel filtra i pacchetti di crittografia deboli noti quando l'applicazione usa il \_ flag SCH USE STRONG \_ \_ \_ \_ \_ CRYPTO. In Windows 10, le suite di crittografia RC4 versione 1507 vengono filtrate.

> [!IMPORTANT]
> I servizi Web HTTP/2 hanno esito negativo con suite di crittografia non compatibili con HTTP/2. Per assicurarsi che i servizi Web funzionino con client e browser HTTP/2, vedere Come distribuire l'ordinamento di [pacchetti di crittografia personalizzati.](https://support.microsoft.com/help/4032720/how-to-deploy-custom-cipher-suite-ordering-in-windows-server-2016)

 

La conformità FIPS è diventata più complessa con l'aggiunta di curve ellittiche che rende fuorviante la colonna abilitata per la modalità FIPS nelle versioni precedenti di questa tabella. Ad esempio, una suite di crittografia come TLS \_ ECDHE \_ RSA \_ WITH \_ AES \_ 128 \_ CBC \_ SHA256 è solo un reclamo FIPS quando si usano curve ellittiche NIST. Per scoprire quali combinazioni di curve ellittiche e suite di crittografia verranno abilitate in modalità FIPS, vedere la sezione 3.3.1 delle linee guida per la selezione, la configurazione e l'uso delle implementazioni [TLS.]( https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-52r1.pdf)

Ad Windows 10, versione 1507, le suite di crittografia seguenti sono abilitate e in questo ordine di priorità per impostazione predefinita usando il provider Microsoft Schannel:



| Stringa della suite di crittografia                                                                                            | Consentito da SCH \_ USE \_ STRONG \_ CRYPTO | Versioni del protocollo TLS/SSL                     |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------|-----------------------------------------------|
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                                        | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                                        | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 256 \_ CBC \_ SHA384<br/>                                                        | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                                        | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                           | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ RSA CON \_ \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                           | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ RSA CON \_ \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                                          | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ RSA CON \_ \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                                          | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ RSA CON \_ \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                             | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ RSA CON \_ \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                             | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ RSA \_ CON \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                                               | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ CON \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                                               | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ CON \_ AES \_ 256 \_ CBC \_ SHA256<br/>                                                               | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ CON \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                                               | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA \_ CON \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                                  | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ RSA \_ CON \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                                  | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ CON \_ AES \_ 256 \_ GCM \_ SHA384<br/>                                                      | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ CON \_ AES \_ 128 \_ GCM \_ SHA256<br/>                                                      | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ CON \_ AES \_ 256 \_ CBC \_ SHA384<br/>                                                      | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ CON \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                                      | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ ECDHE \_ ECDSA \_ CON \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                         | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ ECDHE \_ ECDSA \_ CON \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                         | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| \_ \_ DSS TLS DHE CON \_ \_ AES \_ 256 \_ CBC \_ SHA256<br/>                                                          | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ DSS \_ CON \_ AES \_ 128 \_ CBC \_ SHA256<br/>                                                          | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ DHE \_ DSS \_ CON \_ AES \_ 256 \_ CBC \_ SHA<br/>                                                             | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ DSS \_ CON \_ AES \_ 128 \_ CBC \_ SHA<br/>                                                             | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ RSA \_ CON \_ 3DES \_ EDE \_ CBC \_ SHA<br/>                                                                 | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0<br/>          |
| TLS \_ DHE \_ DSS \_ CON \_ 3DES \_ EDE \_ CBC \_ SHA<br/>                                                            | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ CON \_ RC4 \_ 128 \_ SHA<br/>                                                                       | No<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ CON \_ RC4 \_ 128 \_ MD5<br/>                                                                       | No<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ CON \_ \_ SHA256 NULL <br/> Usato solo quando l'applicazione richiede in modo esplicito.<br/>            | Sì<br/>                      | TLS 1.2<br/>                            |
| TLS \_ RSA CON SHA \_ \_ \_ NULL <br/> Usato solo quando l'applicazione richiede in modo esplicito.<br/>               | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| SSL \_ CK \_ RC4 \_ 128 \_ WITH \_ MD5 <br/> Usato solo quando l'applicazione richiede in modo esplicito.<br/>            | No<br/>                       | SSL 2.0<br/>                            |
| SSL \_ CK \_ DES \_ 192 \_ EDE3 \_ CBC \_ WITH \_ MD5 <br/> Usato solo quando l'applicazione richiede in modo esplicito.<br/> | Sì<br/>                      | SSL 2.0<br/>                            |



 

I pacchetti di crittografia seguenti sono supportati dal provider Microsoft Schannel, ma non sono abilitati per impostazione predefinita:



| Stringa della suite di crittografia                                                                  | Consentito da SCH \_ USE \_ STRONG \_ CRYPTO | Versioni del protocollo TLS/SSL                     |
|--------------------------------------------------------------------------------------|-------------------------------------|-----------------------------------------------|
| TLS \_ RSA CON DES \_ \_ \_ CBC \_ SHA<br/>                                             | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ EXPORT1024 \_ CON \_ RC4 \_ 56 \_ SHA<br/>                                  | No<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA \_ EXPORT1024 \_ CON DES \_ \_ CBC \_ SHA<br/>                                 | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| ESPORTAZIONE \_ RSA TLS CON \_ \_ \_ RC4 \_ 40 \_ MD5<br/>                                      | No<br/>                       | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ RSA WITH NULL \_ \_ \_ MD5 viene usato solo quando l'applicazione richiede in modo esplicito.<br/> | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ DHE \_ DSS \_ CON DES \_ \_ CBC \_ SHA<br/>                                        | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| TLS \_ \_ DSS \_ EXPORT1024 \_ CON DES \_ \_ CBC \_ SHA<br/>                            | Sì<br/>                      | TLS 1.2, TLS 1.1, TLS 1.0, SSL 3.0<br/> |
| SSL \_ CK \_ DES \_ 64 \_ CBC \_ WITH \_ MD5<br/>                                          | Sì<br/>                      | SSL 2.0<br/>                            |
| SSL \_ CK \_ RC4 \_ 128 \_ EXPORT40 \_ WITH \_ MD5<br/>                                    | No<br/>                       | SSL 2.0<br/>                            |



 

Per aggiungere pacchetti di crittografia, distribuire criteri di gruppo o usare i cmdlet TLS:

-   Per usare i criteri di gruppo, configurare SSL Cipher Suite Order in Configurazione computer > Modelli amministrativi > Rete > Ssl Configuration Impostazioni con l'elenco di priorità per tutti i pacchetti di crittografia che si desidera sia abilitato.
-   Per usare PowerShell, vedere [Cmdlet TLS.](/powershell/module/tls/?view=win10-ps)

> [!Note]  
> Prima di Windows 10, le stringhe del gruppo di crittografia venivano aggiunte con la curva ellittica per determinare la priorità della curva. Windows 10 supporta un'impostazione dell'ordine di priorità a curva ellittica in modo che il suffisso a curva ellittica non sia obbligatorio e venga sostituito dal nuovo ordine di priorità della curva ellittica, se specificato, per consentire alle organizzazioni di usare Criteri di gruppo per configurare versioni diverse di Windows con gli stessi pacchetti di crittografia.

 

> [!IMPORTANT]
> I servizi Web HTTP/2 non sono compatibili con gli ordini di pacchetti di crittografia TLS personalizzati. Per altre informazioni, [vedere Come distribuire l'ordinamento dei pacchetti di crittografia personalizzati.](https://support.microsoft.com/help/4032720/how-to-deploy-custom-cipher-suite-ordering-in-windows-server-2016)

 

 

 
