---
description: Definisce i codici di errore restituiti da CAPICOM.
ms.assetid: e72b8290-b482-4629-8b87-5a15677865a6
title: CAPICOM_ERROR_CODE enumerazione (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ERROR_CODE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: abdd2556ace3e3c3c82ccdeedc907d77f9ce1702
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480697"
---
# <a name="capicom_error_code-enumeration"></a>Enumerazione CAPICOM \_ ERROR \_ CODE

Il **tipo di enumerazione \_ CAPICOM ERROR \_ CODE** definisce i codici di errore restituiti da CAPICOM.

> [!Note]  
> Visual Basic Gli errori di Scripting Edition restituiscono un **valore Err.number** maggiore di zero. Per questi errori, **i valori Err.Description** forniscono informazioni sulla causa dell'errore. Oltre agli errori Visual Basic Scripting Edition, gli errori CAPICOM restituiscono i codici definiti da **CAPICOM \_ ERROR \_ CODE**.

 

## <a name="members"></a>Membri




| Membro | Descrizione | valore | 
|--------|-------------|-------|
| <strong>CAPICOM_E_ENCODE_INVALID_TYPE</strong> | È stato usato un tipo di codifica non valido.<br /> L'elenco seguente mostra i tipi di codifica validi:<ul><li>CAPICOM_ENCODE_ANY</li><li>CAPICOM_ENCODE_BASE64</li><li>CAPICOM_ENCODE_BINARY</li></ul><br /> | 0x80880100 | 
| <strong>CAPICOM_E_EKU_INVALID_OID</strong> | Impossibile impostare la proprietà <a href="eku-oid.md"><strong>OID</strong></a> <a href="eku.md"><strong>dell'oggetto EKU</strong></a> perché la <a href="eku-name.md"><strong>proprietà Name</strong></a> non è impostata su CAPICOM_EKU_OTHER.<br /> Impostare la <a href="eku-name.md"><strong>proprietà Name</strong></a> su CAPICOM_EKU_OTHER prima di impostare la <a href="eku-oid.md"><strong>proprietà OID.</strong></a><br /> | 0x80880200 | 
| <strong>CAPICOM_E_EKU_OID_NOT_INITIALIZED</strong> | La <a href="eku-oid.md"><strong>proprietà OID</strong></a> dell'oggetto <a href="eku.md"><strong>EKU</strong></a> non è stata inizializzata. <br /> Impostare la <a href="eku-name.md"><strong>proprietà Name</strong></a> su un valore diverso da CAPICOM_EKU_OTHER oppure impostare la proprietà <strong>Name</strong> su CAPICOM_EKU_OTHER e la <a href="eku-oid.md"><strong>proprietà OID</strong></a> su un valore.<br /> | 0x80880201 | 
| <strong>CAPICOM_E_CERTIFICATE_NOT_INITIALIZED</strong> | <a href="certificate.md"><strong>L'oggetto</strong></a> Certificato non è stato inizializzato.<br /> In genere, questo codice di errore viene restituito quando viene creata un'istanza di un oggetto <a href="certificate.md"><strong>Certificate</strong></a> ma non è associata a un certificato digitale. Per associare l'oggetto a un certificato digitale, assegnarlo a un oggetto <strong>Certificato</strong> esistente o chiamare il <a href="certificate-import.md"><strong>metodo Import.</strong></a><br /> | 0x80880210 | 
| <strong>CAPICOM_E_CERTIFICATE_NO_PRIVATE_KEY</strong> | <a href="certificate.md"><strong>All'oggetto</strong></a> Certificato non è associata una chiave privata.<br /> Questo codice di errore viene restituito quando si tenta di firmare i dati usando la <a href="signer.md"><strong></strong></a> chiave privata del firmatario, ma l'oggetto <a href="certificate.md"><strong>Certificato</strong></a> associato all'oggetto Firmatario non può essere usato per l'operazione di firma.<br /> | 0x80880211 | 
| <strong>CAPICOM_E_CHAIN_NOT_BUILT</strong> | <a href="chain.md"><strong>L'oggetto Chain</strong></a> non è stato inizializzato. <br /> Per inizializzare <a href="chain.md"><strong>l'oggetto Chain,</strong></a> chiamare il <a href="chain-build.md"><strong>metodo Build.</strong></a><br /> | 0x80880220 | 
| <strong>CAPICOM_E_STORE_NOT_OPENED</strong> | <a href="store.md"><strong>L'oggetto</strong></a> Store non è stato inizializzato. <br /> Per inizializzare <a href="store.md"><strong>l'oggetto Store,</strong></a> chiamare il <a href="store-open.md"><strong>metodo Open.</strong></a><br /> | 0x80880230 | 
| <strong>CAPICOM_E_STORE_EMPTY</strong> | <a href="store.md"><strong>L'oggetto</strong></a> Store non contiene <a href="certificate.md"><strong>oggetti</strong></a> Certificate.<br /> | 0x80880231 | 
| <strong>CAPICOM_E_STORE_INVALID_OPEN_MODE</strong> | Il <em>parametro OpenMode</em> del <a href="store-open.md"><strong>metodo Store.Open</strong></a> non contiene un valore valido di CAPICOM_STORE_OPEN_MODE.<br /> L'elenco seguente mostra i valori validi di CAPICOM_STORE_OPEN_MODE:<ul><li>CAPICOM_STORE_OPEN_READ_ONLY</li><li>CAPICOM_STORE_OPEN_READ_WRITE</li><li>CAPICOM_STORE_OPEN_MAXIMUM_ALLOWED</li><li>CAPICOM_STORE_OPEN_EXISTING_ONLY</li><li>CAPICOM_STORE_OPEN_INCLUDE_ARCHIVED</li></ul><br /> | 0x80880232 | 
| <strong>CAPICOM_E_STORE_INVALID_SAVE_AS_TYPE</strong> | Il <em>valore SaveAs</em> passato al <a href="store-export.md"><strong>metodo Export</strong></a> dell'oggetto <a href="store.md"><strong>Store</strong></a> non è valido. <br /> L'elenco seguente mostra i <em>valori SaveAs</em> validi:<ul><li>CAPICOM_STORE_SAVE_AS_SERIALIZED</li><li>CAPICOM_STORE_SAVE_AS_PKCS7</li></ul><br /> | 0x80880233 | 
| <strong>CAPICOM_E_ATTRIBUTE_NAME_NOT_INITIALIZED</strong> | La <a href="attribute-name.md"><strong>proprietà Name</strong></a> dell'oggetto <a href="attribute.md"><strong>Attribute</strong></a> non è stata inizializzata. <br /> Impostare la <a href="attribute-name.md"><strong>proprietà Name.</strong></a><br /> | 0x80880240 | 
| <strong>CAPICOM_E_ATTRIBUTE_VALUE_NOT_INITIALIZED</strong> | La <a href="attribute-value.md"><strong>proprietà Value</strong></a> dell'oggetto <a href="attribute.md"><strong>Attribute</strong></a> non è stata inizializzata. <br /> Impostare la <a href="attribute-value.md"><strong>proprietà Value.</strong></a><br /> | 0x80880241 | 
| <strong>CAPICOM_E_ATTRIBUTE_INVALID_NAME</strong> | La <a href="attribute-name.md"><strong>proprietà Name</strong></a> dell'oggetto <a href="attribute.md"><strong>Attribute</strong></a> non è valida. <br /> L'elenco seguente mostra i nomi degli attributi validi:<ul><li>CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME</li><li>CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_NAME</li><li>CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_DESCRIPTION</li></ul><br /> | 0x80880242 | 
| <strong>CAPICOM_E_ATTRIBUTE_INVALID_VALUE</strong> | La <a href="attribute-value.md"><strong>proprietà Value</strong></a> dell'oggetto <a href="attribute.md"><strong>Attribute</strong></a> non è valida perché il tipo di dati non corrisponde al tipo di dati indicato dalla <strong>proprietà Name.</strong> <br /> Ad esempio, se la <a href="attribute-value.md"><strong>proprietà Name</strong></a> è impostata su CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME, il tipo di dati deve essere <strong>DATE</strong>.<br /> | 0x80880243 | 
| <strong>CAPICOM_E_SIGNER_NOT_INITIALIZED</strong> | <a href="signer.md"><strong>L'oggetto Firmatario</strong></a> non è stato inizializzato. <br /> Per inizializzare <a href="signer.md"><strong>l'oggetto Signer,</strong></a> impostare la <a href="signer-certificate.md"><strong>proprietà Certificate.</strong></a><br /> | 0x80880250 | 
| <strong>CAPICOM_E_SIGNER_NOT_FOUND</strong> | Impossibile trovare il firmatario <a href="signeddata.md"><strong>nell'oggetto SignedData.</strong></a> <br /> In genere, questa operazione non si verifica con <a href="signeddata.md"><strong>un oggetto SignedData</strong></a> creato da CAPICOM. Tuttavia, se <strong>l'oggetto SignedData</strong> è stato creato da un prodotto di terze parti, il certificato del firmatario potrebbe non essere incluso nella PKCS #7 struttura.<br /> | 0x80880251 | 
| <strong>CAPICOM_E_SIGNER_NO_CHAIN</strong> | Impossibile <a href="chain.md"><strong>trovare</strong></a> un oggetto Chain nell'oggetto <a href="signer.md"><strong>Firmatario.</strong></a><br /> | 0x80880252 // v2.0 | 
| <strong>CAPICOM_E_SIGNER_INVALID_USAGE</strong> | Viene effettuato un tentativo di usare il firmatario in un modo non valido.<br /> | 0x80880253 //v2.0 | 
| <strong>CAPICOM_E_SIGN_NOT_INITIALIZED</strong> | <a href="signeddata.md"><strong>L'oggetto SignedData</strong></a> non è stato inizializzato. <br /> Per inizializzare <a href="signeddata.md"><strong>l'oggetto SignedData,</strong></a> impostare la <a href="signeddata-content.md"><strong>proprietà Content</strong></a> o chiamare il <a href="signeddata-verify.md"><strong>metodo Verify.</strong></a><br /> | 0x80880260 | 
| <strong>CAPICOM_E_SIGN_INVALID_TYPE</strong> | <a href="signeddata.md"><strong>L'oggetto SignedData</strong></a> contiene un tipo non valido. <br /> In genere, ciò si verifica quando si tenta di verificare un messaggio in busta con un <a href="signeddata.md"><strong>oggetto SignedData</strong></a> o viceversa.<br /> | 0x80880261 | 
| <strong>CAPICOM_E_SIGN_NOT_SIGNED</strong> | <a href="signeddata.md"><strong>L'oggetto SignedData</strong></a> non è stato firmato. <br /> Per firmare <a href="signeddata.md"><strong>l'oggetto SignedData,</strong></a> chiamare il <a href="signeddata-sign.md"><strong>metodo Sign.</strong></a><br /> | 0x80880262 | 
| <strong>CAPICOM_E_INVALID_ALGORITHM</strong> | Il valore dell'algoritmo <a href="algorithm-name.md"><strong>per la</strong></a> proprietà Name <a href="algorithm.md"><strong>dell'oggetto Algorithm</strong></a> non è valido. <br /> L'elenco seguente mostra i valori validi dell'algoritmo per la <a href="algorithm-name.md"><strong>proprietà</strong></a> Name:<ul><li>CAPICOM_ENCRYPTION_ALGORITHM_RC2</li><li>CAPICOM_ENCRYPTION_ALGORITHM_RC4</li><li>CAPICOM_ENCRYPTION_ALGORITHM_DES</li><li>CAPICOM_ENCRYPTION_ALGORITHM_3DES</li></ul><br /> | 0x80880270 | 
| <strong>CAPICOM_E_INVALID_KEY_LENGTH</strong> | Il valore della lunghezza della chiave <a href="algorithm-keylength.md"><strong>per la proprietà KeyLength</strong></a> dell'oggetto <a href="algorithm.md"><strong>Algorithm</strong></a> non è valido. <br /> L'elenco seguente mostra i valori di lunghezza di chiave validi per la <a href="algorithm-keylength.md"><strong>proprietà KeyLength:</strong></a><ul><li>CAPICOM_ENCRYPTION_KEY_LENGTH_MAXIMUM</li><li>CAPICOM_ENCRYPTION_KEY_LENGTH_40_BITS</li><li>CAPICOM_ENCRYPTION_KEY_LENGTH_56_BITS</li><li>CAPICOM_ENCRYPTION_KEY_LENGTH_128_BITS</li></ul><br /> | 0x80880271 | 
| <strong>CAPICOM_E_ENVELOP_NOT_INITIALIZED</strong> | <a href="envelopeddata.md"><strong>L'oggetto EnvelopedData</strong></a> non è stato inizializzato. <br /> Per inizializzare <a href="envelopeddata.md"><strong>l'oggetto EnvelopedData,</strong></a> impostare la <a href="envelopeddata-content.md"><strong>proprietà Content</strong></a> o chiamare il <a href="envelopeddata-decrypt.md"><strong>metodo Decrypt.</strong></a><br /> | 0x80880280 | 
| <strong>CAPICOM_E_ENVELOP_INVALID_TYPE</strong> | <a href="envelopeddata.md"><strong>L'oggetto EnvelopedData</strong></a> contiene un tipo non valido. <br /> In genere, ciò si verifica quando si tenta di verificare un messaggio firmato con un <a href="envelopeddata.md"><strong>oggetto EnvelopedData</strong></a> o viceversa.<br /> | 0x80880281 | 
| <strong>CAPICOM_E_ENVELOP_NO_RECIPIENT</strong> | Non è specificato alcun destinatario <a href="envelopeddata.md"><strong>nell'oggetto EnvelopedData</strong></a> quando viene chiamato il <a href="envelopeddata-encrypt.md"><strong>metodo Encrypt</strong></a> di un oggetto <strong>EnvelopedData.</strong> <br /> Per aggiungere un destinatario, chiamare il <a href="recipients-add.md"><strong>metodo Recipients.Add.</strong></a><br /> | 0x80880282 | 
| <strong>CAPICOM_E_ENVELOP_RECIPIENT_NOT_FOUND</strong> | Impossibile trovare il destinatario <a href="envelopeddata.md"><strong>nell'oggetto EnvelopedData.</strong></a> <br /> In genere, questa operazione non si verifica con <a href="envelopeddata.md"><strong>un oggetto EnvelopedData</strong></a> creato da CAPICOM. Tuttavia, se <strong>l'oggetto EnvelopedData</strong> è stato creato da un prodotto di terze parti, il certificato del destinatario potrebbe non essere incluso nella PKCS #7 sicurezza.<br /> | 0x80880283 | 
| <strong>CAPICOM_E_ENCRYPT_NOT_INITIALIZED</strong> | <a href="encrypteddata.md"><strong>L'oggetto EncryptedData</strong></a> non è stato inizializzato. <br /> Per inizializzare <a href="encrypteddata.md"><strong>l'oggetto EncryptedData,</strong></a> impostare la <a href="encrypteddata-content.md"><strong>proprietà Content</strong></a> o chiamare il <a href="encrypteddata-decrypt.md"><strong>metodo Decrypt.</strong></a><br /> | 0x80880290 | 
| <strong>CAPICOM_E_ENCRYPT_INVALID_TYPE</strong> | <a href="encrypteddata.md"><strong>L'oggetto EncryptedData</strong></a> non è un tipo valido. <br /> In genere, ciò significa che i dati sono danneggiati.<br /> | 0x80880291 | 
| <strong>CAPICOM_E_ENCRYPT_NO_SECRET</strong> | Il segreto di un <a href="encrypteddata.md"><strong>oggetto EncryptedData</strong></a> non è stato inizializzato. <br /> Per inizializzare il segreto di <a href="encrypteddata.md"><strong>un oggetto EncryptedData,</strong></a> chiamare il <a href="encrypteddata-setsecret.md"><strong>metodo SetSecret.</strong></a><br /> | 0x80880292 | 
| <strong>CAPICOM_E_PRIVATE_KEY_NOT_INITIALIZED</strong> | <a href="privatekey.md"><strong>L'oggetto PrivateKey</strong></a> non è stato inizializzato.<br /> | 0x80880300 // v2.0 | 
| <strong>CAPICOM_E_PRIVATE_KEY_NOT_EXPORTABLE</strong> | <a href="privatekey.md"><strong>L'oggetto PrivateKey</strong></a> non può essere esportato.<br /> | 0x80880301 // v2.0 | 
| <strong>CAPICOM_E_ENCODE_NOT_INITIALIZED</strong> | <a href="encodeddata.md"><strong>L'oggetto EncodedData</strong></a> non è stato inizializzato.<br /> | 0x80880320 // v2.0 | 
| <strong>CAPICOM_E_EXTENSION_NOT_INITIALIZED</strong> | <a href="extension.md"><strong>L'oggetto</strong></a> Extension non è stato inizializzato.<br /> | 0x80880330 // v2.0 | 
| <strong>CAPICOM_E_PROPERTY_NOT_INITIALIZED</strong> | La <a href="extendedproperty-propid.md"><strong>proprietà PropID</strong></a> dell'oggetto <a href="extendedproperty.md"><strong>ExtendedProperty</strong></a> non è stata inizializzata.<br /> | 0x80880340 // v2.0 | 
| <strong>CAPICOM_E_FIND_INVALID_TYPE</strong> | Il <em>parametro FindType</em> del <a href="certificates-find.md"><strong>metodo Certificates.Find</strong></a> non è un valore dell CAPICOM_CERTIFICATE_FIND_TYPE enumere. <a href="capicom-certificate-find-type.md"><strong></strong></a><br /> | 0x80880350 // v2.0 | 
| <strong>CAPICOM_E_FIND_INVALID_PREDEFINED_POLICY</strong> | I criteri predefiniti specificati per l'operazione di ricerca non sono validi.<br /> | 0x80880351 // v2.0 | 
| <strong>CAPICOM_E_CODE_NOT_INITIALIZED</strong> | <a href="signedcode.md"><strong>L'oggetto SignedCode</strong></a> non è stato inizializzato.<br /> | 0x80880360 // v2.0 | 
| <strong>CAPICOM_E_CODE_NOT_SIGNED</strong> | <a href="signedcode.md"><strong>L'oggetto SignedCode</strong></a> non è stato firmato.<br /> Per firmare <a href="signedcode.md"><strong>l'oggetto SignedCode,</strong></a> chiamare il <a href="signedcode-sign.md"><strong>metodo Sign.</strong></a><br /> | 0x80880361 // v2.0 | 
| <strong>CAPICOM_E_CODE_DESCRIPTION_NOT_INITIALIZED</strong> | La <a href="signedcode-description.md"><strong>proprietà Description</strong></a> dell'oggetto <a href="signedcode.md"><strong>SignedCode</strong></a> non è stata inizializzata.<br /> | 0x80880362 // v2.0 | 
| <strong>CAPICOM_E_CODE_DESCRIPTION_URL_NOT_INITIALIZED</strong> | La <a href="signedcode-descriptionurl.md"><strong>proprietà DescriptionURL</strong></a> dell'oggetto <a href="signedcode.md"><strong>SignedCode</strong></a> non è stata inizializzata.<br /> | 0x80880363 // v2.0 | 
| <strong>CAPICOM_E_CODE_INVALID_TIMESTAMP_URL</strong> | Il <em>parametro URL</em> del metodo <a href="signedcode-timestamp.md"><strong>SignedCode.Timestamp</strong></a> non è valido.<br /> | 0x80880364 // v2.0 | 
| <strong>CAPICOM_E_HASH_NO_DATA</strong> | <a href="hasheddata.md"><strong>L'oggetto HashedData</strong></a> non contiene dati.<br /> | 0x80880370 // v2.0 | 
| <strong>CAPICOM_E_INVALID_CONVERT_TYPE</strong> | Il tipo di conversione non è valido.<br /> | 0x80880380 // v2.0 | 
| <strong>CAPICOM_E_NOT_SUPPORTED</strong> | L'operazione richiesta non è supportata nella piattaforma corrente. <br /> | 0x80880900 | 
| <strong>CAPICOM_E_UI_DISABLED</strong> | Durante la firma, <a href="signer-certificate.md"><strong>la proprietà Certificate</strong></a> dell'oggetto <a href="signer.md"><strong>Signer</strong></a> non è stata impostata, ma la richiesta per il certificato utente è stata disabilitata. <br /> Abilitare la richiesta impostando la <a href="settings-enablepromptforcertificateui.md"><strong>proprietà EnablePromptForCertificateUI</strong></a> dell'oggetto <a href="settings.md"><strong>Impostazioni</strong></a> oppure impostare la <a href="signer-certificate.md"><strong>proprietà Certificate</strong></a> dell'oggetto <a href="signer.md"><strong>Signer.</strong></a><br /> | 0x80880901 | 
| <strong>CAPICOM_E_CANCELLED</strong> | L'operazione è stata annullata dall'utente. <br /> Ciò si verifica quando all'utente viene richiesta l'autorizzazione per eseguire una determinata operazione, ad esempio l'accesso alla chiave privata, e l'utente annulla l'operazione.<br /> | 0x80880902 | 
| <strong>CAPICOM_E_NOT_ALLOWED</strong> | L'operazione tentata non è consentita.<br /> Ad esempio, la modifica <a href="extendedproperty-propid.md"><strong>della proprietà PropID</strong></a> di un <a href="extendedproperty.md"><strong>oggetto ExtendedProperty</strong></a> non è consentita se l'oggetto è collegato a un certificato.<br /> | 0x80880903 // v2.0 | 
| <strong>CAPICOM_E_OUT_OF_RESOURCE</strong> | CAPICOM ha eseguito l'esecuzione di una risorsa.<br /> | 0x80880904 // v2.0 | 
| <strong>CAPICOM_E_INTERNAL</strong> | Si è verificato un errore interno. <br /> Per assistenza, contattare il supporto tecnico Microsoft.<br /> | 0x80880911 | 
| <strong>CAPICOM_E_UNKNOWN</strong> | Si è verificato un errore sconosciuto. <br /> Raccogliere il maggior numero possibile di informazioni e contattare il fornitore.<br /> | 0x80880999 | 




## <a name="requirements"></a>Requisiti



| Requisito | valore |
|----------------------------|--------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                |
| Intestazione<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 




