---
title: Costanti WINBIO_BIR_FIELD (tipi WinBio \_ . h)
description: Specificare una maschera di maschera.
ms.assetid: D8D12BCF-FEB3-4E02-B751-9F3AE5048BC1
topic_type:
- apiref
api_name:
- WINBIO_BIR_FIELD_SUBHEAD_COUNT
- WINBIO_BIR_FIELD_PRODUCT_ID
- WINBIO_BIR_FIELD_PATRON_ID
- WINBIO_BIR_FIELD_INDEX
- WINBIO_BIR_FIELD_CREATION_DATE
- WINBIO_BIR_FIELD_VALIDITY_PERIOD
- WINBIO_BIR_FIELD_BIOMETRIC_TYPE
- WINBIO_BIR_FIELD_BIOMETRIC_SUBTYPE
- WINBIO_BIR_FIELD_CBEFF_HEADER_VERSION
- WINBIO_BIR_FIELD_PATRON_HEADER_VERSION
- WINBIO_BIR_FIELD_BIOMETRIC_PURPOSE
- WINBIO_BIR_FIELD_BIOMETRIC_CONDITION
- WINBIO_BIR_FIELD_QUALITY
- WINBIO_BIR_FIELD_CREATOR
- WINBIO_BIR_FIELD_CHALLENGE
- WINBIO_BIR_FIELD_PAYLOAD
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 104710f1686f13227fbe65782c2baf9c13149650
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340732"
---
# <a name="winbio_bir_field-constants"></a>\_Costanti di \_ campo WINBIO Bir

Le costanti seguenti vengono usate per creare una maschera di maschera per il membro **ValidFields** della struttura dell' [**\_ \_ intestazione WINBIO bir**](winbio-bir-header.md) .



| Costante/valore                                                                                                                                                                                                                                                                                           | Descrizione                                                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_BIR_FIELD_SUBHEAD_COUNT"></span><span id="winbio_bir_field_subhead_count"></span><dl> <dt>**WINBIO \_ \_Numero di \_ sottointestazioni \_ del campo bir**</dt> <dt>0x0001</dt> </dl>                          | Fornito per conformità con NISTIR 6529-A, il formato comune CBEFF (Biometric Exchange formats Framework) A, ma non usato.<br/> |
| <span id="WINBIO_BIR_FIELD_PRODUCT_ID"></span><span id="winbio_bir_field_product_id"></span><dl> <dt>**WINBIO \_ \_ \_ \_ ID prodotto campo bir**</dt> <dt>0x0002</dt> </dl>                                   | Il membro **ProductID** è valido.<br/>                                                                                                 |
| <span id="WINBIO_BIR_FIELD_PATRON_ID"></span><span id="winbio_bir_field_patron_id"></span><dl> <dt>**WINBIO \_ \_ \_ \_ ID patron del campo bir**</dt> <dt>0x0004</dt> </dl>                                      | Fornito per conformità con NISTIR 6529-A, CBEFF mecenate Format A, ma non usato.<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_INDEX"></span><span id="winbio_bir_field_index"></span><dl> <dt>**WINBIO \_ \_ \_ Indice del campo bir**</dt> <dt>0x0008</dt> </dl>                                                   | Fornito per conformità con NISTIR 6529-A, CBEFF mecenate Format A, ma non usato.<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_CREATION_DATE"></span><span id="winbio_bir_field_creation_date"></span><dl> <dt>**WINBIO \_ \_ \_ \_ Data creazione campo bir**</dt> <dt>0x0010</dt> </dl>                          | Il membro **CreationDate** è valido.<br/>                                                                                              |
| <span id="WINBIO_BIR_FIELD_VALIDITY_PERIOD"></span><span id="winbio_bir_field_validity_period"></span><dl> <dt>**WINBIO \_ \_Periodo di \_ validità \_ del campo bir**</dt> <dt>0x0020</dt> </dl>                    | Il membro **ValidityPeriod** è valido.<br/>                                                                                            |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_TYPE"></span><span id="winbio_bir_field_biometric_type"></span><dl> <dt>**WINBIO \_ \_ \_ \_ Tipo biometrico del campo bir**</dt> <dt>0x0040</dt> </dl>                       | Il membro del **tipo** è valido.<br/>                                                                                                      |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_SUBTYPE"></span><span id="winbio_bir_field_biometric_subtype"></span><dl> <dt>**WINBIO \_ \_SOTTOtipo \_ biometrico \_ del campo bir**</dt> <dt>0x0080</dt> </dl>              | Il membro del **sottotipo** è valido.<br/>                                                                                                   |
| <span id="WINBIO_BIR_FIELD_CBEFF_HEADER_VERSION"></span><span id="winbio_bir_field_cbeff_header_version"></span><dl> <dt>**WINBIO \_ BIR \_ Field \_ CBEFF \_ header \_ versione**</dt> <dt>0x0100</dt> </dl>    | Il membro **HeaderVersion** è valido.<br/>                                                                                             |
| <span id="WINBIO_BIR_FIELD_PATRON_HEADER_VERSION"></span><span id="winbio_bir_field_patron_header_version"></span><dl> <dt>**WINBIO \_ \_Versione di \_ \_ intestazione patron \_ del campo bir**</dt> <dt>0x0200</dt> </dl> | Il membro **PatronHeaderVersion** è valido.<br/>                                                                                       |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_PURPOSE"></span><span id="winbio_bir_field_biometric_purpose"></span><dl> <dt>**WINBIO \_ Il \_ campo bir 0x0400 \_ \_ scopo biometrico**</dt> <dt></dt> </dl>              | Il membro **scopo** è valido.<br/>                                                                                                   |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_CONDITION"></span><span id="winbio_bir_field_biometric_condition"></span><dl> <dt>**WINBIO \_ \_ \_ \_ Condizione biometrica del campo bir**</dt> <dt>0x0800</dt> </dl>        | Fornito per conformità con NISTIR 6529-A, CBEFF mecenate Format A, ma non usato.<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_QUALITY"></span><span id="winbio_bir_field_quality"></span><dl> <dt>**WINBIO \_ \_ \_ Qualità del campo bir**</dt> <dt>0x1000</dt> </dl>                                             | Il membro **dataquality** è valido.<br/>                                                                                               |
| <span id="WINBIO_BIR_FIELD_CREATOR"></span><span id="winbio_bir_field_creator"></span><dl> <dt>**WINBIO \_ \_ \_ Creatore del campo bir**</dt> <dt>0x2000</dt> </dl>                                             | Fornito per conformità con NISTIR 6529-A, CBEFF mecenate Format A, ma non usato.<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_CHALLENGE"></span><span id="winbio_bir_field_challenge"></span><dl> <dt>**WINBIO \_ 0x4000 \_ di \_ test del campo bir**</dt> <dt></dt> </dl>                                       | Fornito per conformità con NISTIR 6529-A, CBEFF mecenate Format A, ma non usato.<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_PAYLOAD"></span><span id="winbio_bir_field_payload"></span><dl> <dt>**WINBIO \_ \_ \_ Payload campo bir**</dt> <dt>0x8000</dt> </dl>                                             | Fornito per conformità con NISTIR 6529-A, CBEFF mecenate Format A, ma non usato.<br/>                                                   |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                                    |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>\_Tipi WinBio. h (includere WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti dell'applicazione client](client-application-constants.md)
</dt> </dl>

 

 





