---
description: Gli strumenti di crittografia forniscono gli strumenti da riga di comando per la firma del codice, la verifica della firma e altre attività di crittografia.
ms.assetid: 21adbcfb-fadd-4818-9dc5-23bfd526b525
title: Strumenti di crittografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8003bb002bd8d203547779c96bc15491a5418169
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306446"
---
# <a name="cryptography-tools"></a>Strumenti di crittografia

Gli strumenti di crittografia forniscono gli strumenti da riga di comando per la firma del codice, la verifica della firma e altre attività di crittografia.

## <a name="introduction-to-code-signing"></a>Introduzione alla firma del codice

Il settore software deve fornire agli utenti i mezzi per considerare attendibile il codice, incluso il codice pubblicato su Internet. Molte pagine Web contengono solo informazioni statiche che possono essere scaricate con pochi rischi. Alcune pagine contengono tuttavia controlli e applicazioni da scaricare ed eseguire nel computer di un utente. Questi file eseguibili possono essere rischiosi per il download e l'esecuzione.

Il software in pacchetto usa la personalizzazione e gli outlet di vendita attendibili per garantire l'integrità degli utenti, ma queste garanzie non sono disponibili quando il codice viene trasmesso su Internet. Inoltre, Internet non è in grado di fornire alcuna garanzia sull'identità dell'autore del software. Né può garantire che il software scaricato non sia stato modificato dopo la creazione. I browser possono presentare un messaggio di avviso in cui vengono illustrati i possibili rischi derivanti dal download dei dati di qualsiasi tipo, ma i browser non sono in grado di verificare che il codice sia quello che dichiara. Per rendere Internet un supporto affidabile per la distribuzione del software, è necessario adottare un approccio più attivo.

Un approccio per fornire garanzie dell'autenticità e dell' [*integrità*](../secgloss/i-gly.md) dei file è il fissaggio delle [*firme digitali*](../secgloss/d-gly.md) a tali file. Una firma digitale collegata a un file identifica in modo positivo il server di distribuzione del file e garantisce che il contenuto del file non sia stato modificato dopo la creazione della firma.

È possibile creare e verificare firme digitali usando le API di crittografia di Microsoft. Per informazioni di base sulla crittografia e sulle funzioni [*CryptoAPI*](../secgloss/c-gly.md) , vedere [Cryptography Essentials](cryptography-essentials.md).

Per informazioni dettagliate sulle [*firme digitali*](../secgloss/d-gly.md), i [*certificati*](../secgloss/c-gly.md)e gli [*archivi certificati*](../secgloss/c-gly.md), vedere gli argomenti seguenti:

-   [Hash e firme digitali](hashes-and-digital-signatures.md)
-   [Certificati digitali](digital-certificates.md)
-   [Gestione dei certificati con archivi certificati](managing-certificates-with-certificate-stores.md)
-   [Verifica dell'attendibilità del certificato](certificate-trust-verification.md)

Attualmente, gli strumenti CryptoAPI supportano la tecnologia Microsoft Authenticode consentendo ai fornitori di software di firmare i seguenti tipi di file per la verifica Authenticode.



| Estensione del file                             | Contenuto                                                                                                                                                                                                                              |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| appx<br/>                                | File del programma di installazione per un'app del dispositivo Windows Store.<br/>                                                                                                                                                                            |
| .cab<br/>                                 | File autonomi usati per l'installazione e l'installazione dell'applicazione. In un file CAB, più file vengono compressi in un unico file. Sono comunemente presenti nei dischi di distribuzione software Microsoft.<br/>                        |
| CAT<br/>                                 | File che contengono [*Identificazione*](../secgloss/t-gly.md) digitale di diversi file. Un file con estensione cat può essere utilizzato per garantire l'integrità dei file di cui sono incluse le identificazioni personali.<br/> |
| DLL<br/>                                 | File che contengono funzioni eseguibili.<br/>                                                                                                                                                                                   |
| EXE<br/>                                 | File che contengono programmi eseguibili.<br/>                                                                                                                                                                                    |
| .js<br/> .vbs<br/> .wsf<br/>  | File della shell di Windows per JScript o Microsoft Visual Basic Scripting Edition (VBScript).<br/>                                                                                                                                    |
| msi<br/> msp<br/> mst<br/> | File di Windows Installer.<br/>                                                                                                                                                                                                   |
| ocx<br/>                                 | File che contengono i controlli Microsoft ActiveX.<br/>                                                                                                                                                                             |
| PS1<br/>                                 | File che contengono script di PowerShell.<br/>                                                                                                                                                                                     |
| . STL<br/>                                 | File che contengono un [*elenco di certificati attendibili*](../secgloss/c-gly.md) (CTL).<br/>                                                                           |
| .sys<br/>                                 | File che contengono i file binari del driver.<br/>                                                                                                                                                                                        |



 

Per informazioni sulla firma digitale, vedere i documenti seguenti:

-   CCITT, Recommendation X. 509, *The Directory-Authentication Framework*, consultation Committee, International Telephone and Telegraph, International Telecommunications Union, ginevra, 1989.
-   RSA Laboratories, *PKCS \# 7: standard della sintassi del messaggio crittografico*. Versione 1,5, novembre 1993.
-   Schneier, Bruce, *Applied Cryptography*, 2D ed. New York: John Wiley & Sons, 1996.
-   [https://www.rsa.com](https://www.rsa.com/)

> [!Note]  
> Queste risorse potrebbero non essere disponibili in alcune lingue e paesi o aree geografiche.

 

## <a name="microsoft-cryptography-tools"></a>Strumenti di crittografia Microsoft

Gli strumenti di pubblicazione e la DLL di firma vengono installati nella \\ directory bin dell'installazione di Microsoft SDK. Includono i file seguenti.



| Nome file                    | Commenti                                                                                                                                                                                             |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Cert2SPC.exe](cert2spc.md) | Consente di creare un [*certificato di pubblicazione software*](../secgloss/s-gly.md) (SPC) esclusivamente a scopo di test.<br/> |
| [CertMgr.exe](certmgr.md)   | Gestisce certificati, scopi consentiti e [*elenchi di revoche di certificati*](../secgloss/c-gly.md) (CRL).<br/>             |
| [MakeCat.exe](makecat.md)   | Crea un file di catalogo senza segno che contiene gli hash di un set di file insieme agli attributi associati di ogni file.<br/>                                                               |
| [MakeCert.exe](makecert.md) | Crea un certificato [*X. 509*](../secgloss/x-gly.md) solo a scopo di test.<br/>                                                                      |
| Pvk2pfx.exe                  | Converte un file di certificato dell'editore del software (. SPC) o un file di chiave privata (con estensione PVK) in formato di file PFX (Personal Information Exchange).<br/>                                                   |
| [SetReg.exe](setreg.md)     | Imposta chiavi del registro di sistema che controllano la verifica del certificato.<br/>                                                                                                                                |
| [SignTool.exe](signtool.md) | Firma e timestamp di un file. Verifica inoltre la firma di un file.<br/>                                                                                                              |



 

 

 
