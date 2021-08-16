---
description: Inizializza un oggetto richiesta di certificato PKCS 10, lo esegue il wrapping in un oggetto richiesta CMC, invia la richiesta CMC a un'autorità di certificazione dell'organizzazione (CA) e salva il certificato restituito dalla \# CA in un file.
ms.assetid: 0231da3b-a183-4443-8735-5affd24b145a
title: enrollFromPublicKey
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0346e2966dc9109ed9413022ead4eda487c37c2ac66ad9da42d2dcee2445032
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780050"
---
# <a name="enrollfrompublickey"></a>enrollFromPublicKey

L'esempio enrollFromPublicKey inizializza un oggetto richiesta di certificato PKCS 10, lo esegue il wrapping in un oggetto richiesta CMC, invia la richiesta CMC a un'autorità di certificazione (CA) dell'organizzazione e salva il certificato restituito dalla \# CA in un file.

## <a name="location"></a>Località

Quando si installa Microsoft Windows Software Development Kit (SDK), l'esempio viene installato, per impostazione predefinita, nella cartella *%ProgramFiles%* \\ Microsoft SDK Windows \\ \\ v7.0 \\ Samples Security \\ \\ X509 Certificate Enrollment \\ VC \\ enrollFromPublicKey.

## <a name="discussion"></a>Discussione

Esempio enrollFromPublicKey:

1.  Elabora gli argomenti della riga di comando seguenti:
    -   Nome di un modello di certificato.
    -   Nome di un file in cui salvare il certificato installato come matrice di byte con codifica Base64.
    -   Nome del modello di certificato di firma facoltativo. Il modello viene usato per creare un certificato di firma se non ne esiste nessuno nell'archivio certificati.
2.  Crea un oggetto chiave privata [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) e chiama il metodo [**Create**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-create) per creare una chiave privata asimmetrica usando il provider di crittografia predefinito, le dimensioni della chiave e i [**valori KeySpec**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyspec) per il computer corrente.
3.  Recupera la parte di chiave pubblica [**dell'oggetto IX509PrivateKey.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)
4.  Crea un [**oggetto IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) e lo inizializza usando il modello specificato nella riga di comando e la chiave pubblica.
5.  Crea un [**oggetto IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) e lo inizializza usando l'oggetto richiesta PKCS \# 10.
6.  Recupera un certificato di firma esistente o, se non è possibile trovarne uno, crea una richiesta di certificato dal modello specificato nella riga di comando e tenta di registrarlo. FindCertByKeyUsage è definito in enrollCommon.cpp.
7.  Verifica la catena di certificati.
8.  Crea un [**oggetto ISignerCertificate,**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) lo inizializza usando il certificato di firma, recupera la raccolta [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) dall'oggetto richiesta CMC e aggiunge l'oggetto certificato di firma alla raccolta.
9.  Codifica la richiesta CMC usando [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER).
10. Crea un [**oggetto ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) e lo usa per recuperare una stringa contenente la configurazione della CA.
11. Crea un oggetto [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) CryptoAPI e lo usa insieme alle stringhe che contengono la configurazione della CA e la richiesta di certificato per inviare la richiesta alla CA.
12. Controlla lo stato del processo di registrazione e salva il certificato installato in un file. La funzione EncodeToFileW è definita in enrollCommon.cpp.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Richiesta CMC](cmc-request.md)
</dt> <dt>

[Richiesta PKCS \# 10](pkcs--10-request.md)
</dt> <dt>

[Uso degli esempi inclusi](using-the-included-samples.md)
</dt> </dl>

 

 
