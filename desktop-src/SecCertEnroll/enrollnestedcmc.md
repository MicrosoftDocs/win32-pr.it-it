---
description: Legge una richiesta di certificato CMC esistente da un file, ne esegue il wrapping in un'altra richiesta CMC, firma la richiesta esterna, la invia a un'autorità di certificazione (CA) e salva la risposta del certificato dalla CA in un file.
ms.assetid: b1a9161d-1f9a-4c5b-acd2-6058dc65a258
title: enrollNestedCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b55c2957fc04e8bd9a088d3a07ed10c639c29d27dd1262b34709a9215c6c8b15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882941"
---
# <a name="enrollnestedcmc"></a>enrollNestedCMC

L'esempio enrollNestedCMC legge una richiesta di certificato CMC esistente da un file, ne esegue il wrapping in un'altra richiesta CMC, firma la richiesta esterna, la invia a un'autorità di certificazione (CA) e salva la risposta del certificato dalla CA in un file.

## <a name="location"></a>Località

Quando si installa Microsoft Windows Software Development Kit (SDK), l'esempio viene installato, per impostazione predefinita, nella cartella *%ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v7.0 \\ Samples \\ X509 Certificate Enrollment \\ VC \\ enrollNestedCMC .

## <a name="discussion"></a>Discussione

L'esempio enrollNestedCMC:

1.  Elabora gli argomenti della riga di comando seguenti:
    -   Nome del file di input.
    -   Nome del file di output.
    -   Modello di richiesta facoltativo.
2.  Legge una richiesta CMC esistente da un file come matrice di byte con codifica Base63, converte la matrice di byte in **un BSTR,** crea un oggetto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) e usa **BSTR** per inizializzare l'oggetto richiesta. L'oggetto inizializzato diventa la richiesta interna.
3.  Usa l'oggetto richiesta interno creato e inizializzato nel passaggio precedente per inizializzare un'altra richiesta CMC.
4.  Recupera un certificato di firma esistente o, se non è possibile trovarne uno, crea una richiesta di certificato dal modello specificato nella riga di comando e tenta di registrarlo. Le funzioni findCertByTemplate e enrollCertByTemplate sono definite in enrollCommon.cpp.
5.  Recupera la [**raccolta ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) dalla richiesta CMC esterna, crea un nuovo oggetto [**ISignerCertificate,**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) lo inizializza usando il certificato di firma recuperato e lo aggiunge alla raccolta.
6.  Codifica la richiesta CMC usando Distinguished Encoding Rules (DER) e recupera la richiesta come **BSTR.**
7.  Crea un [**oggetto ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) e lo usa per recuperare una stringa che contiene la configurazione della CA.
8.  Crea un oggetto [**CryptoAPI ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) e lo usa insieme alle stringhe che contengono la configurazione della CA e la richiesta di certificato per inviare la richiesta alla CA.
9.  Controlla lo stato del processo di registrazione e salva la risposta del certificato dalla CA in un file. La funzione EncodeToFileW è definita in enrollCommon.cpp.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Richiesta CMC](cmc-request.md)
</dt> <dt>

[Uso degli esempi inclusi](using-the-included-samples.md)
</dt> </dl>

 

 
