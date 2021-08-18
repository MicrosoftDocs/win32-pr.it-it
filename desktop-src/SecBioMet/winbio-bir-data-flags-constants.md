---
title: WINBIO_BIR_DATA_FLAGS costanti (Winbio \_ types.h)
description: Specificare la condizione dei dati.
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
ms.openlocfilehash: 87769500de02dedc7247b15e94064a43b7c6d528234c27ad700d4a336f42a092
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622631"
---
# <a name="winbio_bir_data_flags-constants"></a>Costanti DI \_ WINBIO BIR \_ DATA \_ FLAGS

Le costanti seguenti vengono usate dal **membro DataFlags** della struttura [**WINBIO \_ BIR \_ HEADER.**](winbio-bir-header.md)



| Costante/valore                                                                                                                                                                                                                                                                                   | Descrizione                                                                                                                                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_FLAG_PRIVACY"></span><span id="winbio_data_flag_privacy"></span><dl> <dt>**WINBIO \_ DATA \_ FLAG \_ PRIVACY**</dt> <dt>0x02</dt> </dl>                                       | I dati sono crittografati.<br/>                                                                                                                                                                                 |
| <span id="WINBIO_DATA_FLAG_INTEGRITY"></span><span id="winbio_data_flag_integrity"></span><dl> <dt>**WINBIO \_ INTEGRITÀ \_ DEI FLAG \_ DI**</dt> <dt>DATI 0x01</dt> </dl>                                 | I dati sono firmati digitalmente o sono protetti da un codice mac (Message Authentication Code).<br/>                                                                                                                   |
| <span id="WINBIO_DATA_FLAG_SIGNED"></span><span id="winbio_data_flag_signed"></span><dl> <dt>**WINBIO \_ FLAG \_ DI \_ DATI FIRMATO**</dt> <dt>0X04</dt> </dl>                                          | Se questo flag e il flag **WINBIO \_ DATA FLAG INTEGRITY \_ \_ sono** impostati, i dati vengono firmati. Se questo flag non è impostato ma il flag **WINBIO \_ DATA \_ FLAG \_ INTEGRITY** è impostato, viene calcolato un MAC sui dati.<br/> |
| <span id="WINBIO_DATA_FLAG_RAW"></span><span id="winbio_data_flag_raw"></span><dl> <dt>**WINBIO \_ FLAG \_ \_ DI**</dt> DATI NON <dt>0X20</dt> </dl>                                                   | I dati sono nel formato con cui sono stati acquisiti.<br/>                                                                                                                                                  |
| <span id="WINBIO_DATA_FLAG_INTERMEDIATE"></span><span id="winbio_data_flag_intermediate"></span><dl> <dt>**WINBIO \_ FLAG \_ DI \_ DATI INTERMEDI**</dt> <dt>0X40</dt> </dl>                        | I dati non sono elaborati, ma non sono stati elaborati completamente.<br/>                                                                                                                                             |
| <span id="WINBIO_DATA_FLAG_PROCESSED"></span><span id="winbio_data_flag_processed"></span><dl> <dt>**WINBIO \_ FLAG \_ DI \_ DATI ELABORATO**</dt> <dt>0x80</dt> </dl>                                 | I dati sono stati elaborati.<br/>                                                                                                                                                                           |
| <span id="WINBIO_DATA_FLAG_OPTION_MASK_PRESENT"></span><span id="winbio_data_flag_option_mask_present"></span><dl> <dt>**WINBIO \_ DATA \_ FLAG OPTION MASK PRESENT \_ \_ \_ 0x08**</dt> <dt></dt> </dl> | Maschera del flag. Questo valore è sempre uno (1).<br/>                                                                                                                                                           |



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

 

 





