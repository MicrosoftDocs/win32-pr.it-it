---
description: CryptXML consente agli sviluppatori di estendere gli algoritmi crittografici supportati in modo nativo mediante la registrazione di una DLL di estensione crittografica a livello di sistema.
ms.assetid: b0625481-660a-4fd5-ba15-d532998f95a6
title: Estensioni crittografiche della firma digitale XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8747521913ca1d551f1a2d4fd5b1c79d80065832
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "103885892"
---
# <a name="xml-digital-signature-cryptographic-extensions"></a><span data-ttu-id="67ae9-103">Estensioni crittografiche della firma digitale XML</span><span class="sxs-lookup"><span data-stu-id="67ae9-103">XML Digital Signature Cryptographic Extensions</span></span>

<span data-ttu-id="67ae9-104">CryptXML consente agli sviluppatori di estendere gli algoritmi crittografici supportati in modo nativo mediante la registrazione di una DLL di estensione crittografica a livello di sistema.</span><span class="sxs-lookup"><span data-stu-id="67ae9-104">CryptXML allows developers to extend natively supported cryptographic algorithms by registering a system wide cryptographic extension DLL.</span></span> <span data-ttu-id="67ae9-105">Le DLL di estensione estendono gli algoritmi supportati dagli elementi XML **SignatureMethod** e **DigestMethod** .</span><span class="sxs-lookup"><span data-stu-id="67ae9-105">Extension DLLs extend the algorithms supported by **SignatureMethod** and **DigestMethod** XML elements.</span></span> <span data-ttu-id="67ae9-106">Le DLL di estensione possono supportare algoritmi che codificano parametri aggiuntivi nella firma digitale XML.</span><span class="sxs-lookup"><span data-stu-id="67ae9-106">Extension DLLs can support algorithms that encode additional parameters into the XML digital signature.</span></span>

<span data-ttu-id="67ae9-107">Tutte le DLL delle estensioni devono supportare la funzione [**CryptXmlDllGetInterface**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface) , che restituisce un puntatore a una struttura di [**\_ \_ \_ interfaccia di crittografia XML Crypt**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_cryptographic_interface) .</span><span class="sxs-lookup"><span data-stu-id="67ae9-107">All extensions DLLs must support the [**CryptXmlDllGetInterface**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface) function, which returns a pointer to a [**CRYPT\_XML\_CRYPTOGRAPHIC\_INTERFACE**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_cryptographic_interface) structure.</span></span> <span data-ttu-id="67ae9-108">Questa struttura fornisce i puntatori a funzione per le funzioni di estensione crittografiche implementate.</span><span class="sxs-lookup"><span data-stu-id="67ae9-108">This structure provides function pointers to implemented cryptographic extension functions.</span></span> <span data-ttu-id="67ae9-109">Le funzioni supportate dipendono dal tipo di algoritmo di crittografia supportato e dal fatto che l'algoritmo debba codificare i parametri nella firma digitale XML.</span><span class="sxs-lookup"><span data-stu-id="67ae9-109">The functions supported depend on the type of cryptographic algorithm supported and whether the algorithm must encode parameters into the XML digital signature.</span></span>

<span data-ttu-id="67ae9-110">Le funzioni delle estensioni crittografiche includono i seguenti puntatori a funzione:</span><span class="sxs-lookup"><span data-stu-id="67ae9-110">Cryptographic extensions functions include the following function pointers:</span></span>

<dl> <dt>

<span data-ttu-id="67ae9-111"><span id="Required_functions"></span><span id="required_functions"></span><span id="REQUIRED_FUNCTIONS"></span>Funzioni obbligatorie</span><span class="sxs-lookup"><span data-stu-id="67ae9-111"><span id="Required_functions"></span><span id="required_functions"></span><span id="REQUIRED_FUNCTIONS"></span>Required functions</span></span>
</dt> <dd>

-   [<span data-ttu-id="67ae9-112">**CryptXmlDllGetInterface**</span><span class="sxs-lookup"><span data-stu-id="67ae9-112">**CryptXmlDllGetInterface**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface)
-   [<span data-ttu-id="67ae9-113">**CryptXmlDllGetAlgorithmInfo**</span><span class="sxs-lookup"><span data-stu-id="67ae9-113">**CryptXmlDllGetAlgorithmInfo**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetalgorithminfo)

</dd> <dt>

<span data-ttu-id="67ae9-114"><span id="Digest_Method_functions"></span><span id="digest_method_functions"></span><span id="DIGEST_METHOD_FUNCTIONS"></span>Funzioni del metodo digest</span><span class="sxs-lookup"><span data-stu-id="67ae9-114"><span id="Digest_Method_functions"></span><span id="digest_method_functions"></span><span id="DIGEST_METHOD_FUNCTIONS"></span>Digest Method functions</span></span>
</dt> <dd>

-   [<span data-ttu-id="67ae9-115">**CryptXmlDllCloseDigest**</span><span class="sxs-lookup"><span data-stu-id="67ae9-115">**CryptXmlDllCloseDigest**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllclosedigest)
-   [<span data-ttu-id="67ae9-116">**CryptXmlDllCreateDigest**</span><span class="sxs-lookup"><span data-stu-id="67ae9-116">**CryptXmlDllCreateDigest**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatedigest)
-   [<span data-ttu-id="67ae9-117">**CryptXmlDllDigestData**</span><span class="sxs-lookup"><span data-stu-id="67ae9-117">**CryptXmlDllDigestData**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldlldigestdata)
-   [<span data-ttu-id="67ae9-118">**CryptXmlDllFinalizeDigest**</span><span class="sxs-lookup"><span data-stu-id="67ae9-118">**CryptXmlDllFinalizeDigest**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllfinalizedigest)

</dd> <dt>

<span data-ttu-id="67ae9-119"><span id="Signature_Method_Functions"></span><span id="signature_method_functions"></span><span id="SIGNATURE_METHOD_FUNCTIONS"></span>Funzioni metodo di firma</span><span class="sxs-lookup"><span data-stu-id="67ae9-119"><span id="Signature_Method_Functions"></span><span id="signature_method_functions"></span><span id="SIGNATURE_METHOD_FUNCTIONS"></span>Signature Method Functions</span></span>
</dt> <dd>

-   [<span data-ttu-id="67ae9-120">**CryptXmlDllSignData**</span><span class="sxs-lookup"><span data-stu-id="67ae9-120">**CryptXmlDllSignData**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllsigndata)
-   [<span data-ttu-id="67ae9-121">**CryptXmlDllVerifySignature**</span><span class="sxs-lookup"><span data-stu-id="67ae9-121">**CryptXmlDllVerifySignature**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllverifysignature)
-   [<span data-ttu-id="67ae9-122">**CryptXmlDllCreateKey**</span><span class="sxs-lookup"><span data-stu-id="67ae9-122">**CryptXmlDllCreateKey**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatekey)
-   [<span data-ttu-id="67ae9-123">**CryptXmlDllEncodeKeyValue**</span><span class="sxs-lookup"><span data-stu-id="67ae9-123">**CryptXmlDllEncodeKeyValue**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllencodekeyvalue)

</dd> <dt>

<span data-ttu-id="67ae9-124"><span id="For_algorithms_with_default_encoded_parameters"></span><span id="for_algorithms_with_default_encoded_parameters"></span><span id="FOR_ALGORITHMS_WITH_DEFAULT_ENCODED_PARAMETERS"></span>Per gli algoritmi con parametri codificati predefiniti</span><span class="sxs-lookup"><span data-stu-id="67ae9-124"><span id="For_algorithms_with_default_encoded_parameters"></span><span id="for_algorithms_with_default_encoded_parameters"></span><span id="FOR_ALGORITHMS_WITH_DEFAULT_ENCODED_PARAMETERS"></span>For algorithms with default encoded parameters</span></span>
</dt> <dd>

-   [<span data-ttu-id="67ae9-125">**CryptXmlDllEncodeAlgorithm**</span><span class="sxs-lookup"><span data-stu-id="67ae9-125">**CryptXmlDllEncodeAlgorithm**</span></span>](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllencodealgorithm)

</dd> </dl>

<span data-ttu-id="67ae9-126">Le DLL dell'estensione di crittografia sono registrate a livello di sistema.</span><span class="sxs-lookup"><span data-stu-id="67ae9-126">Cryptographic extension DLLs are registered on a system-wide basis.</span></span> <span data-ttu-id="67ae9-127">Per la registrazione di una DLL di estensione crittografica sono necessari privilegi di amministratore.</span><span class="sxs-lookup"><span data-stu-id="67ae9-127">Administrator privileges are required to register a cryptographic extension DLL.</span></span>

<span data-ttu-id="67ae9-128">Tutte le estensioni crittografiche CryptXML sono registrate dal valore URI impostato nel campo **SignatureMethod** o attributo dell'algoritmo dell'elemento **DigestMethod** .</span><span class="sxs-lookup"><span data-stu-id="67ae9-128">All CryptXML cryptographic extensions are registered by the URI value set in the **SignatureMethod** or the algorithm attribute field of the **DigestMethod** element.</span></span>

<span data-ttu-id="67ae9-129">I percorsi del registro di sistema per le DLL di estensione sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="67ae9-129">The registry paths for the extension DLLs are as follows:</span></span>

<dl> <dt>

<span data-ttu-id="67ae9-130"><span id="32-bit"></span><span id="32-BIT"></span>32 bit</span><span class="sxs-lookup"><span data-stu-id="67ae9-130"><span id="32-bit"></span><span id="32-BIT"></span>32-bit</span></span>
</dt> <dd>

<span data-ttu-id="67ae9-131">**HKEY \_ \_Computer locale** \\ **software** \\ **Microsoft** \\ **Cryptography** \\ **CryptXML** \\ **URI** \\ *{URI}*</span><span class="sxs-lookup"><span data-stu-id="67ae9-131">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Cryptography**\\**CryptXML**\\**URI**\\ *{uri}*</span></span>

</dd> <dt>

<span data-ttu-id="67ae9-132"><span id="64-bit"></span><span id="64-BIT"></span>64 bit</span><span class="sxs-lookup"><span data-stu-id="67ae9-132"><span id="64-bit"></span><span id="64-BIT"></span>64-bit</span></span>
</dt> <dd>

<span data-ttu-id="67ae9-133">**HKEY \_ \_Computer locale** \\ **software** \\ **Microsoft** \\ **Cryptography** \\ **CryptXML** \\ **URI** \\ *{URI}*</span><span class="sxs-lookup"><span data-stu-id="67ae9-133">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Cryptography**\\**CryptXML**\\**URI**\\ *{uri}*</span></span>

<span data-ttu-id="67ae9-134">**HKEY \_ \_Computer locale** \\ **software** \\ **WOW6432NODE** \\ **Microsoft** \\ **Cryptography** \\ **CryptXML** \\ **URI** \\ *{URI}*</span><span class="sxs-lookup"><span data-stu-id="67ae9-134">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**WOW6432NODE**\\**Microsoft**\\**Cryptography**\\**CryptXML**\\**URI**\\ *{uri}*</span></span>

</dd> </dl>

<span data-ttu-id="67ae9-135">Ogni chiave contiene le impostazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="67ae9-135">Each key contains the following settings.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="67ae9-136">Nome</span><span class="sxs-lookup"><span data-stu-id="67ae9-136">Name</span></span></th>
<th><span data-ttu-id="67ae9-137">Tipo</span><span class="sxs-lookup"><span data-stu-id="67ae9-137">Type</span></span></th>
<th><span data-ttu-id="67ae9-138">Data</span><span class="sxs-lookup"><span data-stu-id="67ae9-138">Data</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="67ae9-139">DLL</span><span class="sxs-lookup"><span data-stu-id="67ae9-139">DLL</span></span><br/></td>
<td><span data-ttu-id="67ae9-140">Stringa espandibile</span><span class="sxs-lookup"><span data-stu-id="67ae9-140">Expandable string</span></span><br/></td>
<td><span data-ttu-id="67ae9-141">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="67ae9-141">Required.</span></span><br/><span data-ttu-id="67ae9-142">Percorso assoluto della DLL del provider di crittografia XML.</span><span class="sxs-lookup"><span data-stu-id="67ae9-142">The absolute path to the XML Cryptographic Provider DLL.</span></span>
<blockquote>
<p><span data-ttu-id="67ae9-143"><b>Nota: </b> È consigliabile che le DLL di estensione crittografiche si trovino in directory che possono essere scritte solo da applicazioni con privilegi amministrativi.</span><span class="sxs-lookup"><span data-stu-id="67ae9-143"><b>Note: </b>We recommend that cryptographic extension DLLs be located in directories that can only be written to by applications with administrative privilege.</span></span></p>
<p><span data-ttu-id="67ae9-144"><a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya"><strong>LoadLibrary</strong></a> viene utilizzato per caricare la DLL dell'estensione di crittografia.</span><span class="sxs-lookup"><span data-stu-id="67ae9-144"><a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya"><strong>LoadLibrary</strong></a> is used to load the cryptographic extension DLL.</span></span><br/></p>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67ae9-145">Nome</span><span class="sxs-lookup"><span data-stu-id="67ae9-145">Name</span></span><br/></td>
<td><span data-ttu-id="67ae9-146"><strong>Stringa</strong></span><span class="sxs-lookup"><span data-stu-id="67ae9-146"><strong>String</strong></span></span></td>
<td><span data-ttu-id="67ae9-147">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="67ae9-147">Optional.</span></span><br/> <span data-ttu-id="67ae9-148">Nome visualizzato associato a questo URI.</span><span class="sxs-lookup"><span data-stu-id="67ae9-148">The display name associated with this URI.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67ae9-149">GroupId</span><span class="sxs-lookup"><span data-stu-id="67ae9-149">GroupId</span></span><br/></td>
<td><span data-ttu-id="67ae9-150"><strong>DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="67ae9-150"><strong>DWORD</strong></span></span></td>
<td><span data-ttu-id="67ae9-151">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="67ae9-151">Required.</span></span><br/> <span data-ttu-id="67ae9-152">Identificatore di gruppo associato a questo algoritmo di crittografia.</span><span class="sxs-lookup"><span data-stu-id="67ae9-152">The group identifier associated with this cryptographic algorithm.</span></span> <span data-ttu-id="67ae9-153">I valori possibili sono i seguenti:<strong>CRYPT_XML_GROUP_ID_HASH</strong> \ <strong></strong> = 1</span><span class="sxs-lookup"><span data-stu-id="67ae9-153">Possible values include the following:<strong>CRYPT_XML_GROUP_ID_HASH</strong>\<strong></strong> = 1</span></span><br/><span data-ttu-id="67ae9-154"><strong></strong> \ CRYPT_XML_GROUP_ID_SIGN <strong></strong> = 2</span><span class="sxs-lookup"><span data-stu-id="67ae9-154"><strong>CRYPT_XML_GROUP_ID_SIGN</strong>\<strong></strong> = 2</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67ae9-155">CNGAlgid</span><span class="sxs-lookup"><span data-stu-id="67ae9-155">CNGAlgid</span></span><br/></td>
<td><span data-ttu-id="67ae9-156"><strong>Stringa</strong></span><span class="sxs-lookup"><span data-stu-id="67ae9-156"><strong>String</strong></span></span></td>
<td><span data-ttu-id="67ae9-157">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="67ae9-157">Required.</span></span><br/> <span data-ttu-id="67ae9-158">Nome dell'algoritmo CNG da passare alle funzioni BCrypt o NCrypt.</span><span class="sxs-lookup"><span data-stu-id="67ae9-158">The CNG algorithm name to be passed to BCrypt or NCrypt functions.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67ae9-159">CNGExtraAlgid</span><span class="sxs-lookup"><span data-stu-id="67ae9-159">CNGExtraAlgid</span></span><br/></td>
<td><span data-ttu-id="67ae9-160"><strong>Stringa</strong></span><span class="sxs-lookup"><span data-stu-id="67ae9-160"><strong>String</strong></span></span></td>
<td><span data-ttu-id="67ae9-161">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="67ae9-161">Optional.</span></span><br/> <span data-ttu-id="67ae9-162">Stringa di algoritmo aggiuntiva, diversa dalla stringa nel membro CNGAlgid, che può essere passata alle funzioni CNG.</span><span class="sxs-lookup"><span data-stu-id="67ae9-162">An extra algorithm string, other than the string in the CNGAlgid member, that can be passed to the CNG functions.</span></span><br/> <span data-ttu-id="67ae9-163">Per gli algoritmi di firma (CRYPT_XML_GROUP_ID_SIGN), questo membro è la stringa dell'algoritmo a chiave pubblica da passare alle funzioni CNG.</span><span class="sxs-lookup"><span data-stu-id="67ae9-163">For the signature algorithms (CRYPT_XML_GROUP_ID_SIGN), this member is the public key algorithm string to pass to the CNG functions.</span></span><br/> <span data-ttu-id="67ae9-164">Per gli altri valori di GroupId, impostare il membro <strong>pwszCNGExtraAlgid</strong> sulla stringa vuota, L &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="67ae9-164">For the other values of GroupId, set the <strong>pwszCNGExtraAlgid</strong> member to the empty string, L&quot;&quot;.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="67ae9-165">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="67ae9-165">Related topics</span></span>

<dl> <span data-ttu-id="67ae9-166"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="67ae9-166"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="67ae9-167">Algoritmi di crittografia per la firma digitale XML</span><span class="sxs-lookup"><span data-stu-id="67ae9-167">XML Digital Signature Cryptographic Algorithms</span></span>](xml-digital-signature-cryptographic-algorithms.md)
</dt> </dl>

 

 
