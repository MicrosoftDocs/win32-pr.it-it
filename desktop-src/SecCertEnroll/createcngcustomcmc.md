---
description: Crea un oggetto richiesta CMC da una richiesta PKCS 10 annidata \# interna.
ms.assetid: 8a0dc078-22ca-4bff-9cc0-46823912d3da
title: createCNGCustomCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0494fdf2af9e4e96983ed1aff462b38e749516eafe87f645a3bf8ae1b342292d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119798271"
---
# <a name="createcngcustomcmc"></a>createCNGCustomCMC

L'esempio createCNGCustomCMC crea un oggetto richiesta CMC da una richiesta PKCS 10 annidata \# interna. La richiesta interna viene creata usando una chiave privata [*asimmetrica*](/windows/desktop/SecGloss/p-gly). La chiave privata viene creata usando il provider del servizio di crittografia CNG (Cryptography API: Next Generation) e l'algoritmo specificato nella riga di comando. Nella chiave privata vengono impostate anche opzioni personalizzate, ad esempio i criteri di esportazione e il livello di protezione della chiave.

## <a name="location"></a>Località

Quando si installa Microsoft Windows Software Development Kit (SDK), l'esempio viene installato, per impostazione predefinita, nella cartella *%ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v7.0 \\ Samples Security \\ \\ X509 Certificate Enrollment \\ VC \\ createCNGCustomCMC .

## <a name="discussion"></a>Discussione

L'esempio createCNGCustomCMC:

1.  Elabora gli argomenti della riga di comando seguenti:
    -   Nome di un [*provider*](/windows/desktop/SecGloss/c-gly) del servizio di crittografia (CSP) CNG.
    -   Nome dell'algoritmo utilizzato per generare una chiave privata asimmetrica.
    -   Nome dell'algoritmo utilizzato per eseguire [*l'hashing*](/windows/desktop/SecGloss/h-gly) della [*richiesta di certificato.*](/windows/desktop/SecGloss/c-gly)
    -   File di output in cui salvare la richiesta di certificato.
    -   Stringa facoltativa (AlternateSignature) che, se presente, specifica che deve essere usato un algoritmo di firma discreto anziché combinato. Per altre informazioni, vedere la [**proprietà AlternateSignatureAlgorithm.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm)
2.  Crea un [**oggetto IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) e imposta le proprietà seguenti:
    -   [**LegacyCsp**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_legacycsp)
    -   [**ProviderName**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_providername)
    -   [**Algoritmo**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_algorithm)
    -   [**Protezione delle chiavi**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyprotection)
    -   [**ExportPolicy**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_exportpolicy)
3.  Crea una chiave privata asimmetrica.
4.  Crea un [**oggetto IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) e lo inizializza usando la chiave privata.
5.  Crea un [**oggetto IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) e lo inizializza usando l'oggetto richiesta PKCS \# 10 creato nel passaggio 4.
6.  Imposta il flag dell'algoritmo di firma alternativo su **VARIANT \_ TRUE** o **VARIANT \_ FALSE** a seconda che nella riga di comando sia specificata o meno una stringa di firma alternativa. Per altre informazioni, vedere [**AlternateSignatureAlgorithm.**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm)
7.  Crea un [*identificatore di oggetto*](/windows/desktop/SecGloss/h-gly) [*dell'algoritmo*](/windows/desktop/SecGloss/o-gly) hash (OID) dal nome dell'algoritmo specificato nella riga di comando e imposta l'OID nell'oggetto richiesta CMC.
8.  Firma la richiesta di certificato e la codifica [*usando Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER).
9.  Recupera una stringa che contiene la richiesta di certificato CMC codificata e la salva in un file. La funzione EncodeToFileW è definita in EnrollCommon.cpp.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Richiesta CMC](cmc-request.md)
</dt> <dt>

[Richiesta PKCS \# 10](pkcs--10-request.md)
</dt> <dt>

[Uso degli esempi inclusi](using-the-included-samples.md)
</dt> <dt>

[**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)
</dt> </dl>

 

 
