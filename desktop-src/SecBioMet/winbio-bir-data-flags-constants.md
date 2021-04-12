---
title: Costanti WINBIO_BIR_DATA_FLAGS (tipi WinBio \_ . h)
description: Consente di specificare la condizione dei dati.
ms.assetid: F6F7F68A-3294-4AF8-A1A7-C6A869A2CC3C
topic_type:
- apiref
api_name:
- WINBIO_DATA_FLAG_PRIVACY
- WINBIO_DATA_FLAG_INTEGRITY
- WINBIO_DATA_FLAG_SIGNED
- WINBIO_DATA_FLAG_RAW
- WINBIO_DATA_FLAG_INTERMEDIATE
- WINBIO_DATA_FLAG_PROCESSED
- WINBIO_DATA_FLAG_OPTION_MASK_PRESENT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8195cf17040c35b9e42f8977b36c5ddc6f2ea33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400926"
---
# <a name="winbio_bir_data_flags-constants"></a>\_ \_ Costanti flag di dati WINBIO bir \_

Le costanti seguenti vengono usate dal membro **Dataflags** della struttura dell' [**intestazione WINBIO \_ Bir \_**](winbio-bir-header.md) .



| Costante/valore                                                                                                                                                                                                                                                                                   | Descrizione                                                                                                                                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_FLAG_PRIVACY"></span><span id="winbio_data_flag_privacy"></span><dl> <dt>**WINBIO \_ 0x02 \_ \_ privacy del flag di dati**</dt> <dt></dt> </dl>                                       | I dati sono crittografati.<br/>                                                                                                                                                                                 |
| <span id="WINBIO_DATA_FLAG_INTEGRITY"></span><span id="winbio_data_flag_integrity"></span><dl> <dt>**WINBIO \_ \_ \_ Integrità del flag di dati**</dt> <dt>0x01</dt> </dl>                                 | I dati sono firmati digitalmente o sono protetti da un codice MAC (Message Authentication Code).<br/>                                                                                                                   |
| <span id="WINBIO_DATA_FLAG_SIGNED"></span><span id="winbio_data_flag_signed"></span><dl> <dt>**WINBIO \_ FLAG di dati con \_ \_ segno**</dt> <dt>0x04</dt> </dl>                                          | Se vengono impostati questo flag e il flag di **\_ integrità del \_ flag \_ di dati WINBIO** , i dati vengono firmati. Se questo flag non è impostato ma è impostato il flag di **\_ integrità del \_ flag \_ di dati WINBIO** , viene calcolato un Mac sui dati.<br/> |
| <span id="WINBIO_DATA_FLAG_RAW"></span><span id="winbio_data_flag_raw"></span><dl> <dt>**WINBIO \_ FLAG di dati 0x20 \_ \_ RAW**</dt> <dt></dt> </dl>                                                   | I dati sono nel formato con cui sono stati acquisiti.<br/>                                                                                                                                                  |
| <span id="WINBIO_DATA_FLAG_INTERMEDIATE"></span><span id="winbio_data_flag_intermediate"></span><dl> <dt>**WINBIO \_ 0x40 \_ \_ intermedio del flag di dati**</dt> <dt></dt> </dl>                        | I dati non sono elaborati ma non sono stati completamente elaborati.<br/>                                                                                                                                             |
| <span id="WINBIO_DATA_FLAG_PROCESSED"></span><span id="winbio_data_flag_processed"></span><dl> <dt>**WINBIO \_ FLAG di dati \_ \_ elaborati**</dt> <dt>0x80</dt> </dl>                                 | I dati sono stati elaborati.<br/>                                                                                                                                                                           |
| <span id="WINBIO_DATA_FLAG_OPTION_MASK_PRESENT"></span><span id="winbio_data_flag_option_mask_present"></span><dl> <dt>**WINBIO \_ Maschera di opzione del flag di dati \_ \_ \_ \_ presente**</dt> <dt>0x08</dt> </dl> | Maschera del flag. Questo valore è sempre uno (1).<br/>                                                                                                                                                           |



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

 

 





