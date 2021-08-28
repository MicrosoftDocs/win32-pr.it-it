---
description: CryptXML consente agli sviluppatori di estendere gli algoritmi di crittografia supportati in modo nativo registrando una DLL di estensione crittografica a livello di sistema.
ms.assetid: b0625481-660a-4fd5-ba15-d532998f95a6
title: Estensioni crittografiche per la firma digitale XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41bf0f2d99b34d59e9817f8568b03be20e72dda1
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474937"
---
# <a name="xml-digital-signature-cryptographic-extensions"></a>Estensioni crittografiche per la firma digitale XML

CryptXML consente agli sviluppatori di estendere gli algoritmi di crittografia supportati in modo nativo registrando una DLL di estensione crittografica a livello di sistema. Le DLL di estensione estendono gli algoritmi supportati dagli elementi XML **SignatureMethod** e **DigestMethod.** Le DLL di estensione possono supportare algoritmi che codificano parametri aggiuntivi nella firma digitale XML.

Tutte le DLL delle estensioni devono supportare la funzione [**CryptXmlDllGetInterface,**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface) che restituisce un puntatore a una [**struttura CRYPT \_ XML \_ CRYPTOGRAPHIC \_ INTERFACE.**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_cryptographic_interface) Questa struttura fornisce puntatori a funzione per le funzioni di estensione crittografiche implementate. Le funzioni supportate dipendono dal tipo di algoritmo di crittografia supportato e dal fatto che l'algoritmo deve codificare i parametri nella firma digitale XML.

Le funzioni delle estensioni crittografiche includono i puntatori a funzione seguenti:

<dl> <dt>

<span id="Required_functions"></span><span id="required_functions"></span><span id="REQUIRED_FUNCTIONS"></span>Funzioni obbligatorie
</dt> <dd>

-   [**CryptXmlDllGetInterface**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface)
-   [**CryptXmlDllGetAlgorithmInfo**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetalgorithminfo)

</dd> <dt>

<span id="Digest_Method_functions"></span><span id="digest_method_functions"></span><span id="DIGEST_METHOD_FUNCTIONS"></span>Funzioni del metodo Digest
</dt> <dd>

-   [**CryptXmlDllCloseDigest**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllclosedigest)
-   [**CryptXmlDllCreateDigest**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatedigest)
-   [**CryptXmlDllDigestData**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldlldigestdata)
-   [**CryptXmlDllFinalizeDigest**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllfinalizedigest)

</dd> <dt>

<span id="Signature_Method_Functions"></span><span id="signature_method_functions"></span><span id="SIGNATURE_METHOD_FUNCTIONS"></span>Funzioni del metodo di firma
</dt> <dd>

-   [**CryptXmlDllSignData**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllsigndata)
-   [**CryptXmlDllVerifySignature**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllverifysignature)
-   [**CryptXmlDllCreateKey**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatekey)
-   [**CryptXmlDllEncodeKeyValue**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllencodekeyvalue)

</dd> <dt>

<span id="For_algorithms_with_default_encoded_parameters"></span><span id="for_algorithms_with_default_encoded_parameters"></span><span id="FOR_ALGORITHMS_WITH_DEFAULT_ENCODED_PARAMETERS"></span>Per algoritmi con parametri codificati predefiniti
</dt> <dd>

-   [**CryptXmlDllEncodeAlgorithm**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllencodealgorithm)

</dd> </dl>

Le DLL di estensione crittografica vengono registrate a livello di sistema. Per registrare una DLL di estensione crittografica sono necessari privilegi di amministratore.

Tutte le estensioni di crittografia CryptXML vengono registrate dal valore URI impostato nel **campo SignatureMethod** o dell'attributo algorithm dell'elemento **DigestMethod.**

I percorsi del Registro di sistema per le DLL di estensione sono i seguenti:

<dl> <dt>

<span id="32-bit"></span><span id="32-BIT"></span>32 bit
</dt> <dd>

**HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Cryptography** \\ **CryptXML** \\ **URI** \\ *{uri}*

</dd> <dt>

<span id="64-bit"></span><span id="64-BIT"></span>64 bit
</dt> <dd>

**HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Cryptography** \\ **CryptXML** \\ **URI** \\ *{uri}*

**HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **WOW6432NODE** \\ **Microsoft** \\ **Cryptography** \\ **CryptXML** \\ **URI** \\ *{uri}*

</dd> </dl>

Ogni chiave contiene le impostazioni seguenti.




| Nome | Tipo | Dati | 
|------|------|------|
| DLL<br /> | Stringa espandibile<br /> | Obbligatorio.<br />Percorso assoluto della DLL del provider del servizio di crittografia XML.<blockquote><p><b>Nota: </b> È consigliabile che le DLL delle estensioni crittografiche si trovino in directory in cui possono essere scritte solo applicazioni con privilegi amministrativi.</p><p><a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya"><strong>LoadLibrary viene</strong></a> usato per caricare la DLL dell'estensione di crittografia.<br /></p></blockquote><br /> | 
| Nome<br /> | <strong>Stringa</strong> | facoltativo.<br /> Nome visualizzato associato a questo URI.<br /> | 
| GroupId<br /> | <strong>DWORD</strong> | Obbligatorio.<br /> Identificatore di gruppo associato a questo algoritmo di crittografia. I valori possibili sono i seguenti:<strong>CRYPT_XML_GROUP_ID_HASH</strong> \<strong> </strong> = 1<br /><strong></strong> \<strong> CRYPT_XML_GROUP_ID_SIGN </strong> = 2<br /> | 
| CNGAlgid<br /> | <strong>Stringa</strong> | Obbligatorio.<br /> Nome dell'algoritmo CNG da passare alle funzioni BCrypt o NCrypt.<br /> | 
| CNGExtraAlgid<br /> | <strong>Stringa</strong> | facoltativo.<br /> Stringa di algoritmo aggiuntiva, diversa dalla stringa nel membro CNGAlgid, che può essere passata alle funzioni CNG.<br /> Per gli algoritmi di firma (CRYPT_XML_GROUP_ID_SIGN), questo membro è la stringa dell'algoritmo a chiave pubblica da passare alle funzioni CNG.<br /> Per gli altri valori di GroupId, impostare il membro <strong>pwszCNGExtraAlgid</strong> sulla stringa vuota L"". <br /> | 




 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>


</dt> <dt>

[Algoritmi di crittografia con firma digitale XML](xml-digital-signature-cryptographic-algorithms.md)
</dt> </dl>

 

 
