---
description: La cartella enrollCommon contiene le macro e le funzioni helper seguenti usate dagli esempi forniti con Certificate Enrollment SDK.
ms.assetid: a9b3532d-9640-4373-a6c6-7828cb6f55c7
title: enrollCommon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d087ce1aeced0ef68f5b33a06546897d09687ae5ccbd096f1bb34552d0a4a10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780070"
---
# <a name="enrollcommon"></a>enrollCommon

La cartella enrollCommon contiene le macro e le funzioni helper seguenti usate dagli esempi forniti con Certificate Enrollment SDK. Viene installato per impostazione predefinita nella cartella *%ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v7.0 \\ Samples Security \\ \\ X509 Certificate Enrollment \\ VC \\ enrollCommon .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Funzione</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>_JumpIfError</td>
<td>Macro che accetta un <strong>valore HRESULT,</strong> un'etichetta e una stringa di errore, stampa la stringa e trasferisce il controllo del programma alla prima istruzione successiva all'etichetta.</td>
</tr>
<tr class="even">
<td>_JumpError</td>
<td>Uguale alla macro _JumpIfError.</td>
</tr>
<tr class="odd">
<td>_PrintIfError</td>
<td>Attualmente non utilizzato.</td>
</tr>
<tr class="even">
<td>_PrintError</td>
<td>Macro che stampa un messaggio di errore e un <strong>valore HRESULT.</strong></td>
</tr>
<tr class="odd">
<td>convertWszToSz</td>
<td>Converte una stringa di caratteri wide in una stringa di caratteri ASCII usando la <strong>funzione WideCharToMultiByte</strong> e l'identificatore della tabella codici ANSI corrente per il sistema. Questa funzione viene usata dalle funzioni decConvertFromUnicode e findOIDFromTemplateName definite in enrollCommon.cpp.</td>
</tr>
<tr class="even">
<td>convertSzToWsz</td>
<td>Converte una stringa ASCII in una stringa di caratteri wide usando la <strong>funzione MultiByteToWideChar</strong> e l'identificatore della tabella codici ANSI corrente per il sistema. Questa funzione viene usata dalla funzione findCertByTemplate definita in enrollCommon.cpp.</td>
</tr>
<tr class="odd">
<td>convertSzToBstr</td>
<td>Converte una stringa ASCII in <strong>BSTR</strong> usando la <strong>funzione MultiByteToWideChar.</strong> Questa funzione non è attualmente usata.</td>
</tr>
<tr class="even">
<td>convertWszToBstr</td>
<td>Converte una stringa di caratteri wide in <strong>un oggetto BSTR.</strong> Questa funzione viene usata dall'esempio installResponseFromPFX.</td>
</tr>
<tr class="odd">
<td>checkEnrollStatus</td>
<td>Controlla lo stato del processo di registrazione certificati usando le interfacce <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> e <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus"><strong>IX509EnrollmentStatus.</strong></a> Questa funzione viene usata dagli esempi enrollEOBOCMC, enrollPKCS7, enrollRenewalPKCS7, enrollSimpleMachineCert e enrollSimpleUserCert.</td>
</tr>
<tr class="even">
<td>findCertByKeyUsage</td>
<td>Enumera l'archivio certificati personale dell'utente corrente per trovare il primo certificato per il quale l'uso previsto della chiave pubblica corrisponde a un valore specificato. Il valore specificato può essere una combinazione bit per bit dei flag seguenti:
<ul>
<li>CERT_DATA_ENCIPHERMENT_KEY_USAGE</li>
<li>CERT_DIGITAL_SIGNATURE_KEY_USAGE</li>
<li>CERT_KEY_AGREEMENT_KEY_USAGE</li>
<li>CERT_KEY_CERT_SIGN_KEY_USAGE</li>
<li>CERT_KEY_ENCIPHERMENT_KEY_USAGE</li>
<li>CERT_NON_REPUDIATION_KEY_USAGE</li>
<li>CERT_OFFLINE_CRL_SIGN_KEY_USAGE</li>
</ul>
Questa funzione viene usata dall'esempio enrollFromPublicKey.<br/></td>
</tr>
<tr class="odd">
<td>findCertByEKU</td>
<td>Enumera l'archivio certificati personale dell'utente corrente per trovare il primo certificato per cui l'estensione EKU (Enhanced Key Usage) corrisponde a quella specificata nell'input. Per altre informazioni sull'estensione EKU, vedere <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage"><strong>l'interfaccia IX509ExtensionEnhancedKeyUsage.</strong></a> Questa funzione viene usata dall'esempio enrollEOBOCMC.</td>
</tr>
<tr class="even">
<td>findCertByTemplate</td>
<td>Enumera l'archivio certificati personale dell'utente corrente per trovare il primo certificato per cui il modello corrisponde a quello specificato, in base al nome, nell'input. Questa funzione viene usata dagli esempi enrollPKCS7 e enrollRenewalPKCS7.</td>
</tr>
<tr class="odd">
<td>enrollCertByTemplate</td>
<td>Inizializza un <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>oggetto IX509Enrollment</strong></a> usando un modello, tenta di registrare la richiesta di certificato creata in modo implicito e monitora lo stato del processo di registrazione. Questa funzione viene usata dagli esempi enrollEOBOCMC, enrollFromPublicKey, enrollPKCS7 e enrollRenewalPKCS7.</td>
</tr>
<tr class="even">
<td>verifyCertContext</td>
<td>Verifica la conformità della catena di certificati rispetto ai criteri (di base) specificati e, facoltativamente, a un'estensione EKU (Enhanced Key Usage) specificata. Per altre informazioni, vedere la <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy"><strong>funzione CertVerifyCertificateChainPolicy</strong></a> e le CERT_CHAIN_POLICY_PARA <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_policy_para"><strong>e</strong></a> <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_para"><strong>CERT_CHAIN_PARA</strong></a> seguenti. Questa funzione viene usata dagli esempi enrollEOBOCMC, enrollFromPublicKey, enrollPKCS7 e enrollRenewalPKCS7.</td>
</tr>
<tr class="odd">
<td>decConvertFromUnicode</td>
<td>Converte una stringa di caratteri Unicode a byte doppio in una stringa di caratteri ANSI a byte singolo. Questa funzione viene usata dalla funzione DecodeFileW definita in enrollCommon.cpp.</td>
</tr>
<tr class="even">
<td>DecodeFileW</td>
<td>Decodifica un certificato codificato o un file di richiesta di certificato in una matrice di byte. Questa funzione viene usata dall'esempio installResponseFromPFX.</td>
</tr>
<tr class="odd">
<td>EncodeToFileW</td>
<td>Codifica un certificato o una richiesta di certificato e lo salva in un file. Questa funzione viene usata dagli esempi createCNGCustomCMC, enrollEOBOCMC e enrollFromPublicKey.</td>
</tr>
<tr class="even">
<td>findOIDFromTemplateName</td>
<td>Recupera l'identificatore di oggetto per un modello specificato in base al nome. Questa funzione viene usata dalla funzione findCertByTemplate definita in enrollCommon.cpp.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso degli esempi inclusi](using-the-included-samples.md)
</dt> </dl>

 

