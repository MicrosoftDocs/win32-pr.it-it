---
description: CryptXML definisce i limiti globali seguenti nel file di intestazione Cryptxml.h.
ms.assetid: 8f4dc314-76fc-40ce-a1e1-a701ae39d66d
title: Limiti di CryptXML (Cryptxml.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98a0dcdf5dc8f8bd9efed4dcdb15ca316ecb1645e5775f3d714f46c6835b3a18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100921"
---
# <a name="cryptxml-limits"></a>Limiti di CryptXML

CryptXML definisce i limiti globali seguenti nel file di intestazione Cryptxml.h.



| Costante/valore                                                                                                                                                                                                                                                             | Descrizione                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CRYPT_XML_BLOB_MAX"></span><span id="crypt_xml_blob_max"></span><dl> <dt>**CRYPT \_ NUMERO \_ \_ MASSIMO DI BLOB XML**</dt> <dt>0x7FFFFFF8</dt> </dl>                             | I dati codificati non possono superare i 2 gigabyte (GB).<br/>                                                                                                                                                                               |
| <span id="CRYPT_XML_ID_MAX"></span><span id="crypt_xml_id_max"></span><dl> <dt>**CRYPT \_ ID XML \_ \_ MAX**</dt> <dt>256</dt> </dl>                                          | La lunghezza dell'ID non può superare i 256 caratteri.<br/>                                                                                                                                                                                    |
| <span id="CRYPT_XML_URI_MAX"></span><span id="crypt_xml_uri_max"></span><dl> <dt>**CRYPT \_ URI XML \_ \_ MASSIMO**</dt> <dt>8 \* 1024</dt> </dl>                                   | La lunghezza dell'URI non può superare 8192 caratteri.<br/>                                                                                                                                                                                  |
| <span id="CRYPT_XML_SIGNATURES_MAX"></span><span id="crypt_xml_signatures_max"></span><dl> <dt>**CRYPT \_ FIRME XML \_ \_ MAX**</dt> <dt>16</dt> </dl>                   | Numero massimo predefinito di **elementi Signature** per documento. È possibile eseguire l'override di questo valore specificando un nuovo valore massimo quando si passano valori di proprietà come [**strutture CRYPT \_ XML \_ PROPERTY.**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_property)<br/> |
| <span id="CRYPT_XML_TRANSFORM_MAX"></span><span id="crypt_xml_transform_max"></span><dl> <dt>**CRYPT \_ XML \_ TRANSFORM \_ MAX**</dt> <dt>16</dt> </dl>                      | Numero massimo di trasformazioni, rappresentate dalle [**strutture CRYPT \_ XML \_ ALGORITHM,**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_algorithm) per riferimento, rappresentate da una [**struttura CRYPT XML \_ \_ REFERENCE.**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_reference)<br/>          |
| <span id="CRYPT_XML_SIGNATURE_VALUE_MAX"></span><span id="crypt_xml_signature_value_max"></span><dl> <dt>**CRYPT \_ VALORE \_ MASSIMO DI FIRMA \_ \_ XML**</dt> <dt>2048</dt> </dl> | Lunghezza massima, in byte, di una [**struttura CRYPT \_ XML \_ SIGNATURE.**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_signature)<br/>                                                                                                                         |
| <span id="CRYPT_XML_DIGEST_VALUE_MAX"></span><span id="crypt_xml_digest_value_max"></span><dl> <dt>**CRYPT \_ VALORE DIGEST XML \_ \_ \_ MASSIMO**</dt> <dt>128</dt> </dl>           | Lunghezza massima, in byte, di un digest.<br/>                                                                                                                                                                                 |
| <span id="CRYPT_XML_OBJECTS_MAX"></span><span id="crypt_xml_objects_max"></span><dl> <dt>**CRYPT \_ OGGETTI XML \_ \_ MAX**</dt> <dt>256</dt> </dl>                           | Utilizzato internamente per specificare il numero massimo di **elementi Object** consentiti per ogni firma.<br/>                                                                                                                                |
| <span id="CRYPT_XML_REFERENCES_MAX"></span><span id="crypt_xml_references_max"></span><dl> <dt>**CRYPT \_ RIFERIMENTI XML \_ \_ MAX**</dt> <dt>0x7FF8</dt> </dl>               | Numero massimo di **elementi Reference** consentiti.<br/>                                                                                                                                                                      |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                            |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Cryptxml.h</dt> </dl> |



 

 




