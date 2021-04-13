---
description: La cartella enrollCommon contiene le funzioni di supporto e le macro seguenti usate dagli esempi forniti con l'SDK di registrazione certificati.
ms.assetid: a9b3532d-9640-4373-a6c6-7828cb6f55c7
title: enrollCommon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 384a1f3741fd8bd7762c60da524e2e639c442e41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527000"
---
# <a name="enrollcommon"></a>enrollCommon

La cartella enrollCommon contiene le funzioni di supporto e le macro seguenti usate dagli esempi forniti con l'SDK di registrazione certificati. Viene installato per impostazione predefinita nella cartella *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 certificate di registrazione del certificato \\ VC \\ enrollCommon.



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
<td>Una macro che accetta un valore <strong>HRESULT</strong> , un'etichetta e una stringa di errore, stampa la stringa e trasferisce il controllo Program alla prima istruzione che segue l'etichetta.</td>
</tr>
<tr class="even">
<td>_JumpError</td>
<td>Equivale a _JumpIfError macro.</td>
</tr>
<tr class="odd">
<td>_PrintIfError</td>
<td>Attualmente non utilizzato.</td>
</tr>
<tr class="even">
<td>_PrintError</td>
<td>Macro che stampa un messaggio di errore e un valore <strong>HRESULT</strong> .</td>
</tr>
<tr class="odd">
<td>convertWszToSz</td>
<td>Converte una stringa di caratteri wide in una stringa di caratteri ASCII utilizzando la funzione <strong>WideCharToMultiByte</strong> e l'identificatore della tabella codici ANSI corrente per il sistema. Questa funzione viene usata dalle funzioni decConvertFromUnicode e findOIDFromTemplateName definite in enrollCommon. cpp.</td>
</tr>
<tr class="even">
<td>convertSzToWsz</td>
<td>Converte una stringa ASCII in una stringa di caratteri wide usando la funzione <strong>MultiByteToWideChar</strong> e l'identificatore della tabella codici ANSI corrente per il sistema. Questa funzione viene utilizzata dalla funzione findCertByTemplate definita in enrollCommon. cpp.</td>
</tr>
<tr class="odd">
<td>convertSzToBstr</td>
<td>Converte una stringa ASCII in un <strong>BSTR</strong> utilizzando la funzione <strong>MultiByteToWideChar</strong> . Questa funzione non è attualmente in uso.</td>
</tr>
<tr class="even">
<td>convertWszToBstr</td>
<td>Converte una stringa di caratteri wide in un <strong>BSTR</strong>. Questa funzione viene usata dall'esempio installResponseFromPFX.</td>
</tr>
<tr class="odd">
<td>checkEnrollStatus</td>
<td>Controlla lo stato del processo di registrazione del certificato usando le interfacce <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>metodo IX509Enrollment</strong></a> e <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus"><strong>IX509EnrollmentStatus</strong></a> . Questa funzione viene usata dagli esempi enrollEOBOCMC, enrollPKCS7, enrollRenewalPKCS7, enrollSimpleMachineCert e enrollSimpleUserCert.</td>
</tr>
<tr class="even">
<td>findCertByKeyUsage</td>
<td>Enumera l'archivio certificati personale dell'utente corrente per trovare il primo certificato per il quale l'utilizzo previsto della chiave pubblica corrisponde a un valore specificato. Il valore specificato può essere una combinazione bit per bit dei flag seguenti:
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
<td>Enumera l'archivio certificati personale dell'utente corrente per trovare il primo certificato per il quale l'estensione utilizzo chiavi avanzato (EKU) corrisponde a quella specificata nell'input. Per ulteriori informazioni sull'estensione EKU, vedere l'interfaccia <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage"><strong>IX509ExtensionEnhancedKeyUsage</strong></a> . Questa funzione viene usata dall'esempio enrollEOBOCMC.</td>
</tr>
<tr class="even">
<td>findCertByTemplate</td>
<td>Enumera l'archivio certificati personale dell'utente corrente per trovare il primo certificato per il quale il modello corrisponde a quello specificato, in base al nome, all'input. Questa funzione viene usata dagli esempi enrollPKCS7 e enrollRenewalPKCS7.</td>
</tr>
<tr class="odd">
<td>enrollCertByTemplate</td>
<td>Inizializza un oggetto <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>metodo IX509Enrollment</strong></a> usando un modello, tenta di registrare la richiesta di certificato creata in modo implicito e monitora lo stato del processo di registrazione. Questa funzione viene usata dagli esempi enrollEOBOCMC, enrollFromPublicKey, enrollPKCS7 e enrollRenewalPKCS7.</td>
</tr>
<tr class="even">
<td>verifyCertContext</td>
<td>Verifica la conformità della catena di certificati rispetto ai criteri specificati (base) e, facoltativamente, rispetto a un'estensione di utilizzo chiavi avanzato (EKU) specificata. Per ulteriori informazioni, vedere la funzione <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy"><strong>CertVerifyCertificateChainPolicy</strong></a> e le strutture <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_policy_para"><strong>CERT_CHAIN_POLICY_PARA</strong></a> e <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_para"><strong>CERT_CHAIN_PARA</strong></a> . Questa funzione viene usata dagli esempi enrollEOBOCMC, enrollFromPublicKey, enrollPKCS7 e enrollRenewalPKCS7.</td>
</tr>
<tr class="odd">
<td>decConvertFromUnicode</td>
<td>Converte una stringa di caratteri Unicode a doppio byte in una stringa di caratteri ANSI a byte singolo. Questa funzione viene utilizzata dalla funzione DecodeFileW definita in enrollCommon. cpp.</td>
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
<td>Recupera l'identificatore di oggetto per un modello specificato in base al nome. Questa funzione viene utilizzata dalla funzione findCertByTemplate definita in enrollCommon. cpp.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso degli esempi inclusi](using-the-included-samples.md)
</dt> </dl>

 

