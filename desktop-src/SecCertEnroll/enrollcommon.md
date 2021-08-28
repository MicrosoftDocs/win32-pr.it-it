---
description: La cartella enrollCommon contiene le funzioni helper e le macro seguenti usate dagli esempi forniti con Certificate Enrollment SDK.
ms.assetid: a9b3532d-9640-4373-a6c6-7828cb6f55c7
title: enrollCommon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03ddc05ad1a143de025abbc875c8280a3f419d0e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476017"
---
# <a name="enrollcommon"></a>enrollCommon

La cartella enrollCommon contiene le funzioni helper e le macro seguenti usate dagli esempi forniti con Certificate Enrollment SDK. Viene installato per impostazione predefinita nella cartella *%ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v7.0 \\ Samples Security \\ \\ X509 Certificate Enrollment \\ VC \\ enrollCommon .




| Funzione | Descrizione | 
|----------|-------------|
| _JumpIfError | Macro che accetta un <strong>valore HRESULT,</strong> un'etichetta e una stringa di errore, stampa la stringa e trasferisce il controllo del programma alla prima istruzione che segue l'etichetta. | 
| _JumpError | Uguale alla macro _JumpIfError. | 
| _PrintIfError | Attualmente non utilizzato. | 
| _PrintError | Macro che stampa un messaggio di errore e un <strong>valore HRESULT.</strong> | 
| convertWszToSz | Converte una stringa di caratteri wide in una stringa di caratteri ASCII usando la funzione <strong>WideCharToMultiByte</strong> e l'identificatore della tabella codici ANSI corrente per il sistema. Questa funzione viene usata dalle funzioni decConvertFromUnicode e findOIDFromTemplateName definite in enrollCommon.cpp. | 
| convertSzToWsz | Converte una stringa ASCII in una stringa di caratteri wide usando la <strong>funzione MultiByteToWideChar</strong> e l'identificatore della tabella codici ANSI corrente per il sistema. Questa funzione viene usata dalla funzione findCertByTemplate definita in enrollCommon.cpp. | 
| convertSzToBstr | Converte una stringa ASCII in <strong>BSTR</strong> usando la <strong>funzione MultiByteToWideChar.</strong> Questa funzione non è attualmente usata. | 
| convertWszToBstr | Converte una stringa di caratteri wide in un <strong>oggetto BSTR.</strong> Questa funzione viene usata dall'esempio installResponseFromPFX. | 
| checkEnrollStatus | Controlla lo stato del processo di registrazione certificati usando le interfacce <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> e <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus"><strong>IX509EnrollmentStatus.</strong></a> Questa funzione viene usata dagli esempi enrollEOBOCMC, enrollPKCS7, enrollRenewalPKCS7, enrollSimpleMachineCert e enrollSimpleUserCert. | 
| findCertByKeyUsage | Enumera l'archivio certificati personale dell'utente corrente per trovare il primo certificato per il quale l'utilizzo previsto della chiave pubblica corrisponde a un valore specificato. Il valore specificato può essere una combinazione bit per bit dei flag seguenti:<ul><li>CERT_DATA_ENCIPHERMENT_KEY_USAGE</li><li>CERT_DIGITAL_SIGNATURE_KEY_USAGE</li><li>CERT_KEY_AGREEMENT_KEY_USAGE</li><li>CERT_KEY_CERT_SIGN_KEY_USAGE</li><li>CERT_KEY_ENCIPHERMENT_KEY_USAGE</li><li>CERT_NON_REPUDIATION_KEY_USAGE</li><li>CERT_OFFLINE_CRL_SIGN_KEY_USAGE</li></ul>Questa funzione viene usata dall'esempio enrollFromPublicKey.<br /> | 
| findCertByEKU | Enumera l'archivio certificati personale dell'utente corrente per trovare il primo certificato per il quale l'estensione Utilizzo chiavi avanzato (EKU) corrisponde a quella specificata nell'input. Per altre informazioni sull'estensione EKU, vedere <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage"><strong>l'interfaccia IX509ExtensionEnhancedKeyUsage.</strong></a> Questa funzione viene usata dall'esempio enrollEOBOCMC. | 
| findCertByTemplate | Enumera l'archivio certificati personale dell'utente corrente per trovare il primo certificato per il quale il modello corrisponde a quello specificato, in base al nome, nell'input. Questa funzione viene usata dagli esempi enrollPKCS7 e enrollRenewalPKCS7. | 
| enrollCertByTemplate | Inizializza un <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>oggetto IX509Enrollment</strong></a> usando un modello, tenta di registrare la richiesta di certificato creata in modo implicito e monitora lo stato del processo di registrazione. Questa funzione viene usata dagli esempi enrollEOBOCMC, enrollFromPublicKey, enrollPKCS7 e enrollRenewalPKCS7. | 
| verifyCertContext | Verifica la conformità della catena di certificati rispetto ai criteri (di base) specificati e, facoltativamente, a un'estensione EKU (Enhanced Key Usage) specificata. Per altre informazioni, vedere <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy"><strong>la funzione CertVerifyCertificateChainPolicy</strong></a> e le <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_policy_para"><strong>CERT_CHAIN_POLICY_PARA</strong></a> e <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_para"><strong>CERT_CHAIN_PARA</strong></a> seguenti. Questa funzione viene usata dagli esempi enrollEOBOCMC, enrollFromPublicKey, enrollPKCS7 e enrollRenewalPKCS7. | 
| decConvertFromUnicode | Converte una stringa di caratteri Unicode a byte doppio in una stringa di caratteri ANSI a byte singolo. Questa funzione viene usata dalla funzione DecodeFileW definita in enrollCommon.cpp. | 
| DecodeFileW | Decodifica un certificato codificato o un file di richiesta di certificato in una matrice di byte. Questa funzione viene usata dall'esempio installResponseFromPFX. | 
| EncodeToFileW | Codifica un certificato o una richiesta di certificato e lo salva in un file. Questa funzione viene usata dagli esempi createCNGCustomCMC, enrollEOBOCMC e enrollFromPublicKey. | 
| findOIDFromTemplateName | Recupera l'identificatore di oggetto per un modello specificato in base al nome. Questa funzione viene usata dalla funzione findCertByTemplate definita in enrollCommon.cpp. | 




 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso degli esempi inclusi](using-the-included-samples.md)
</dt> </dl>

 

