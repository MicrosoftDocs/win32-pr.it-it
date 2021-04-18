---
description: Di seguito sono riportati i codici di errore in fase di esecuzione, definiti in Cryptxml. h, che possono essere restituiti dalle funzioni CryptXML.
ms.assetid: c3678767-aab3-4771-b2f2-8d79545d420d
title: Codici di errore CryptXML (Cryptxml. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5906c406f14081844ddce042f0e170668950e7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318245"
---
# <a name="cryptxml-error-codes"></a>Codici di errore CryptXML

Di seguito sono riportati i codici di errore in fase di esecuzione, definiti in Cryptxml. h, che possono essere restituiti dalle funzioni CryptXML.



| Costante/valore                                                                                                                                                                                                                                                                             | Descrizione                                                                                                        |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| <span id="CRYPT_XML_E_LARGE"></span><span id="crypt_xml_e_large"></span><dl> <dt>**Crypt \_ 0x80092101L XML \_ E \_ large**</dt> <dt></dt> </dl>                                               | Il valore fornito è troppo grande.<br/>                                                                        |
| <span id="CRYPT_XML_E_ENCODING"></span><span id="crypt_xml_e_encoding"></span><dl> <dt>**Crypt \_ 0x80092103L \_ \_ codifica XML E**</dt> <dt></dt> </dl>                                      | La codifica XML specificata non è supportata.<br/>                                                              |
| <span id="CRYPT_XML_E_ALGORITHM"></span><span id="crypt_xml_e_algorithm"></span><dl> <dt>**Crypt \_ 0x80092104L \_ \_ algoritmo XML E**</dt> <dt></dt> </dl>                                   | L'algoritmo XML specificato non è supportato.<br/>                                                             |
| <span id="CRYPT_XML_E_TRANSFORM"></span><span id="crypt_xml_e_transform"></span><dl> <dt>**Crypt \_ 0x80092105L \_ di \_ trasformazione XML E**</dt> <dt></dt> </dl>                                   | La trasformazione specificata non è supportata.<br/>                                                                 |
| <span id="CRYPT_XML_E_HANDLE"></span><span id="crypt_xml_e_handle"></span><dl> <dt>**Crypt \_ 0x80092106L \_ E \_ handle XML**</dt> <dt></dt> </dl>                                            | Handle fornito non valido.<br/>                                                                       |
| <span id="CRYPT_XML_E_OPERATION"></span><span id="crypt_xml_e_operation"></span><dl> <dt>**Crypt \_ 0x80092107L \_ \_ operazione XML E**</dt> <dt></dt> </dl>                                   | Operazione non valida.<br/>                                                                             |
| <span id="CRYPT_XML_E_UNRESOLVED_REFERENCE"></span><span id="crypt_xml_e_unresolved_reference"></span><dl> <dt>**Crypt \_ 0x80092108L \_ di \_ \_ riferimento XML E non risolto**</dt> <dt></dt> </dl> | Non è possibile risolvere l'elemento **Reference** .<br/>                                                            |
| <span id="CRYPT_XML_E_INVALID_DIGEST"></span><span id="crypt_xml_e_invalid_digest"></span><dl> <dt>**Crypt \_ 0x80092109L \_ \_ \_ digest XML E non valido**</dt> <dt></dt> </dl>                   | Il valore del digest non è valido.<br/>                                                                          |
| <span id="CRYPT_XML_E_INVALID_SIGNATURE"></span><span id="crypt_xml_e_invalid_signature"></span><dl> <dt>**Crypt \_ 0x8009210AL \_ \_ \_ firma XML E non valida**</dt> <dt></dt> </dl>          | Il valore della firma non è valido.<br/>                                                                       |
| <span id="CRYPT_XML_E_HASH_FAILED"></span><span id="crypt_xml_e_hash_failed"></span><dl> <dt>**Crypt \_ \_Hash XML E 0x8009210BL \_ \_ non riuscito**</dt> <dt></dt> </dl>                            | Impossibile creare o calcolare l'hash.<br/>                                                                 |
| <span id="CRYPT_XML_E_SIGN_FAILED"></span><span id="crypt_xml_e_sign_failed"></span><dl> <dt>**Crypt \_ 0x8009210CL \_ firma XML E \_ \_ non riuscita**</dt> <dt></dt> </dl>                            | Operazione di crittografia della firma non riuscita.<br/>                                                           |
| <span id="CRYPT_XML_E_VERIFY_FAILED"></span><span id="crypt_xml_e_verify_failed"></span><dl> <dt>**Crypt \_ 0x8009210DL XML \_ E \_ verifica \_ non riuscita**</dt> <dt></dt> </dl>                      | Impossibile verificare la firma.<br/>                                                                      |
| <span id="CRYPT_XML_E_TOO_MANY_SIGNATURES"></span><span id="crypt_xml_e_too_many_signatures"></span><dl> <dt>**Crypt \_ XML \_ E \_ troppe \_ \_ firme**</dt> <dt>0x8009210EL</dt> </dl>   | Il numero di elementi della **firma** nel documento supera il limite massimo consentito per l'elaborazione.<br/> |
| <span id="CRYPT_XML_E_INVALID_KEYVALUE"></span><span id="crypt_xml_e_invalid_keyvalue"></span><dl> <dt>**Crypt \_ XML \_ E \_ \_ valore**</dt> di <dt>0x8009210FL</dt> non valido </dl>             | Il valore della chiave fornito non è valido.<br/>                                                           |
| <span id="CRYPT_XML_E_UNEXPECTED_XML"></span><span id="crypt_xml_e_unexpected_xml"></span><dl> <dt>**Crypt \_ XML \_ E \_ imprevisto 0x80092110L \_ XML**</dt> <dt></dt> </dl>                   | Rilevato XML non valido o imprevisto.<br/>                                                              |
| <span id="CRYPT_XML_E_SIGNER"></span><span id="crypt_xml_e_signer"></span><dl> <dt>**Crypt \_ 0x80092111L \_ E \_ FIRMATARIo XML**</dt> <dt></dt> </dl>                                            | Impossibile individuare la chiave del firmatario.<br/>                                                                      |
| <span id="CRYPT_XML_E_NON_UNIQUE_ID"></span><span id="crypt_xml_e_non_unique_id"></span><dl> <dt>**Crypt \_ \_ID XML E \_ non \_ univoco \_**</dt> <dt>0x80092112L</dt> </dl>                     | È stato trovato un attributo **ID** non univoco.<br/>                                                                 |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                            |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Cryptxml. h</dt> </dl> |



 

 




