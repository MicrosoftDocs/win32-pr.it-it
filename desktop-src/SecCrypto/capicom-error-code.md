---
description: Definisce i codici di errore restituiti da CAPICOM.
ms.assetid: e72b8290-b482-4629-8b87-5a15677865a6
title: Enumerazione CAPICOM_ERROR_CODE (CAPICOM. h)
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
ms.openlocfilehash: ccd4963c83f1ad7ce3bc686b7736ce47d699ce30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329228"
---
# <a name="capicom_error_code-enumeration"></a>\_Enumerazione del codice di errore CAPICOM \_

Il tipo di enumerazione del **\_ \_ codice di errore CAPICOM** definisce i codici di errore restituiti da CAPICOM.

> [!Note]  
> Visual Basic errori di Scripting Edition restituiscono un valore **Err. Number** maggiore di zero. Per tali errori, i valori **Err. Description** forniscono informazioni sulla ragione dell'errore. Oltre ai Visual Basic errori di Scripting Edition, gli errori di CAPICOM restituiscono i codici definiti dal **codice di \_ errore \_ di CAPICOM**.

 

## <a name="members"></a>Membri



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Membro</th>
<th>Descrizione</th>
<th>Valore</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>CAPICOM_E_ENCODE_INVALID_TYPE</strong></td>
<td>È stato usato un tipo di codifica non valido.<br/> Nell'elenco seguente sono riportati i tipi di codifica validi:
<ul>
<li>CAPICOM_ENCODE_ANY</li>
<li>CAPICOM_ENCODE_BASE64</li>
<li>CAPICOM_ENCODE_BINARY</li>
</ul>
<br/></td>
<td>0x80880100</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_EKU_INVALID_OID</strong></td>
<td>Impossibile impostare la proprietà <a href="eku-oid.md"><strong>OID</strong></a> dell'oggetto <a href="eku.md"><strong>EKU</strong></a> perché la proprietà <a href="eku-name.md"><strong>Name</strong></a> non è impostata su CAPICOM_EKU_OTHER.<br/> Impostare la proprietà <a href="eku-name.md"><strong>Name</strong></a> su CAPICOM_EKU_OTHER prima di impostare la proprietà <a href="eku-oid.md"><strong>OID</strong></a> .<br/></td>
<td>0x80880200</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_EKU_OID_NOT_INITIALIZED</strong></td>
<td>La proprietà <a href="eku-oid.md"><strong>OID</strong></a> dell'oggetto <a href="eku.md"><strong>EKU</strong></a> non è stata inizializzata. <br/> Impostare la proprietà <a href="eku-name.md"><strong>Name</strong></a> su un valore diverso da CAPICOM_EKU_OTHER oppure impostare la proprietà <strong>Name</strong> su CAPICOM_EKU_OTHER e la proprietà <a href="eku-oid.md"><strong>OID</strong></a> su un valore.<br/></td>
<td>0x80880201</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_CERTIFICATE_NOT_INITIALIZED</strong></td>
<td>L'oggetto <a href="certificate.md"><strong>certificato</strong></a> non è stato inizializzato.<br/> Questo codice di errore viene in genere restituito quando viene creata un'istanza di un oggetto <a href="certificate.md"><strong>certificato</strong></a> , che non è associato a un certificato digitale. Per associare l'oggetto a un certificato digitale, assegnarlo a un oggetto <strong>certificato</strong> esistente o chiamare il metodo <a href="certificate-import.md"><strong>Import</strong></a> .<br/></td>
<td>0x80880210</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_CERTIFICATE_NO_PRIVATE_KEY</strong></td>
<td>All'oggetto <a href="certificate.md"><strong>certificato</strong></a> non è associata una chiave privata.<br/> Questo codice di errore viene restituito quando viene effettuato un tentativo di firmare i dati utilizzando la chiave privata del firmatario, ma l'oggetto <a href="certificate.md"><strong>certificato</strong></a> associato all'oggetto <a href="signer.md"><strong>firmatario</strong></a> non può essere utilizzato per l'operazione di firma.<br/></td>
<td>0x80880211</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_CHAIN_NOT_BUILT</strong></td>
<td>L'oggetto <a href="chain.md"><strong>Chain</strong></a> non è stato inizializzato. <br/> Per inizializzare l'oggetto <a href="chain.md"><strong>Chain</strong></a> , chiamare il metodo di <a href="chain-build.md"><strong>compilazione</strong></a> .<br/></td>
<td>0x80880220</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_STORE_NOT_OPENED</strong></td>
<td>L'oggetto <a href="store.md"><strong>Store</strong></a> non è stato inizializzato. <br/> Per inizializzare l'oggetto <a href="store.md"><strong>Store</strong></a> , chiamare il metodo <a href="store-open.md"><strong>Open</strong></a> .<br/></td>
<td>0x80880230</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_STORE_EMPTY</strong></td>
<td>L'oggetto <a href="store.md"><strong>Store</strong></a> non contiene oggetti <a href="certificate.md"><strong>Certificate</strong></a> .<br/></td>
<td>0x80880231</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_STORE_INVALID_OPEN_MODE</strong></td>
<td>Il parametro <em>OpenMode</em> del metodo <a href="store-open.md"><strong>Store. Open</strong></a> non contiene un valore valido di CAPICOM_STORE_OPEN_MODE.<br/> L'elenco seguente mostra i valori validi di CAPICOM_STORE_OPEN_MODE:
<ul>
<li>CAPICOM_STORE_OPEN_READ_ONLY</li>
<li>CAPICOM_STORE_OPEN_READ_WRITE</li>
<li>CAPICOM_STORE_OPEN_MAXIMUM_ALLOWED</li>
<li>CAPICOM_STORE_OPEN_EXISTING_ONLY</li>
<li>CAPICOM_STORE_OPEN_INCLUDE_ARCHIVED</li>
</ul>
<br/></td>
<td>0x80880232</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_STORE_INVALID_SAVE_AS_TYPE</strong></td>
<td>Il valore di <em>SaveAs</em> passato al metodo <a href="store-export.md"><strong>Export</strong></a> dell'oggetto <a href="store.md"><strong>Store</strong></a> non è valido. <br/> Nell'elenco seguente sono riportati i valori di <em>SaveAs</em> validi:
<ul>
<li>CAPICOM_STORE_SAVE_AS_SERIALIZED</li>
<li>CAPICOM_STORE_SAVE_AS_PKCS7</li>
</ul>
<br/></td>
<td>0x80880233</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_ATTRIBUTE_NAME_NOT_INITIALIZED</strong></td>
<td>La proprietà <a href="attribute-name.md"><strong>Name</strong></a> dell'oggetto <a href="attribute.md"><strong>attribute</strong></a> non è stata inizializzata. <br/> Impostare la proprietà <a href="attribute-name.md"><strong>Name</strong></a> .<br/></td>
<td>0x80880240</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_ATTRIBUTE_VALUE_NOT_INITIALIZED</strong></td>
<td>La proprietà <a href="attribute-value.md"><strong>value</strong></a> dell'oggetto <a href="attribute.md"><strong>attribute</strong></a> non è stata inizializzata. <br/> Impostare la proprietà <a href="attribute-value.md"><strong>value</strong></a> .<br/></td>
<td>0x80880241</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_ATTRIBUTE_INVALID_NAME</strong></td>
<td>La proprietà <a href="attribute-name.md"><strong>Name</strong></a> dell'oggetto <a href="attribute.md"><strong>attributo</strong></a> non è valida. <br/> Nell'elenco seguente sono riportati i nomi di attributo validi:
<ul>
<li>CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME</li>
<li>CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_NAME</li>
<li>CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_DESCRIPTION</li>
</ul>
<br/></td>
<td>0x80880242</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_ATTRIBUTE_INVALID_VALUE</strong></td>
<td>La proprietà <a href="attribute-value.md"><strong>value</strong></a> dell'oggetto <a href="attribute.md"><strong>attribute</strong></a> non è valida perché il tipo di dati non corrisponde al tipo di dati indicato dalla proprietà <strong>Name</strong> . <br/> Se, ad esempio, la proprietà <a href="attribute-value.md"><strong>Name</strong></a> è impostata su CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME, il tipo di dati deve essere <strong>date</strong>.<br/></td>
<td>0x80880243</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_SIGNER_NOT_INITIALIZED</strong></td>
<td>L'oggetto <a href="signer.md"><strong>firmatario</strong></a> non è stato inizializzato. <br/> Per inizializzare l'oggetto <a href="signer.md"><strong>firmatario</strong></a> , impostare la proprietà <a href="signer-certificate.md"><strong>Certificate</strong></a> .<br/></td>
<td>0x80880250</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_SIGNER_NOT_FOUND</strong></td>
<td>Impossibile trovare il firmatario nell'oggetto <a href="signeddata.md"><strong>SignedData</strong></a> . <br/> In genere, questa operazione non viene eseguita con un oggetto <a href="signeddata.md"><strong>SignedData</strong></a> creato da CAPICOM; Tuttavia, se l'oggetto <strong>SignedData</strong> è stato creato da un prodotto di terze parti, il certificato del firmatario potrebbe non essere incluso nella struttura di #7 Pkcs.<br/></td>
<td>0x80880251</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_SIGNER_NO_CHAIN</strong></td>
<td>Impossibile trovare un oggetto <a href="chain.md"><strong>Chain</strong></a> nell'oggetto <a href="signer.md"><strong>firmatario</strong></a> .<br/></td>
<td>0x80880252//v 2.0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_SIGNER_INVALID_USAGE</strong></td>
<td>Viene effettuato un tentativo di utilizzare il firmatario in modo non valido.<br/></td>
<td>//V2.0 0x80880253</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_SIGN_NOT_INITIALIZED</strong></td>
<td>L'oggetto <a href="signeddata.md"><strong>SignedData</strong></a> non è stato inizializzato. <br/> Per inizializzare l'oggetto <a href="signeddata.md"><strong>SignedData</strong></a> , impostare la proprietà <a href="signeddata-content.md"><strong>Content</strong></a> o chiamare il metodo <a href="signeddata-verify.md"><strong>Verify</strong></a> .<br/></td>
<td>0x80880260</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_SIGN_INVALID_TYPE</strong></td>
<td>L'oggetto <a href="signeddata.md"><strong>SignedData</strong></a> contiene un tipo non valido. <br/> In genere, ciò si verifica quando viene effettuato un tentativo di verificare un messaggio in busta con un oggetto <a href="signeddata.md"><strong>SignedData</strong></a> o viceversa.<br/></td>
<td>0x80880261</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_SIGN_NOT_SIGNED</strong></td>
<td>L'oggetto <a href="signeddata.md"><strong>SignedData</strong></a> non è stato firmato. <br/> Per firmare l'oggetto <a href="signeddata.md"><strong>SignedData</strong></a> , chiamare il metodo <a href="signeddata-sign.md"><strong>Sign</strong></a> .<br/></td>
<td>0x80880262</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_INVALID_ALGORITHM</strong></td>
<td>Il valore dell'algoritmo per la proprietà <a href="algorithm-name.md"><strong>Name</strong></a> dell'oggetto <a href="algorithm.md"><strong>Algorithm</strong></a> non è valido. <br/> Nell'elenco seguente vengono illustrati i valori di algoritmo validi per la proprietà <a href="algorithm-name.md"><strong>Name</strong></a> :
<ul>
<li>CAPICOM_ENCRYPTION_ALGORITHM_RC2</li>
<li>CAPICOM_ENCRYPTION_ALGORITHM_RC4</li>
<li>CAPICOM_ENCRYPTION_ALGORITHM_DES</li>
<li>CAPICOM_ENCRYPTION_ALGORITHM_3DES</li>
</ul>
<br/></td>
<td>0x80880270</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_INVALID_KEY_LENGTH</strong></td>
<td>Il valore della lunghezza della chiave per la proprietà della <a href="algorithm-keylength.md"><strong>lunghezza</strong></a> della chiave dell'oggetto <a href="algorithm.md"><strong>Algorithm</strong></a> non è valido. <br/> Nell'elenco seguente sono riportati i valori validi per la lunghezza della chiave per la proprietà di <a href="algorithm-keylength.md"><strong>lunghezza</strong></a> della chiave:
<ul>
<li>CAPICOM_ENCRYPTION_KEY_LENGTH_MAXIMUM</li>
<li>CAPICOM_ENCRYPTION_KEY_LENGTH_40_BITS</li>
<li>CAPICOM_ENCRYPTION_KEY_LENGTH_56_BITS</li>
<li>CAPICOM_ENCRYPTION_KEY_LENGTH_128_BITS</li>
</ul>
<br/></td>
<td>0x80880271</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_ENVELOP_NOT_INITIALIZED</strong></td>
<td>L'oggetto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> non è stato inizializzato. <br/> Per inizializzare l'oggetto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> , impostare la proprietà <a href="envelopeddata-content.md"><strong>Content</strong></a> o chiamare il metodo <a href="envelopeddata-decrypt.md"><strong>Decrypt</strong></a> .<br/></td>
<td>0x80880280</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_ENVELOP_INVALID_TYPE</strong></td>
<td>L'oggetto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> contiene un tipo non valido. <br/> In genere, ciò si verifica quando viene effettuato un tentativo di verificare un messaggio firmato con un oggetto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> o viceversa.<br/></td>
<td>0x80880281</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_ENVELOP_NO_RECIPIENT</strong></td>
<td>Non è stato specificato alcun destinatario nell'oggetto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> quando viene chiamato il metodo <a href="envelopeddata-encrypt.md"><strong>Encrypt</strong></a> di un oggetto <strong>EnvelopedData</strong> . <br/> Per aggiungere un destinatario, chiamare il metodo <a href="recipients-add.md"><strong>Recipients. Add</strong></a> .<br/></td>
<td>0x80880282</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_ENVELOP_RECIPIENT_NOT_FOUND</strong></td>
<td>Impossibile trovare il destinatario nell'oggetto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> . <br/> In genere, questa operazione non viene eseguita con un oggetto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> creato da CAPICOM; Tuttavia, se l'oggetto <strong>EnvelopedData</strong> è stato creato da un prodotto di terze parti, il certificato del destinatario potrebbe non essere incluso nella struttura di #7 Pkcs.<br/></td>
<td>0x80880283</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_ENCRYPT_NOT_INITIALIZED</strong></td>
<td>L'oggetto <a href="encrypteddata.md"><strong>EncryptedData</strong></a> non è stato inizializzato. <br/> Per inizializzare l'oggetto <a href="encrypteddata.md"><strong>EncryptedData</strong></a> , impostare la proprietà <a href="encrypteddata-content.md"><strong>Content</strong></a> o chiamare il metodo <a href="encrypteddata-decrypt.md"><strong>Decrypt</strong></a> .<br/></td>
<td>0x80880290</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_ENCRYPT_INVALID_TYPE</strong></td>
<td>L'oggetto <a href="encrypteddata.md"><strong>EncryptedData</strong></a> non è un tipo valido. <br/> In genere, ciò significa che i dati sono danneggiati.<br/></td>
<td>0x80880291</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_ENCRYPT_NO_SECRET</strong></td>
<td>Il segreto di un oggetto <a href="encrypteddata.md"><strong>EncryptedData</strong></a> non è stato inizializzato. <br/> Per inizializzare il segreto di un oggetto <a href="encrypteddata.md"><strong>EncryptedData</strong></a> , chiamare il metodo <a href="encrypteddata-setsecret.md"><strong>sesecret</strong></a> .<br/></td>
<td>0x80880292</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_PRIVATE_KEY_NOT_INITIALIZED</strong></td>
<td>L'oggetto <a href="privatekey.md"><strong>PrivateKey</strong></a> non è stato inizializzato.<br/></td>
<td>0x80880300//v 2.0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_PRIVATE_KEY_NOT_EXPORTABLE</strong></td>
<td>Impossibile esportare l'oggetto <a href="privatekey.md"><strong>PrivateKey</strong></a> .<br/></td>
<td>0x80880301//v 2.0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_ENCODE_NOT_INITIALIZED</strong></td>
<td>L'oggetto <a href="encodeddata.md"><strong>EncodedData</strong></a> non è stato inizializzato.<br/></td>
<td>0x80880320//v 2.0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_EXTENSION_NOT_INITIALIZED</strong></td>
<td>L'oggetto di <a href="extension.md"><strong>estensione</strong></a> non è stato inizializzato.<br/></td>
<td>0x80880330//v 2.0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_PROPERTY_NOT_INITIALIZED</strong></td>
<td>La proprietà <a href="extendedproperty-propid.md"><strong>propid</strong></a> dell'oggetto <a href="extendedproperty.md"><strong>ExtendedProperty</strong></a> non è stata inizializzata.<br/></td>
<td>0x80880340//v 2.0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_FIND_INVALID_TYPE</strong></td>
<td>Il parametro <em>FindType</em> del metodo <a href="certificates-find.md"><strong>Certificates. Find</strong></a> non è un valore dell'enumerazione <a href="capicom-certificate-find-type.md"><strong>CAPICOM_CERTIFICATE_FIND_TYPE</strong></a> .<br/></td>
<td>0x80880350//v 2.0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_FIND_INVALID_PREDEFINED_POLICY</strong></td>
<td>Il criterio predefinito specificato per l'operazione di ricerca non è valido.<br/></td>
<td>0x80880351//v 2.0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_CODE_NOT_INITIALIZED</strong></td>
<td>L'oggetto <a href="signedcode.md"><strong>SignedCode</strong></a> non è stato inizializzato.<br/></td>
<td>0x80880360//v 2.0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_CODE_NOT_SIGNED</strong></td>
<td>L'oggetto <a href="signedcode.md"><strong>SignedCode</strong></a> non è stato firmato.<br/> Per firmare l'oggetto <a href="signedcode.md"><strong>SignedCode</strong></a> , chiamare il metodo <a href="signedcode-sign.md"><strong>Sign</strong></a> .<br/></td>
<td>0x80880361//v 2.0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_CODE_DESCRIPTION_NOT_INITIALIZED</strong></td>
<td>La proprietà <a href="signedcode-description.md"><strong>Description</strong></a> dell'oggetto <a href="signedcode.md"><strong>SignedCode</strong></a> non è stata inizializzata.<br/></td>
<td>0x80880362//v 2.0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_CODE_DESCRIPTION_URL_NOT_INITIALIZED</strong></td>
<td>La proprietà <a href="signedcode-descriptionurl.md"><strong>DescriptionURL</strong></a> dell'oggetto <a href="signedcode.md"><strong>SignedCode</strong></a> non è stata inizializzata.<br/></td>
<td>0x80880363//v 2.0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_CODE_INVALID_TIMESTAMP_URL</strong></td>
<td>Il parametro <em>URL</em> del metodo <a href="signedcode-timestamp.md"><strong>SignedCode. timestamp</strong></a> non è valido.<br/></td>
<td>0x80880364//v 2.0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_HASH_NO_DATA</strong></td>
<td>L'oggetto <a href="hasheddata.md"><strong>HashedData</strong></a> non contiene dati.<br/></td>
<td>0x80880370//v 2.0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_INVALID_CONVERT_TYPE</strong></td>
<td>Il tipo di conversione non è valido.<br/></td>
<td>0x80880380//v 2.0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_NOT_SUPPORTED</strong></td>
<td>L'operazione richiesta non è supportata nella piattaforma corrente. <br/></td>
<td>0x80880900</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_UI_DISABLED</strong></td>
<td>Quando si esegue la firma, la proprietà <a href="signer-certificate.md"><strong>Certificate</strong></a> dell'oggetto <a href="signer.md"><strong>firmatario</strong></a> non è stata impostata, ma la richiesta del certificato utente è stata disabilitata. <br/> Abilitare la richiesta impostando la proprietà <a href="settings-enablepromptforcertificateui.md"><strong>EnablePromptForCertificateUI</strong></a> dell'oggetto <a href="settings.md"><strong>Settings</strong></a> oppure impostare la proprietà <a href="signer-certificate.md"><strong>Certificate</strong></a> dell'oggetto <a href="signer.md"><strong>firmatario</strong></a> .<br/></td>
<td>0x80880901</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_CANCELLED</strong></td>
<td>L'operazione è stata annullata dall'utente. <br/> Ciò si verifica quando all'utente viene richiesta l'autorizzazione per eseguire una determinata operazione, ad esempio l'accesso alla chiave privata, e l'utente annulla l'operazione.<br/></td>
<td>0x80880902</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_NOT_ALLOWED</strong></td>
<td>Operazione tentata non consentita.<br/> La modifica della proprietà <a href="extendedproperty-propid.md"><strong>propid</strong></a> di un oggetto <a href="extendedproperty.md"><strong>ExtendedProperty</strong></a> , ad esempio, non è consentita se l'oggetto è associato a un certificato.<br/></td>
<td>0x80880903//v 2.0</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_OUT_OF_RESOURCE</strong></td>
<td>Il capicot ha esaurito una risorsa.<br/></td>
<td>0x80880904//v 2.0</td>
</tr>
<tr class="even">
<td><strong>CAPICOM_E_INTERNAL</strong></td>
<td>Si è verificato un errore interno. <br/> Per assistenza, contattare il supporto tecnico Microsoft.<br/></td>
<td>0x80880911</td>
</tr>
<tr class="odd">
<td><strong>CAPICOM_E_UNKNOWN</strong></td>
<td>Si è verificato un errore sconosciuto. <br/> Raccogliere quante più informazioni possibile e contattare il fornitore.<br/></td>
<td>0x80880999</td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|--------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                |
| Intestazione<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




