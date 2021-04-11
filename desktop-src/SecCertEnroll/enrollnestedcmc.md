---
description: Legge una richiesta di certificato CMC esistente da un file, ne esegue il wrapping in un'altra richiesta CMC, firma questa richiesta esterna, la invia a un'autorità di certificazione (CA) e salva la risposta del certificato dalla CA a un file.
ms.assetid: b1a9161d-1f9a-4c5b-acd2-6058dc65a258
title: enrollNestedCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f1df25a1bc7f6ce16a67f66ff58dc371a526813
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225898"
---
# <a name="enrollnestedcmc"></a>enrollNestedCMC

L'esempio enrollNestedCMC legge una richiesta di certificato CMC esistente da un file, ne esegue il wrapping in un'altra richiesta CMC, firma questa richiesta esterna, la invia a un'autorità di certificazione (CA) e salva la risposta del certificato dalla CA a un file.

## <a name="location"></a>Location

Quando si installa il Software Development Kit (SDK) di Microsoft Windows, l'esempio viene installato per impostazione predefinita nella cartella *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ X509 registrazione certificati \\ VC \\ enrollNestedCMC

## <a name="discussion"></a>Discussione

Esempio enrollNestedCMC:

1.  Elabora gli argomenti della riga di comando seguenti:
    -   Nome del file di input.
    -   Nome del file di output.
    -   Modello di richiesta facoltativo.
2.  Legge una richiesta CMC esistente da un file come matrice di byte codificata in base63, converte la matrice di byte in un **BSTR**, crea un oggetto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) e USA **BSTR** per inizializzare l'oggetto Request. L'oggetto inizializzato diventa la richiesta interna.
3.  Usa l'oggetto richiesta interno creato e inizializzato nel passaggio precedente per inizializzare un'altra richiesta CMC.
4.  Recupera un certificato di firma esistente o, se non è possibile trovarne uno, crea una richiesta di certificato dal modello specificato nella riga di comando e tenta di registrarla. Le funzioni findCertByTemplate e enrollCertByTemplate sono definite in enrollCommon. cpp.
5.  Recupera la raccolta [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) dalla richiesta CMC esterna, crea un nuovo oggetto [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) , lo inizializza usando il certificato di firma recuperato e lo aggiunge alla raccolta.
6.  Codifica la richiesta CMC usando Distinguished Encoding Rules (DER) e recupera la richiesta come **BSTR**.
7.  Crea un oggetto [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) e lo usa per recuperare una stringa che contiene la configurazione della CA.
8.  Crea un oggetto CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) e lo usa più le stringhe che contengono la configurazione della CA e la richiesta di certificato per inviare la richiesta all'autorità di certificazione.
9.  Controlla lo stato del processo di registrazione e salva la risposta del certificato dalla CA in un file. La funzione EncodeToFileW è definita in enrollCommon. cpp.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Richiesta CMC](cmc-request.md)
</dt> <dt>

[Uso degli esempi inclusi](using-the-included-samples.md)
</dt> </dl>

 

 
