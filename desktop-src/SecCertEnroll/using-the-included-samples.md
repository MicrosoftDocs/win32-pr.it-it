---
description: L'API di registrazione certificati include più esempi progettati per semplificare la creazione di applicazioni personalizzate. La maggior parte degli esempi viene scritta con C++, ma sono inclusi anche esempi di C# e Visual Basic Scripting Edition (VBScript).
ms.assetid: 70ac7b75-542c-4d79-85ce-4b1bac414879
title: Uso degli esempi inclusi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd3cbf17d35e65ade52e97438d638cbd4f1489e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315816"
---
# <a name="using-the-included-samples"></a>Uso degli esempi inclusi

L'API di registrazione certificati include più esempi progettati per semplificare la creazione di applicazioni personalizzate. La maggior parte degli esempi viene scritta con C++, ma sono inclusi anche esempi di C# e Visual Basic Scripting Edition (VBScript).

Quando si installa Microsoft Windows Software Development Kit (SDK), per impostazione predefinita vengono installati gli esempi seguenti nella cartella *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 certificate \\ .



| Esempio                                                                 | Descrizione                                                                                                                                                                                                                                                                                                                                                | Linguaggio            |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| [createCNGCustomCMC](createcngcustomcmc.md)                           | Crea un oggetto richiesta CMC da una richiesta PKCS 10 annidata interna \# .<br/>                                                                                                                                                                                                                                                                            | C++<br/>      |
| [enrollCommon](enrollcommon.md)                                       | Contiene le funzioni di supporto e le macro seguenti usate dagli esempi inclusi.<br/>                                                                                                                                                                                                                                                                | C++<br/>      |
| [enrollCustomCMC](enrollcustomcmc.md)                                 | Consente di creare una richiesta di certificato CMC e di registrare un computer in una gerarchia di certificati.<br/>                                                                                                                                                                                                                                                            | C++<br/>      |
| [enrollCustomPKCS10](enrollcustompkcs10.md)                           | Crea una richiesta PKCS \# 10 personalizzata, la invia a un' [*autorità di certificazione*](/windows/desktop/SecGloss/c-gly) (CA) autonoma e installa il certificato emesso nell' [*archivio certificati*](/windows/desktop/SecGloss/c-gly).<br/> | C++<br/>      |
| [enrollCustomPKCS10 \_ 2](enrollcustompkcs10-2.md)                      | Crea una richiesta PKCS \# 10 personalizzata e tenta di registrarla in una CA globale (Enterprise).<br/>                                                                                                                                                                                                                                                               | C++<br/>      |
| [enrollEOBOCMC](enrolleobocmc.md)                                     | Consente di creare una richiesta di certificato CMC per conto di un altro utente e di registrare l'utente in una gerarchia di certificati.<br/>                                                                                                                                                                                                                                    | C++<br/>      |
| [enrollFromPublicKey](enrollfrompublickey.md)                         | Inizializza un \# oggetto richiesta di certificato PKCS 10, ne esegue il wrapping in un oggetto della richiesta CMC, Invia la richiesta CMC a una CA globale (Enterprise) e salva il certificato restituito dalla CA in un file.<br/>                                                                                                                                                      | C++<br/>      |
| [enrollKeyArchivalCMC](enrollkeyarchivalcmc.md)                       | Crea una richiesta di certificato CMC per archiviare una [*chiave privata*](/windows/desktop/SecGloss/p-gly) in un'autorità di certificazione.<br/>                                                                                                                                                                                                     | C++<br/>      |
| [enrollNestedCMC](enrollnestedcmc.md)                                 | Legge una richiesta di certificato CMC esistente da un file, ne esegue il wrapping in un'altra richiesta CMC, firma questa richiesta esterna, la invia a una CA e salva la risposta del certificato dalla CA in un file.<br/>                                                                                                                                                 | C++<br/>      |
| [enrollPKCS7](enrollpkcs7.md)                                         | Crea una richiesta [*PKCS \# 7*](/windows/desktop/SecGloss/p-gly) da un certificato esistente ereditando le chiavi pubbliche e private e il modello di certificato. Nell'esempio viene registrato l'utente in una gerarchia di certificati e viene installata la risposta del certificato.<br/>                                   | C++<br/>      |
| [enrollRenewalPKCS7](enrollrenewalpkcs7.md)                           | Crea un \# oggetto richiesta PKCS 7 per rinnovare un certificato esistente.<br/>                                                                                                                                                                                                                                                                             | C++<br/>      |
| [enrollSimpleMachineCert](enrollsimplemachinecert.md)                 | Consente di registrare un computer in una gerarchia di certificati utilizzando un modello, un nome visualizzato del certificato e la descrizione del certificato.<br/>                                                                                                                                                                                                                 | C++, VBS<br/> |
| [enrollSimpleUserCert](enrollsimpleusercert.md)                       | Registra un utente finale con una CA usando un modello, il nome del soggetto e la lunghezza in bit della chiave.<br/>                                                                                                                                                                                                                                       | C++, C #<br/> |
| [enrollWithIX509EnrollmentHelper](enrollwithix509enrollmenthelper.md) | Viene illustrato come utilizzare il protocollo HTTP di Windows 7 per registrare un certificato in una CA globale (Enterprise).<br/>                                                                                                                                                                                                                                                | C#<br/>      |
| [installResponseFromPFX](installresponsefrompfx.md)                   | Installa un certificato registrato da un file PFX (Personal Information Exchange) nell'archivio certificati.<br/>                                                                                                                                                                                                                                      | C++<br/>      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dell'API di registrazione certificati](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

