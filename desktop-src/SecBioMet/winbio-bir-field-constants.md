---
title: WINBIO_BIR_FIELD costanti (Winbio \_ types.h)
description: Specificare una maschera di bit.
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
ms.openlocfilehash: a354f3119fcef6da3ff204f833616eeb2ac9570cdad0712a87686904ad528958
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035091"
---
# <a name="winbio_bir_field-constants"></a>Costanti FIELD \_ DI WINBIO BIR \_

Le costanti seguenti vengono usate per creare una maschera di bit per il membro **ValidFields** della [**struttura WINBIO \_ BIR \_ HEADER.**](winbio-bir-header.md)



| Costante/valore                                                                                                                                                                                                                                                                                           | Descrizione                                                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_BIR_FIELD_SUBHEAD_COUNT"></span><span id="winbio_bir_field_subhead_count"></span><dl> <dt>**WINBIO \_ CONTEGGIO \_ \_ SUBHEAD \_ CAMPO BIR**</dt> <dt>0x0001</dt> </dl>                          | Fornito per la conformità con NISTIR 6529-A, il Common Biometric Exchange Formats Framework (CBEFF) Format A, ma non usato.<br/> |
| <span id="WINBIO_BIR_FIELD_PRODUCT_ID"></span><span id="winbio_bir_field_product_id"></span><dl> <dt>**WINBIO \_ ID PRODOTTO CAMPO BIR \_ \_ \_ 0x0002**</dt> <dt></dt> </dl>                                   | Il **membro ProductId** è valido.<br/>                                                                                                 |
| <span id="WINBIO_BIR_FIELD_PATRON_ID"></span><span id="winbio_bir_field_patron_id"></span><dl> <dt>**WINBIO \_ ID DEL CAMPO BIR \_ \_ 0X0004 \_**</dt> <dt></dt> </dl>                                      | Fornito per la conformità con NISTIR 6529-A, CBEFF Format A, ma non usato.<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_INDEX"></span><span id="winbio_bir_field_index"></span><dl> <dt>**WINBIO \_ INDICE DEI CAMPI BIR \_ \_ 0x0008**</dt> <dt></dt> </dl>                                                   | Fornito per la conformità con NISTIR 6529-A, CBEFF Format A, ma non usato.<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_CREATION_DATE"></span><span id="winbio_bir_field_creation_date"></span><dl> <dt>**WINBIO \_ DATA DI \_ CREAZIONE \_ CAMPO \_ BIR**</dt> <dt>0x0010</dt> </dl>                          | Il **membro CreationDate** è valido.<br/>                                                                                              |
| <span id="WINBIO_BIR_FIELD_VALIDITY_PERIOD"></span><span id="winbio_bir_field_validity_period"></span><dl> <dt>**WINBIO \_ PERIODO DI \_ \_ VALIDITÀ \_ DEL CAMPO BIR**</dt> <dt>0x0020</dt> </dl>                    | Il **membro ValidityPeriod** è valido.<br/>                                                                                            |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_TYPE"></span><span id="winbio_bir_field_biometric_type"></span><dl> <dt>**WINBIO \_ TIPO BIOMETRICO CAMPO BIR \_ \_ \_ 0x0040**</dt> <dt></dt> </dl>                       | Il **membro Type** è valido.<br/>                                                                                                      |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_SUBTYPE"></span><span id="winbio_bir_field_biometric_subtype"></span><dl> <dt>**WINBIO \_ SOTTOTIPO \_ \_ \_ BIOMETRICO CAMPO BIR**</dt> <dt>0x0080</dt> </dl>              | Il **membro Subtype** è valido.<br/>                                                                                                   |
| <span id="WINBIO_BIR_FIELD_CBEFF_HEADER_VERSION"></span><span id="winbio_bir_field_cbeff_header_version"></span><dl> <dt>**WINBIO \_ VERSIONE \_ DELL'INTESTAZIONE \_ CBEFF \_ DEL \_ CAMPO BIR**</dt> <dt>0x0100</dt> </dl>    | Il **membro HeaderVersion** è valido.<br/>                                                                                             |
| <span id="WINBIO_BIR_FIELD_PATRON_HEADER_VERSION"></span><span id="winbio_bir_field_patron_header_version"></span><dl> <dt>**WINBIO \_ VERSIONE \_ DELL'INTESTAZIONE \_ \_ DEL CAMPO \_ BIR 0X0200**</dt> <dt></dt> </dl> | Il **membroHeaderVersion è** valido.<br/>                                                                                       |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_PURPOSE"></span><span id="winbio_bir_field_biometric_purpose"></span><dl> <dt>**WINBIO \_ BIR \_ FIELD BIOMETRIC PURPOSE \_ \_ 0x0400**</dt> <dt></dt> </dl>              | Il **membro Purpose** è valido.<br/>                                                                                                   |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_CONDITION"></span><span id="winbio_bir_field_biometric_condition"></span><dl> <dt>**WINBIO \_ CONDIZIONE \_ BIOMETRICA \_ \_ DEL CAMPO BIR**</dt> <dt>0x0800</dt> </dl>        | Fornito per la conformità con NISTIR 6529-A, CBEFF Format A, ma non usato.<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_QUALITY"></span><span id="winbio_bir_field_quality"></span><dl> <dt>**WINBIO \_ BIR \_ FIELD \_ QUALITY**</dt> <dt>0x1000</dt> </dl>                                             | Il **membro DataQuality** è valido.<br/>                                                                                               |
| <span id="WINBIO_BIR_FIELD_CREATOR"></span><span id="winbio_bir_field_creator"></span><dl> <dt>**WINBIO \_ BIR \_ FIELD \_ CREATOR**</dt> <dt>0x2000</dt> </dl>                                             | Fornito per la conformità con NISTIR 6529-A, CBEFF Format A, ma non usato.<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_CHALLENGE"></span><span id="winbio_bir_field_challenge"></span><dl> <dt>**WINBIO \_ BIR \_ FIELD \_ CHALLENGE**</dt> <dt>0x4000</dt> </dl>                                       | Fornito per la conformità con NISTIR 6529-A, CBEFF Format A, ma non usato.<br/>                                                   |
| <span id="WINBIO_BIR_FIELD_PAYLOAD"></span><span id="winbio_bir_field_payload"></span><dl> <dt>**WINBIO \_ PAYLOAD DEL \_ CAMPO \_ BIR**</dt> <dt>0x8000</dt> </dl>                                             | Fornito per la conformità con NISTIR 6529-A, CBEFF Format A, ma non usato.<br/>                                                   |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                                    |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Winbio \_ types.h (include Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti dell'applicazione client](client-application-constants.md)
</dt> </dl>

 

 





