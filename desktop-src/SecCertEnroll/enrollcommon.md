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
# <a name="enrollcommon"></a><span data-ttu-id="2b9c3-103">enrollCommon</span><span class="sxs-lookup"><span data-stu-id="2b9c3-103">enrollCommon</span></span>

<span data-ttu-id="2b9c3-104">La cartella enrollCommon contiene le funzioni di supporto e le macro seguenti usate dagli esempi forniti con l'SDK di registrazione certificati.</span><span class="sxs-lookup"><span data-stu-id="2b9c3-104">The enrollCommon folder contains the following helper functions and macros used by the samples provided with the Certificate Enrollment SDK.</span></span> <span data-ttu-id="2b9c3-105">Viene installato per impostazione predefinita nella cartella *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 certificate di registrazione del certificato \\ VC \\ enrollCommon.</span><span class="sxs-lookup"><span data-stu-id="2b9c3-105">It is installed by default in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollCommon folder.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2b9c3-106">Funzione</span><span class="sxs-lookup"><span data-stu-id="2b9c3-106">Function</span></span></th>
<th><span data-ttu-id="2b9c3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b9c3-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2b9c3-108">_JumpIfError</span><span class="sxs-lookup"><span data-stu-id="2b9c3-108">_JumpIfError</span></span></td>
<td><span data-ttu-id="2b9c3-109">Una macro che accetta un valore <strong>HRESULT</strong> , un'etichetta e una stringa di errore, stampa la stringa e trasferisce il controllo Program alla prima istruzione che segue l'etichetta.</span><span class="sxs-lookup"><span data-stu-id="2b9c3-109">Macro that accepts an <strong>HRESULT</strong> value, a label, and an error string, prints the string, and transfers program control to the first statement following the label.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b9c3-110">_JumpError</span><span class="sxs-lookup"><span data-stu-id="2b9c3-110">_JumpError</span></span></td>
<td><span data-ttu-id="2b9c3-111">Equivale a _JumpIfError macro.</span><span class="sxs-lookup"><span data-stu-id="2b9c3-111">Same as the _JumpIfError macro.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b9c3-112">_PrintIfError</span><span class="sxs-lookup"><span data-stu-id="2b9c3-112">_PrintIfError</span></span></td>
<td><span data-ttu-id="2b9c3-113">Attualmente non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="2b9c3-113">Not currently used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b9c3-114">_PrintError</span><span class="sxs-lookup"><span data-stu-id="2b9c3-114">_PrintError</span></span></td>
<td><span data-ttu-id="2b9c3-115">Macro che stampa un messaggio di errore e un valore <strong>HRESULT</strong> .</span><span class="sxs-lookup"><span data-stu-id="2b9c3-115">Macro that prints an error message and an <strong>HRESULT</strong> value.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b9c3-116">convertWszToSz</span><span class="sxs-lookup"><span data-stu-id="2b9c3-116">convertWszToSz</span></span></td>
<td><span data-ttu-id="2b9c3-117">Converte una stringa di caratteri wide in una stringa di caratteri ASCII utilizzando la funzione <strong>WideCharToMultiByte</strong> e l'identificatore della tabella codici ANSI corrente per il sistema.</span><span class="sxs-lookup"><span data-stu-id="2b9c3-117">Converts a wide-character string to an ASCII character string by using the <strong>WideCharToMultiByte</strong> function and the current ANSI code-page identifier for the system.</span></span> <span data-ttu-id="2b9c3-118">Questa funzione viene usata dalle funzioni decConvertFromUnicode e findOIDFromTemplateName definite in enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="2b9c3-118">This function is used by the decConvertFromUnicode and findOIDFromTemplateName functions defined in enrollCommon.cpp.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b9c3-119">convertSzToWsz</span><span class="sxs-lookup"><span data-stu-id="2b9c3-119">convertSzToWsz</span></span></td>
<td><span data-ttu-id="2b9c3-120">Converte una stringa ASCII in una stringa di caratteri wide usando la funzione <strong>MultiByteToWideChar</strong> e l'identificatore della tabella codici ANSI corrente per il sistema.</span><span class="sxs-lookup"><span data-stu-id="2b9c3-120">Converts an ASCII string to a wide-character string by using the <strong>MultiByteToWideChar</strong> function and the current ANSI code-page identifier for the system.</span></span> <span data-ttu-id="2b9c3-121">Questa funzione viene utilizzata dalla funzione findCertByTemplate definita in enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="2b9c3-121">This function is used by the findCertByTemplate function defined in enrollCommon.cpp.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b9c3-122">convertSzToBstr</span><span class="sxs-lookup"><span data-stu-id="2b9c3-122">convertSzToBstr</span></span></td>
<td><span data-ttu-id="2b9c3-123">Converte una stringa ASCII in un <strong>BSTR</strong> utilizzando la funzione <strong>MultiByteToWideChar</strong> .</span><span class="sxs-lookup"><span data-stu-id="2b9c3-123">Converts an ASCII string to a <strong>BSTR</strong> by using the <strong>MultiByteToWideChar</strong> function.</span></span> <span data-ttu-id="2b9c3-124">Questa funzione non è attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="2b9c3-124">This function is not currently used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b9c3-125">convertWszToBstr</span><span class="sxs-lookup"><span data-stu-id="2b9c3-125">convertWszToBstr</span></span></td>
<td><span data-ttu-id="2b9c3-126">Converte una stringa di caratteri wide in un <strong>BSTR</strong>.</span><span class="sxs-lookup"><span data-stu-id="2b9c3-126">Converts a wide-character string to a <strong>BSTR</strong>.</span></span> <span data-ttu-id="2b9c3-127">Questa funzione viene usata dall'esempio installResponseFromPFX.</span><span class="sxs-lookup"><span data-stu-id="2b9c3-127">This function is used by the installResponseFromPFX sample.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b9c3-128">checkEnrollStatus</span><span class="sxs-lookup"><span data-stu-id="2b9c3-128">checkEnrollStatus</span></span></td>
<td><span data-ttu-id="2b9c3-129">Controlla lo stato del processo di registrazione del certificato usando le interfacce <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>metodo IX509Enrollment</strong></a> e <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus"><strong>IX509EnrollmentStatus</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="2b9c3-129">Checks the status of the certificate enrollment process by using the <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> and <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus"><strong>IX509EnrollmentStatus</strong></a> interfaces.</span></span> <span data-ttu-id="2b9c3-130">Questa funzione viene usata dagli esempi enrollEOBOCMC, enrollPKCS7, enrollRenewalPKCS7, enrollSimpleMachineCert e enrollSimpleUserCert.</span><span class="sxs-lookup"><span data-stu-id="2b9c3-130">This function is used by the enrollEOBOCMC, enrollPKCS7, enrollRenewalPKCS7, enrollSimpleMachineCert, and enrollSimpleUserCert samples.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b9c3-131">findCertByKeyUsage</span><span class="sxs-lookup"><span data-stu-id="2b9c3-131">findCertByKeyUsage</span></span></td>
<td><span data-ttu-id="2b9c3-132">Enumera l'archivio certificati personale dell'utente corrente per trovare il primo certificato per il quale l'utilizzo previsto della chiave pubblica corrisponde a un valore specificato.</span><span class="sxs-lookup"><span data-stu-id="2b9c3-132">Enumerates the personal certificate store of the current user to find the first certificate for which the intended use of the public key matches a specified value.</span></span> <span data-ttu-id="2b9c3-133">Il valore specificato può essere una combinazione bit per bit dei flag seguenti:</span><span class="sxs-lookup"><span data-stu-id="2b9c3-133">The value specified can be a bitwise combination of the following flags:</span></span>
<ul>
<li><span data-ttu-id="2b9c3-134">CERT_DATA_ENCIPHERMENT_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="2b9c3-134">CERT_DATA_ENCIPHERMENT_KEY_USAGE</span></span></li>
<li><span data-ttu-id="2b9c3-135">CERT_DIGITAL_SIGNATURE_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="2b9c3-135">CERT_DIGITAL_SIGNATURE_KEY_USAGE</span></span></li>
<li><span data-ttu-id="2b9c3-136">CERT_KEY_AGREEMENT_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="2b9c3-136">CERT_KEY_AGREEMENT_KEY_USAGE</span></span></li>
<li><span data-ttu-id="2b9c3-137">CERT_KEY_CERT_SIGN_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="2b9c3-137">CERT_KEY_CERT_SIGN_KEY_USAGE</span></span></li>
<li><span data-ttu-id="2b9c3-138">CERT_KEY_ENCIPHERMENT_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="2b9c3-138">CERT_KEY_ENCIPHERMENT_KEY_USAGE</span></span></li>
<li><span data-ttu-id="2b9c3-139">CERT_NON_REPUDIATION_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="2b9c3-139">CERT_NON_REPUDIATION_KEY_USAGE</span></span></li>
<li><span data-ttu-id="2b9c3-140">CERT_OFFLINE_CRL_SIGN_KEY_USAGE</span><span class="sxs-lookup"><span data-stu-id="2b9c3-140">CERT_OFFLINE_CRL_SIGN_KEY_USAGE</span></span></li>
</ul>
<span data-ttu-id="2b9c3-141">Questa funzione viene usata dall'esempio enrollFromPublicKey.</span><span class="sxs-lookup"><span data-stu-id="2b9c3-141">This function is used by the enrollFromPublicKey sample.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b9c3-142">findCertByEKU</span><span class="sxs-lookup"><span data-stu-id="2b9c3-142">findCertByEKU</span></span></td>
<td><span data-ttu-id="2b9c3-143">Enumera l'archivio certificati personale dell'utente corrente per trovare il primo certificato per il quale l'estensione utilizzo chiavi avanzato (EKU) corrisponde a quella specificata nell'input.</span><span class="sxs-lookup"><span data-stu-id="2b9c3-143">Enumerates the personal certificate store of the current user to find the first certificate for which the Enhanced Key Usage (EKU) extension matches that specified on input.</span></span> <span data-ttu-id="2b9c3-144">Per ulteriori informazioni sull'estensione EKU, vedere l'interfaccia <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage"><strong>IX509ExtensionEnhancedKeyUsage</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="2b9c3-144">For more information about the EKU extension, see the <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage"><strong>IX509ExtensionEnhancedKeyUsage</strong></a> interface.</span></span> <span data-ttu-id="2b9c3-145">Questa funzione viene usata dall'esempio enrollEOBOCMC.</span><span class="sxs-lookup"><span data-stu-id="2b9c3-145">This function is used by the enrollEOBOCMC sample.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b9c3-146">findCertByTemplate</span><span class="sxs-lookup"><span data-stu-id="2b9c3-146">findCertByTemplate</span></span></td>
<td><span data-ttu-id="2b9c3-147">Enumera l'archivio certificati personale dell'utente corrente per trovare il primo certificato per il quale il modello corrisponde a quello specificato, in base al nome, all'input.</span><span class="sxs-lookup"><span data-stu-id="2b9c3-147">Enumerates the personal certificate store of the current user to find the first certificate for which the template matches that specified, by name, on input.</span></span> <span data-ttu-id="2b9c3-148">Questa funzione viene usata dagli esempi enrollPKCS7 e enrollRenewalPKCS7.</span><span class="sxs-lookup"><span data-stu-id="2b9c3-148">This function is used by the enrollPKCS7 and enrollRenewalPKCS7 samples.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b9c3-149">enrollCertByTemplate</span><span class="sxs-lookup"><span data-stu-id="2b9c3-149">enrollCertByTemplate</span></span></td>
<td><span data-ttu-id="2b9c3-150">Inizializza un oggetto <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>metodo IX509Enrollment</strong></a> usando un modello, tenta di registrare la richiesta di certificato creata in modo implicito e monitora lo stato del processo di registrazione.</span><span class="sxs-lookup"><span data-stu-id="2b9c3-150">Initializes an <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> object by using a template, attempts to enroll the implicitly created certificate request, and monitors the status of the enrollment process.</span></span> <span data-ttu-id="2b9c3-151">Questa funzione viene usata dagli esempi enrollEOBOCMC, enrollFromPublicKey, enrollPKCS7 e enrollRenewalPKCS7.</span><span class="sxs-lookup"><span data-stu-id="2b9c3-151">This function is used by the enrollEOBOCMC, enrollFromPublicKey, enrollPKCS7, and enrollRenewalPKCS7 samples.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b9c3-152">verifyCertContext</span><span class="sxs-lookup"><span data-stu-id="2b9c3-152">verifyCertContext</span></span></td>
<td><span data-ttu-id="2b9c3-153">Verifica la conformità della catena di certificati rispetto ai criteri specificati (base) e, facoltativamente, rispetto a un'estensione di utilizzo chiavi avanzato (EKU) specificata.</span><span class="sxs-lookup"><span data-stu-id="2b9c3-153">Verifies compliance of the certificate chain against the specified (base) policy and, optionally, against a specified Enhanced Key Usage (EKU) extension.</span></span> <span data-ttu-id="2b9c3-154">Per ulteriori informazioni, vedere la funzione <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy"><strong>CertVerifyCertificateChainPolicy</strong></a> e le strutture <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_policy_para"><strong>CERT_CHAIN_POLICY_PARA</strong></a> e <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_para"><strong>CERT_CHAIN_PARA</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="2b9c3-154">For more information, see the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy"><strong>CertVerifyCertificateChainPolicy</strong></a> function and the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_policy_para"><strong>CERT_CHAIN_POLICY_PARA</strong></a> and <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_para"><strong>CERT_CHAIN_PARA</strong></a> structures.</span></span> <span data-ttu-id="2b9c3-155">Questa funzione viene usata dagli esempi enrollEOBOCMC, enrollFromPublicKey, enrollPKCS7 e enrollRenewalPKCS7.</span><span class="sxs-lookup"><span data-stu-id="2b9c3-155">This function is used by the enrollEOBOCMC, enrollFromPublicKey, enrollPKCS7, and enrollRenewalPKCS7 samples.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b9c3-156">decConvertFromUnicode</span><span class="sxs-lookup"><span data-stu-id="2b9c3-156">decConvertFromUnicode</span></span></td>
<td><span data-ttu-id="2b9c3-157">Converte una stringa di caratteri Unicode a doppio byte in una stringa di caratteri ANSI a byte singolo.</span><span class="sxs-lookup"><span data-stu-id="2b9c3-157">Converts a string of double-byte Unicode characters to a string of single-byte ANSI characters.</span></span> <span data-ttu-id="2b9c3-158">Questa funzione viene utilizzata dalla funzione DecodeFileW definita in enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="2b9c3-158">This function is used by the DecodeFileW function defined in enrollCommon.cpp.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b9c3-159">DecodeFileW</span><span class="sxs-lookup"><span data-stu-id="2b9c3-159">DecodeFileW</span></span></td>
<td><span data-ttu-id="2b9c3-160">Decodifica un certificato codificato o un file di richiesta di certificato in una matrice di byte.</span><span class="sxs-lookup"><span data-stu-id="2b9c3-160">Decodes an encoded certificate or certificate request file to a byte array.</span></span> <span data-ttu-id="2b9c3-161">Questa funzione viene usata dall'esempio installResponseFromPFX.</span><span class="sxs-lookup"><span data-stu-id="2b9c3-161">This function is used by the installResponseFromPFX sample.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b9c3-162">EncodeToFileW</span><span class="sxs-lookup"><span data-stu-id="2b9c3-162">EncodeToFileW</span></span></td>
<td><span data-ttu-id="2b9c3-163">Codifica un certificato o una richiesta di certificato e lo salva in un file.</span><span class="sxs-lookup"><span data-stu-id="2b9c3-163">Encodes a certificate or certificate request and saves it to a file.</span></span> <span data-ttu-id="2b9c3-164">Questa funzione viene usata dagli esempi createCNGCustomCMC, enrollEOBOCMC e enrollFromPublicKey.</span><span class="sxs-lookup"><span data-stu-id="2b9c3-164">This function is used by the createCNGCustomCMC, enrollEOBOCMC, and enrollFromPublicKey samples.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b9c3-165">findOIDFromTemplateName</span><span class="sxs-lookup"><span data-stu-id="2b9c3-165">findOIDFromTemplateName</span></span></td>
<td><span data-ttu-id="2b9c3-166">Recupera l'identificatore di oggetto per un modello specificato in base al nome.</span><span class="sxs-lookup"><span data-stu-id="2b9c3-166">Retrieves the object identifier for a template specified by name.</span></span> <span data-ttu-id="2b9c3-167">Questa funzione viene utilizzata dalla funzione findCertByTemplate definita in enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="2b9c3-167">This function is used by the findCertByTemplate function defined in enrollCommon.cpp.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="2b9c3-168">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2b9c3-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b9c3-169">Uso degli esempi inclusi</span><span class="sxs-lookup"><span data-stu-id="2b9c3-169">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

