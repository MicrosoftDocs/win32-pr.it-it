---
description: L'API Di registrazione certificati include più esempi progettati per facilitare la creazione di applicazioni personalizzate. La maggior parte degli esempi viene scritta usando C++, ma sono inclusi anche gli esempi C# e Visual Basic Scripting Edition (VBScript).
ms.assetid: 70ac7b75-542c-4d79-85ce-4b1bac414879
title: Uso degli esempi inclusi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 511d9d5424455c1b54c6bd03cc72138b3672b256d535dcbdaf31d2393b2cb5f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127205"
---
# <a name="using-the-included-samples"></a>Uso degli esempi inclusi

L'API Di registrazione certificati include più esempi progettati per facilitare la creazione di applicazioni personalizzate. La maggior parte degli esempi viene scritta usando C++, ma sono inclusi anche gli esempi C# e Visual Basic Scripting Edition (VBScript).

Quando si installa Microsoft Windows Software Development Kit (SDK), gli esempi seguenti vengono installati, per impostazione predefinita, nella cartella *%ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v7.0 \\ Samples Security \\ \\ X509 Certificate Enrollment \\ .



| Esempio                                                                 | Descrizione                                                                                                                                                                                                                                                                                                                                                | Linguaggio            |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| [createCNGCustomCMC](createcngcustomcmc.md)                           | Crea un oggetto richiesta CMC da una richiesta PKCS 10 annidata \# interna.<br/>                                                                                                                                                                                                                                                                            | C++<br/>      |
| [enrollCommon](enrollcommon.md)                                       | Contiene le macro e le funzioni helper seguenti usate dagli esempi inclusi.<br/>                                                                                                                                                                                                                                                                | C++<br/>      |
| [enrollCustomCMC](enrollcustomcmc.md)                                 | Crea una richiesta di certificato CMC e registra un computer in una gerarchia di certificati.<br/>                                                                                                                                                                                                                                                            | C++<br/>      |
| [enrollCustomPKCS10](enrollcustompkcs10.md)                           | Crea una richiesta PKCS 10 personalizzata, la invia a un'autorità di certificazione (CA) autonoma e installa il certificato emesso \# [*nell'archivio certificati*](/windows/desktop/SecGloss/c-gly). [](/windows/desktop/SecGloss/c-gly)<br/> | C++<br/>      |
| [enrollCustomPKCS10 \_ 2](enrollcustompkcs10-2.md)                      | Crea una richiesta PKCS \# 10 personalizzata e tenta di registrarla in una CA globale (enterprise).<br/>                                                                                                                                                                                                                                                               | C++<br/>      |
| [enrollEOBOCMC](enrolleobocmc.md)                                     | Crea una richiesta di certificato CMC per conto di un altro utente e registra l'utente in una gerarchia di certificati.<br/>                                                                                                                                                                                                                                    | C++<br/>      |
| [enrollFromPublicKey](enrollfrompublickey.md)                         | Inizializza un oggetto richiesta di certificato PKCS 10, lo esegue il wrapping in un oggetto richiesta CMC, invia la richiesta CMC a una CA globale (enterprise) e salva il certificato restituito dalla \# CA in un file.<br/>                                                                                                                                                      | C++<br/>      |
| [enrollKeyArchivalCMC](enrollkeyarchivalcmc.md)                       | Crea una richiesta di certificato CMC per archiviare [*una chiave privata*](/windows/desktop/SecGloss/p-gly) in una CA.<br/>                                                                                                                                                                                                     | C++<br/>      |
| [enrollNestedCMC](enrollnestedcmc.md)                                 | Legge una richiesta di certificato CMC esistente da un file, la esegue il wrapping in un'altra richiesta CMC, firma la richiesta esterna, la invia a una CA e salva la risposta del certificato dalla CA in un file.<br/>                                                                                                                                                 | C++<br/>      |
| [enrollPKCS7](enrollpkcs7.md)                                         | Crea una [*richiesta PKCS \# 7*](/windows/desktop/SecGloss/p-gly) da un certificato esistente ereditando le chiavi pubbliche e private e il modello di certificato. L'esempio registra l'utente in una gerarchia di certificati e installa la risposta del certificato.<br/>                                   | C++<br/>      |
| [enrollRenewalPKCS7](enrollrenewalpkcs7.md)                           | Crea un oggetto richiesta PKCS \# 7 per rinnovare un certificato esistente.<br/>                                                                                                                                                                                                                                                                             | C++<br/>      |
| [enrollSimpleMachineCert](enrollsimplemachinecert.md)                 | Registra un computer in una gerarchia di certificati usando un modello, un nome visualizzato del certificato e la descrizione del certificato.<br/>                                                                                                                                                                                                                 | C++, VBS<br/> |
| [enrollSimpleUserCert](enrollsimpleusercert.md)                       | Registra un utente finale con una CA usando un modello, il nome del soggetto e la lunghezza, in bit, della chiave.<br/>                                                                                                                                                                                                                                       | C++, C #<br/> |
| [enrollWithIX509EnrollmentHelper](enrollwithix509enrollmenthelper.md) | Illustra come usare il protocollo HTTP Windows 7 per registrare un certificato in una CA globale (enterprise).<br/>                                                                                                                                                                                                                                                | C#<br/>      |
| [installResponseFromPFX](installresponsefrompfx.md)                   | Installa un certificato registrato da un file PFX (Personal Information Exchange) nell'archivio certificati.<br/>                                                                                                                                                                                                                                      | C++<br/>      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dell'API di registrazione certificati](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

