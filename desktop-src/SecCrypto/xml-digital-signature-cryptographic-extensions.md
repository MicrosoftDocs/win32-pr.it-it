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
# <a name="xml-digital-signature-cryptographic-extensions"></a>Estensioni crittografiche della firma digitale XML

CryptXML consente agli sviluppatori di estendere gli algoritmi crittografici supportati in modo nativo mediante la registrazione di una DLL di estensione crittografica a livello di sistema. Le DLL di estensione estendono gli algoritmi supportati dagli elementi XML **SignatureMethod** e **DigestMethod** . Le DLL di estensione possono supportare algoritmi che codificano parametri aggiuntivi nella firma digitale XML.

Tutte le DLL delle estensioni devono supportare la funzione [**CryptXmlDllGetInterface**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface) , che restituisce un puntatore a una struttura di [**\_ \_ \_ interfaccia di crittografia XML Crypt**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_cryptographic_interface) . Questa struttura fornisce i puntatori a funzione per le funzioni di estensione crittografiche implementate. Le funzioni supportate dipendono dal tipo di algoritmo di crittografia supportato e dal fatto che l'algoritmo debba codificare i parametri nella firma digitale XML.

Le funzioni delle estensioni crittografiche includono i seguenti puntatori a funzione:

<dl> <dt>

<span id="Required_functions"></span><span id="required_functions"></span><span id="REQUIRED_FUNCTIONS"></span>Funzioni obbligatorie
</dt> <dd>

-   [**CryptXmlDllGetInterface**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface)
-   [**CryptXmlDllGetAlgorithmInfo**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetalgorithminfo)

</dd> <dt>

<span id="Digest_Method_functions"></span><span id="digest_method_functions"></span><span id="DIGEST_METHOD_FUNCTIONS"></span>Funzioni del metodo digest
</dt> <dd>

-   [**CryptXmlDllCloseDigest**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllclosedigest)
-   [**CryptXmlDllCreateDigest**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatedigest)
-   [**CryptXmlDllDigestData**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldlldigestdata)
-   [**CryptXmlDllFinalizeDigest**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllfinalizedigest)

</dd> <dt>

<span id="Signature_Method_Functions"></span><span id="signature_method_functions"></span><span id="SIGNATURE_METHOD_FUNCTIONS"></span>Funzioni metodo di firma
</dt> <dd>

-   [**CryptXmlDllSignData**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllsigndata)
-   [**CryptXmlDllVerifySignature**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllverifysignature)
-   [**CryptXmlDllCreateKey**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatekey)
-   [**CryptXmlDllEncodeKeyValue**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllencodekeyvalue)

</dd> <dt>

<span id="For_algorithms_with_default_encoded_parameters"></span><span id="for_algorithms_with_default_encoded_parameters"></span><span id="FOR_ALGORITHMS_WITH_DEFAULT_ENCODED_PARAMETERS"></span>Per gli algoritmi con parametri codificati predefiniti
</dt> <dd>

-   [**CryptXmlDllEncodeAlgorithm**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllencodealgorithm)

</dd> </dl>

Le DLL dell'estensione di crittografia sono registrate a livello di sistema. Per la registrazione di una DLL di estensione crittografica sono necessari privilegi di amministratore.

Tutte le estensioni crittografiche CryptXML sono registrate dal valore URI impostato nel campo **SignatureMethod** o attributo dell'algoritmo dell'elemento **DigestMethod** .

I percorsi del registro di sistema per le DLL di estensione sono i seguenti:

<dl> <dt>

<span id="32-bit"></span><span id="32-BIT"></span>32 bit
</dt> <dd>

**HKEY \_ \_Computer locale** \\ **software** \\ **Microsoft** \\ **Cryptography** \\ **CryptXML** \\ **URI** \\ *{URI}*

</dd> <dt>

<span id="64-bit"></span><span id="64-BIT"></span>64 bit
</dt> <dd>

**HKEY \_ \_Computer locale** \\ **software** \\ **Microsoft** \\ **Cryptography** \\ **CryptXML** \\ **URI** \\ *{URI}*

**HKEY \_ \_Computer locale** \\ **software** \\ **WOW6432NODE** \\ **Microsoft** \\ **Cryptography** \\ **CryptXML** \\ **URI** \\ *{URI}*

</dd> </dl>

Ogni chiave contiene le impostazioni seguenti.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Nome</th>
<th>Tipo</th>
<th>Data</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DLL<br/></td>
<td>Stringa espandibile<br/></td>
<td>Obbligatorio.<br/>Percorso assoluto della DLL del provider di crittografia XML.
<blockquote>
<p><b>Nota: </b> È consigliabile che le DLL di estensione crittografiche si trovino in directory che possono essere scritte solo da applicazioni con privilegi amministrativi.</p>
<p><a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya"><strong>LoadLibrary</strong></a> viene utilizzato per caricare la DLL dell'estensione di crittografia.<br/></p>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Nome<br/></td>
<td><strong>Stringa</strong></td>
<td>facoltativo.<br/> Nome visualizzato associato a questo URI.<br/></td>
</tr>
<tr class="odd">
<td>GroupId<br/></td>
<td><strong>DWORD</strong></td>
<td>Obbligatorio.<br/> Identificatore di gruppo associato a questo algoritmo di crittografia. I valori possibili sono i seguenti:<strong>CRYPT_XML_GROUP_ID_HASH</strong> \ <strong></strong> = 1<br/><strong></strong> \ CRYPT_XML_GROUP_ID_SIGN <strong></strong> = 2<br/></td>
</tr>
<tr class="even">
<td>CNGAlgid<br/></td>
<td><strong>Stringa</strong></td>
<td>Obbligatorio.<br/> Nome dell'algoritmo CNG da passare alle funzioni BCrypt o NCrypt.<br/></td>
</tr>
<tr class="odd">
<td>CNGExtraAlgid<br/></td>
<td><strong>Stringa</strong></td>
<td>facoltativo.<br/> Stringa di algoritmo aggiuntiva, diversa dalla stringa nel membro CNGAlgid, che può essere passata alle funzioni CNG.<br/> Per gli algoritmi di firma (CRYPT_XML_GROUP_ID_SIGN), questo membro è la stringa dell'algoritmo a chiave pubblica da passare alle funzioni CNG.<br/> Per gli altri valori di GroupId, impostare il membro <strong>pwszCNGExtraAlgid</strong> sulla stringa vuota, L &quot; &quot; . <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>


</dt> <dt>

[Algoritmi di crittografia per la firma digitale XML](xml-digital-signature-cryptographic-algorithms.md)
</dt> </dl>

 

 
