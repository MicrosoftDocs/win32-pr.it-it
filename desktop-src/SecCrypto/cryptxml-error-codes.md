---
description: Di seguito sono riportati i codici di errore di run-time, definiti in Cryptxml.h, che possono essere restituiti dalle funzioni CryptXML.
ms.assetid: c3678767-aab3-4771-b2f2-8d79545d420d
title: Codici di errore CryptXML (Cryptxml.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccb4b06070ca77f8b55f96d3e6c4732abc22c26970b83b6a70c720b7bade8a84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767978"
---
# <a name="cryptxml-error-codes"></a>Codici di errore CryptXML

Di seguito sono riportati i codici di errore di run-time, definiti in Cryptxml.h, che possono essere restituiti dalle funzioni CryptXML.



| Costante/valore                                                                                                                                                                                                                                                                             | Descrizione                                                                                                        |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| <span id="CRYPT_XML_E_LARGE"></span><span id="crypt_xml_e_large"></span><dl> <dt>**CRYPT \_ XML \_ E \_ LARGE**</dt> <dt>0x80092101L</dt> </dl>                                               | Il valore fornito è troppo grande.<br/>                                                                        |
| <span id="CRYPT_XML_E_ENCODING"></span><span id="crypt_xml_e_encoding"></span><dl> <dt>**CRYPT \_ CODIFICA \_ \_ XML E**</dt> <dt>0x80092103L</dt> </dl>                                      | La codifica XML specificata non è supportata.<br/>                                                              |
| <span id="CRYPT_XML_E_ALGORITHM"></span><span id="crypt_xml_e_algorithm"></span><dl> <dt>**CRYPT \_ \_ALGORITMO \_ XML E**</dt> <dt>0x80092104L</dt> </dl>                                   | L'algoritmo XML specificato non è supportato.<br/>                                                             |
| <span id="CRYPT_XML_E_TRANSFORM"></span><span id="crypt_xml_e_transform"></span><dl> <dt>**CRYPT \_ XML \_ E \_ TRANSFORM**</dt> <dt>0x80092105L</dt> </dl>                                   | La trasformazione specificata non è supportata.<br/>                                                                 |
| <span id="CRYPT_XML_E_HANDLE"></span><span id="crypt_xml_e_handle"></span><dl> <dt>**CRYPT \_ HANDLE \_ \_ XML E**</dt> <dt>0x80092106L</dt> </dl>                                            | L'handle fornito non è valido.<br/>                                                                       |
| <span id="CRYPT_XML_E_OPERATION"></span><span id="crypt_xml_e_operation"></span><dl> <dt>**CRYPT \_ XML \_ E \_ OPERATION**</dt> <dt>0x80092107L</dt> </dl>                                   | L'operazione non è valida.<br/>                                                                             |
| <span id="CRYPT_XML_E_UNRESOLVED_REFERENCE"></span><span id="crypt_xml_e_unresolved_reference"></span><dl> <dt>**CRYPT \_ RIFERIMENTO \_ XML E \_ UNRESOLVED \_**</dt> <dt>0x80092108L</dt> </dl> | Impossibile risolvere **l'elemento Reference.**<br/>                                                            |
| <span id="CRYPT_XML_E_INVALID_DIGEST"></span><span id="crypt_xml_e_invalid_digest"></span><dl> <dt>**CRYPT \_ XML \_ E \_ INVALID \_ DIGEST**</dt> <dt>0x80092109L</dt> </dl>                   | Il valore digest non è valido.<br/>                                                                          |
| <span id="CRYPT_XML_E_INVALID_SIGNATURE"></span><span id="crypt_xml_e_invalid_signature"></span><dl> <dt>**CRYPT \_ XML \_ E \_ INVALID \_ SIGNATURE**</dt> <dt>0x8009210AL</dt> </dl>          | Il valore della firma non è valido.<br/>                                                                       |
| <span id="CRYPT_XML_E_HASH_FAILED"></span><span id="crypt_xml_e_hash_failed"></span><dl> <dt>**CRYPT \_ HASH \_ XML E NON \_ \_ RIUSCITO**</dt> <dt>0x8009210BL</dt> </dl>                            | Impossibile creare o calcolare l'hash.<br/>                                                                 |
| <span id="CRYPT_XML_E_SIGN_FAILED"></span><span id="crypt_xml_e_sign_failed"></span><dl> <dt>**CRYPT \_ XML \_ E \_ SIGN \_ FAILED**</dt> <dt>0x8009210CL</dt> </dl>                            | L'operazione di firma crittografica non è riuscita.<br/>                                                           |
| <span id="CRYPT_XML_E_VERIFY_FAILED"></span><span id="crypt_xml_e_verify_failed"></span><dl> <dt>**CRYPT \_ XML \_ E \_ VERIFY \_ FAILED**</dt> <dt>0x8009210DL</dt> </dl>                      | Impossibile verificare la firma.<br/>                                                                      |
| <span id="CRYPT_XML_E_TOO_MANY_SIGNATURES"></span><span id="crypt_xml_e_too_many_signatures"></span><dl> <dt>**CRYPT \_ XML \_ E \_ TROPPE \_ \_ FIRME**</dt> <dt>0x8009210EL</dt> </dl>   | Il numero di **elementi Signature** nel documento ha superato il limite massimo consentito per l'elaborazione.<br/> |
| <span id="CRYPT_XML_E_INVALID_KEYVALUE"></span><span id="crypt_xml_e_invalid_keyvalue"></span><dl> <dt>**CRYPT \_ XML \_ E \_ INVALID \_ KEYVALUE**</dt> <dt>0x8009210FL</dt> </dl>             | Il valore della chiave fornito non è valido.<br/>                                                           |
| <span id="CRYPT_XML_E_UNEXPECTED_XML"></span><span id="crypt_xml_e_unexpected_xml"></span><dl> <dt>**CRYPT \_ XML \_ XML \_ \_ IMPREVISTO**</dt> <dt>0x80092110L</dt> </dl>                   | È stato rilevato codice XML non valido o imprevisto.<br/>                                                              |
| <span id="CRYPT_XML_E_SIGNER"></span><span id="crypt_xml_e_signer"></span><dl> <dt>**CRYPT \_ XML \_ E \_ SIGNER**</dt> <dt>0x80092111L</dt> </dl>                                            | Impossibile individuare la chiave del firmatario.<br/>                                                                      |
| <span id="CRYPT_XML_E_NON_UNIQUE_ID"></span><span id="crypt_xml_e_non_unique_id"></span><dl> <dt>**CRYPT \_ XML \_ E NON UNIQUE \_ \_ \_ ID**</dt> <dt>0x80092112L</dt> </dl>                     | È stato trovato un **attributo ID** non univoco.<br/>                                                                 |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                            |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Cryptxml.h</dt> </dl> |



 

 




