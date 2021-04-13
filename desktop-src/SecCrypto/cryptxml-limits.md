---
description: CryptXML definisce i limiti globali seguenti nel file di intestazione Cryptxml. h.
ms.assetid: 8f4dc314-76fc-40ce-a1e1-a701ae39d66d
title: Limiti di CryptXML (Cryptxml. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccc56ee6459be2160efdeb8e9874e7dd0c53518d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484597"
---
# <a name="cryptxml-limits"></a>Limiti di CryptXML

CryptXML definisce i limiti globali seguenti nel file di intestazione Cryptxml. h.



| Costante/valore                                                                                                                                                                                                                                                             | Descrizione                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CRYPT_XML_BLOB_MAX"></span><span id="crypt_xml_blob_max"></span><dl> <dt>**Crypt \_ \_ \_ Numero massimo**</dt> di <dt>0x7FFFFFF8</dt> BLOB XML </dl>                             | I dati codificati non possono superare 2 gigabyte (GB).<br/>                                                                                                                                                                               |
| <span id="CRYPT_XML_ID_MAX"></span><span id="crypt_xml_id_max"></span><dl> <dt>**Crypt \_ \_ID XML \_ massimo**</dt> <dt>256</dt> </dl>                                          | La lunghezza dell'ID non può superare i 256 caratteri.<br/>                                                                                                                                                                                    |
| <span id="CRYPT_XML_URI_MAX"></span><span id="crypt_xml_uri_max"></span><dl> <dt>**Crypt \_ \_URI XML \_ MAX**</dt> <dt>8 \* 1024</dt> </dl>                                   | La lunghezza dell'URI non può superare i 8192 caratteri.<br/>                                                                                                                                                                                  |
| <span id="CRYPT_XML_SIGNATURES_MAX"></span><span id="crypt_xml_signatures_max"></span><dl> <dt>**Crypt \_ \_Firme XML \_ Max**</dt> <dt>16</dt> </dl>                   | Numero massimo predefinito di elementi della **firma** per documento. È possibile eseguire l'override di questo valore specificando un nuovo valore massimo quando si passano i valori delle proprietà come strutture di [**\_ \_ proprietà XML di crittografia**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_property) .<br/> |
| <span id="CRYPT_XML_TRANSFORM_MAX"></span><span id="crypt_xml_transform_max"></span><dl> <dt>**Crypt \_ \_Trasformazione XML \_ Max**</dt> <dt>16</dt> </dl>                      | Numero massimo di trasformazioni, rappresentate dalle strutture dell' [**\_ \_ algoritmo XML Crypt**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_algorithm) , per riferimento, rappresentate da una struttura di [**\_ \_ riferimento XML Crypt**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_reference) .<br/>          |
| <span id="CRYPT_XML_SIGNATURE_VALUE_MAX"></span><span id="crypt_xml_signature_value_max"></span><dl> <dt>**Crypt \_ \_Valore della firma XML \_ \_ Max**</dt> <dt>2048</dt> </dl> | Lunghezza massima, in byte, di una struttura [**di \_ \_ firma XML di crittografia**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_signature) .<br/>                                                                                                                         |
| <span id="CRYPT_XML_DIGEST_VALUE_MAX"></span><span id="crypt_xml_digest_value_max"></span><dl> <dt>**Crypt \_ \_Valore del digest XML \_ \_ massimo**</dt> <dt>128</dt> </dl>           | Lunghezza massima, in byte, di un digest.<br/>                                                                                                                                                                                 |
| <span id="CRYPT_XML_OBJECTS_MAX"></span><span id="crypt_xml_objects_max"></span><dl> <dt>**Crypt \_ \_Oggetti XML \_ Max**</dt> <dt>256</dt> </dl>                           | Utilizzato internamente per specificare il numero massimo di elementi **oggetto** consentiti per firma.<br/>                                                                                                                                |
| <span id="CRYPT_XML_REFERENCES_MAX"></span><span id="crypt_xml_references_max"></span><dl> <dt>**Crypt \_ \_Riferimenti XML \_ Max**</dt> <dt>0x7FF8</dt> </dl>               | Numero massimo di elementi di **riferimento** consentiti.<br/>                                                                                                                                                                      |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                            |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Cryptxml. h</dt> </dl> |



 

 




