---
title: WINBIO_IRIS costanti (Winbio \_ types.h)
description: Specificare i tipi per il riconoscimento dell'iris.
ms.assetid: B1A594E3-6DEA-4071-B40F-569B8094E801
topic_type:
- apiref
api_name:
- WINBIO_IRIS_TYPE_UNKNOWN
- WINBIO_IRIS_LEFT_EYE
- WINBIO_IRIS_RIGHT_EYE
- WINBIO_IRIS_UNSPECIFIED_POS_01
- WINBIO_IRIS_UNSPECIFIED_POS_02
- WINBIO_IRIS_BOTH_EYES
- WINBIO_IRIS_EITHER_EYE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd528bc9a902379591fb6d9587fa66bda9df50ad74cb5e5723f8646a53609a39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909960"
---
# <a name="winbio_iris-constants"></a>Costanti di WINBIO \_ IRIS

Le costanti seguenti sono valori **\_ \_ SUBTYPE BIOMETRICI WINBIO** che possono essere usati per specificare i tipi per il riconoscimento dell'iris oltre ANSI INCITS 379-2004: "Iris Image Interchange Format", che non definisce alcun valore dell'occhio sinistro/destro:



| Costante/valore                                                                                                                                                                                                                                                                   | Descrizione                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_IRIS_TYPE_UNKNOWN_"></span><span id="winbio_iris_type_unknown_"></span><dl> <dt> **TIPO \_ DI WINBIO IRIS \_ \_ SCONOSCIUTO**</dt> <dt>0</dt> </dl>                       | Il tipo di iris è sconosciuto. <br/>                                                                                                                                 |
| <span id="WINBIO_IRIS_LEFT_EYE_"></span><span id="winbio_iris_left_eye_"></span><dl> <dt> **WINBIO \_ IRIS \_ LEFT \_ EYE**</dt> <dt>0xF5</dt> </dl>                               | Il tipo di iris è l'occhio sinistro. <br/>                                                                                                                            |
| <span id="WINBIO_IRIS_RIGHT_EYE_"></span><span id="winbio_iris_right_eye_"></span><dl> <dt> **WINBIO \_ IRIS \_ RIGHT \_ EYE**</dt> <dt>0xF6</dt> </dl>                            | Il tipo di iris è l'occhio destro. <br/>                                                                                                                           |
| <span id="WINBIO_IRIS_UNSPECIFIED_POS_01"></span><span id="winbio_iris_unspecified_pos_01"></span><dl> <dt>**WINBIO \_ IRIS \_ UNSPECIFIED \_ POS \_ 01**</dt> <dt>0xF7</dt> </dl>    | Sottotipo associato al primo modello dell'utente quando un solo occhio è fotogramma della fotocamera e non può essere determinato se si tratta dell'occhio sinistro o destro dell'utente.<br/>  |
| <span id="WINBIO_IRIS_UNSPECIFIED_POS_02_"></span><span id="winbio_iris_unspecified_pos_02_"></span><dl> <dt> **WINBIO \_ IRIS \_ NON SPECIFICATO POS \_ \_ 02**</dt> <dt>0xF8</dt> </dl> | Sottotipo associato al secondo modello dell'utente quando un solo occhio è fotogramma della fotocamera e non può essere determinato se si tratta dell'occhio sinistro o destro dell'utente.<br/> |
| <span id="WINBIO_IRIS_BOTH_EYES_"></span><span id="winbio_iris_both_eyes_"></span><dl> <dt> **WINBIO \_ IRIS \_ BOTH \_ EYES**</dt> <dt>0xF9</dt> </dl>                             | Il tipo di iris è entrambi gli occhi. <br/>                                                                                                                               |
| <span id="WINBIO_IRIS_EITHER_EYE_"></span><span id="winbio_iris_either_eye_"></span><dl> <dt> **WINBIO \_ IRIS \_ 0XFA \_**</dt> <dt></dt> </dl>                          | Il tipo di iris è eye. <br/>                                                                                                                              |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                                   |
| Server minimo supportato<br/> | \[Windows Server 2016 solo app desktop\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Winbio \_ types.h (include Winbio.h)</dt> </dl> |



 

 





