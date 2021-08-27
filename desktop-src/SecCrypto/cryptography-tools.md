---
description: Gli strumenti di crittografia forniscono strumenti da riga di comando per la firma del codice, la verifica della firma e altre attività di crittografia.
ms.assetid: 21adbcfb-fadd-4818-9dc5-23bfd526b525
title: Strumenti di crittografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9547ba1d3a13958859c2f0504c60a1a1bbe4a67403c9709bb57900b73ad3a50d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100981"
---
# <a name="cryptography-tools"></a>Strumenti di crittografia

Gli strumenti di crittografia forniscono strumenti da riga di comando per la firma del codice, la verifica della firma e altre attività di crittografia.

## <a name="introduction-to-code-signing"></a>Introduzione alla firma del codice

Il settore del software deve fornire agli utenti i mezzi per considerare attendibile il codice, incluso il codice pubblicato su Internet. Molte pagine Web contengono solo informazioni statiche che possono essere scaricate con poco rischio. Alcune pagine, tuttavia, contengono controlli e applicazioni da scaricare ed eseguire nel computer di un utente. Questi file eseguibili possono essere rischiosi da scaricare ed eseguire.

Il software in pacchetto usa la personalizzazione e i punti vendita attendibili per garantire agli utenti l'integrità, ma queste garanzie non sono disponibili quando il codice viene trasmesso su Internet. Inoltre, Internet stesso non può fornire alcuna garanzia sull'identità dell'autore del software. Né può garantire che qualsiasi software scaricato non sia stato modificato dopo la creazione. I browser possono visualizzare un messaggio di avviso che spiega i possibili rischi di download di dati di qualsiasi tipo, ma i browser non possono verificare che il codice sia quello che dichiara di essere. È necessario un approccio più attivo per rendere Internet un supporto affidabile per la distribuzione del software.

Un approccio per garantire l'autenticità e l'integrità dei file consiste nel collegare firme [*digitali*](../secgloss/d-gly.md) a tali file. [](../secgloss/i-gly.md) Una firma digitale allegata a un file identifica in modo positivo il server di distribuzione del file e garantisce che il contenuto del file non sia stato modificato dopo la creazione della firma.

Le firme digitali possono essere create e verificate usando le API di crittografia di Microsoft. Per informazioni di base sulla crittografia e sulle [*funzioni CryptoAPI,*](../secgloss/c-gly.md) vedere [Cryptography Essentials](cryptography-essentials.md).

Per informazioni dettagliate su [*firme*](../secgloss/d-gly.md)digitali, [*certificati*](../secgloss/c-gly.md)e archivi [*certificati,*](../secgloss/c-gly.md)vedere gli argomenti seguenti:

-   [Hash e firme digitali](hashes-and-digital-signatures.md)
-   [Certificati digitali](digital-certificates.md)
-   [Gestione dei certificati con archivi certificati](managing-certificates-with-certificate-stores.md)
-   [Verifica dell'attendibilità del certificato](certificate-trust-verification.md)

Attualmente, Gli strumenti CryptoAPI supportano la tecnologia Microsoft Authenticode consentendo ai fornitori di software di firmare i tipi di file seguenti per la verifica Authenticode.



| Estensione del file                             | Contenuto                                                                                                                                                                                                                              |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| appx<br/>                                | File del programma di installazione per un Windows app per dispositivi dello Store.<br/>                                                                                                                                                                            |
| .cab<br/>                                 | File autonomi usati per l'installazione e l'installazione dell'applicazione. In un file CAB più file vengono compressi in un unico file. Si trovano comunemente nei dischi di distribuzione software Microsoft.<br/>                        |
| CAT<br/>                                 | File che contengono [*identificazioni digitali di*](../secgloss/t-gly.md) più file. È possibile usare un file cat per garantire l'integrità dei file di cui include l'identificazione personale.<br/> |
| DLL<br/>                                 | File che contengono funzioni eseguibili.<br/>                                                                                                                                                                                   |
| EXE<br/>                                 | File che contengono programmi eseguibili.<br/>                                                                                                                                                                                    |
| .js<br/> .vbs<br/> .wsf<br/>  | Windows file della shell per JScript o Microsoft Visual Basic Scripting Edition (VBScript).<br/>                                                                                                                                    |
| msi<br/> msp<br/> mst<br/> | Windows file del programma di installazione.<br/>                                                                                                                                                                                                   |
| ocx<br/>                                 | File che contengono i controlli ActiveX Microsoft.<br/>                                                                                                                                                                             |
| PS1<br/>                                 | File che contengono script di PowerShell.<br/>                                                                                                                                                                                     |
| .stl<br/>                                 | File che contengono un [*elenco di certificati attendibili*](../secgloss/c-gly.md) (CTL).<br/>                                                                           |
| .sys<br/>                                 | File che contengono file binari del driver.<br/>                                                                                                                                                                                        |



 

Per informazioni sulla firma digitale, vedere i documenti seguenti:

-   CCITT, Recommendation X.509, *The Directory-Authentication Framework,* Consult committee, International Telephone and Telegraph, International Telecommunications Union, Geneva, 1989.
-   RSA Laboratories, *PKCS \# 7: Cryptographic Message Syntax Standard*. Versione 1.5, novembre 1993.
-   Schneier, Bruce, *Applied Cryptography*, 2d ed. New York: John Wiley &, 1996.
-   [https://www.rsa.com](https://www.rsa.com/)

> [!Note]  
> Queste risorse potrebbero non essere disponibili in alcune lingue e paesi o aree geografiche.

 

## <a name="microsoft-cryptography-tools"></a>Strumenti di crittografia Microsoft

Gli strumenti di pubblicazione e la DLL di firma vengono installati nella \\ directory Bin dell'installazione di Microsoft SDK. Includono i file seguenti.



| Nome file                    | Commenti                                                                                                                                                                                             |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Cert2SPC.exe](cert2spc.md) | Crea un [*certificato Publisher software*](../secgloss/s-gly.md) (SPC) solo a scopo di test.<br/> |
| [CertMgr.exe](certmgr.md)   | Gestisce certificati, CRL ed elenchi [*di revoche*](../secgloss/c-gly.md) di certificati (CRL).<br/>             |
| [MakeCat.exe](makecat.md)   | Crea un file di catalogo non firmato che contiene gli hash di un set di file insieme agli attributi associati di ogni file.<br/>                                                               |
| [MakeCert.exe](makecert.md) | Crea un [*certificato X.509*](../secgloss/x-gly.md) solo a scopo di test.<br/>                                                                      |
| Pvk2pfx.exe                  | Converte un file di certificato dell'editore software (con estensione spc) o un file di chiave privata (con estensione pvk) nel formato di file PFX (Personal Information Exchange).<br/>                                                   |
| [SetReg.exe](setreg.md)     | Imposta le chiavi del Registro di sistema che controllano la verifica del certificato.<br/>                                                                                                                                |
| [SignTool.exe](signtool.md) | Segni e timestamp di un file. Controlla inoltre la firma di un file.<br/>                                                                                                              |



 

 

 
