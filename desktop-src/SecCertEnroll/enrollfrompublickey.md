---
description: Inizializza un \# oggetto richiesta di certificato PKCS 10, ne esegue il wrapping in un oggetto richiesta CMC, Invia la richiesta CMC a un'autorità di certificazione dell'organizzazione (Enterprise) e salva il certificato restituito dalla CA in un file.
ms.assetid: 0231da3b-a183-4443-8735-5affd24b145a
title: enrollFromPublicKey
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21b336d04727f4bb4b90674bad6bb6c429465a0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752727"
---
# <a name="enrollfrompublickey"></a>enrollFromPublicKey

Nell'esempio enrollFromPublicKey viene inizializzato un \# oggetto richiesta di certificato PKCS 10, ne viene eseguito il wrapping in un oggetto richiesta CMC, viene inviata la richiesta CMC a un'autorità di certificazione dell'organizzazione (Enterprise) e il certificato restituito dalla CA viene salvato in un file.

## <a name="location"></a>Location

Quando si installa il Software Development Kit (SDK) di Microsoft Windows, l'esempio viene installato per impostazione predefinita nella cartella *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 certificate \\ VC \\ enrollFromPublicKey

## <a name="discussion"></a>Discussione

Esempio enrollFromPublicKey:

1.  Elabora gli argomenti della riga di comando seguenti:
    -   Nome di un modello di certificato.
    -   Nome di un file in cui salvare il certificato installato come matrice di byte con codifica Base64.
    -   Nome facoltativo del modello di certificato di firma. Il modello viene usato per creare un certificato di firma, se non ne esiste alcuno nell'archivio certificati.
2.  Crea un oggetto chiave privata [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) e chiama il metodo [**create**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-create) per creare una chiave privata asimmetrica usando i valori predefiniti del [**provider di crittografia**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyspec) , della chiave e della chiave per il computer corrente.
3.  Recupera la parte della chiave pubblica dell'oggetto [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) .
4.  Crea un oggetto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) e lo inizializza usando il modello specificato nella riga di comando e la chiave pubblica.
5.  Crea un oggetto [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) e lo inizializza usando l' \# oggetto richiesta PKCS 10.
6.  Recupera un certificato di firma esistente o, se non è possibile trovarne uno, crea una richiesta di certificato dal modello specificato nella riga di comando e tenta di registrarla. FindCertByKeyUsage è definito in enrollCommon. cpp.
7.  Verifica la catena di certificati.
8.  Crea un oggetto [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) , lo inizializza usando il certificato di firma, recupera la raccolta [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) dall'oggetto della richiesta CMC e aggiunge l'oggetto certificato di firma alla raccolta.
9.  Codifica la richiesta CMC usando [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (der).
10. Crea un oggetto [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) e lo usa per recuperare una stringa che contiene la configurazione della CA.
11. Crea un oggetto CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) e lo usa più le stringhe che contengono la configurazione della CA e la richiesta di certificato per inviare la richiesta all'autorità di certificazione.
12. Controlla lo stato del processo di registrazione e salva il certificato installato in un file. La funzione EncodeToFileW è definita in enrollCommon. cpp.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Richiesta CMC](cmc-request.md)
</dt> <dt>

[\#Richiesta PKCS 10](pkcs--10-request.md)
</dt> <dt>

[Uso degli esempi inclusi](using-the-included-samples.md)
</dt> </dl>

 

 
