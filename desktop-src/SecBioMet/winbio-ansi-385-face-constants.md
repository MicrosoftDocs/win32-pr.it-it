---
title: WINBIO_ANSI_385_FACE costanti (Winbio \_ types.h)
description: Specificare i tipi di immagine del viso frontale per il riconoscimento facciale.
ms.assetid: 16D21E40-C158-4674-80D0-AE9494124B96
topic_type:
- apiref
api_name:
- WINBIO_ANSI_385_FACE_TYPE_UNKNOWN
- WINBIO_ANSI_385_FACE_FRONTAL_FULL
- WINBIO_ANSI_385_FACE_FRONTAL_TOKEN
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6bd8ddc173915e2bbd912a6a668c63b4be733f32357189fe6ff3365a20bacfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119410311"
---
# <a name="winbio_ansi_385_face-constants"></a>Costanti \_ FACE WINBIO ANSI \_ 385 \_

Le costanti seguenti sono valori **\_ \_ SUBTYPE BIOMETRIC WINBIO** che possono essere usati per specificare i due tipi di immagini frontali del viso, come definito da ANSI INCITS 385-2004: "Face Recognition Format for Data Interchange": risoluzione completa e risoluzione bassa. In pratica, il framework biometrico userà solo immagini a risoluzione completa per il riconoscimento facciale.



| Costante/valore                                                                                                                                                                                                                                                                          | Descrizione                                                |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------|
| <span id="WINBIO_ANSI_385_FACE_TYPE_UNKNOWN"></span><span id="winbio_ansi_385_face_type_unknown"></span><dl> <dt>**WINBIO \_ ANSI \_ 385 \_ FACE TYPE \_ \_ UNKNOWN**</dt> <dt>0</dt> </dl>    | Il tipo di immagine del viso frontale è sconosciuto.<br/>         |
| <span id="WINBIO_ANSI_385_FACE_FRONTAL_FULL"></span><span id="winbio_ansi_385_face_frontal_full"></span><dl> <dt>**WINBIO \_ ANSI \_ 385 \_ FACE \_ FRONTAL \_ FULL**</dt> <dt>1</dt> </dl>    | Il tipo di immagine frontale del viso è la risoluzione completa.<br/> |
| <span id="WINBIO_ANSI_385_FACE_FRONTAL_TOKEN"></span><span id="winbio_ansi_385_face_frontal_token"></span><dl> <dt>**WINBIO \_ ANSI \_ 385 \_ FACE \_ FRONTAL \_ TOKEN**</dt> <dt>2</dt> </dl> | Il tipo di immagine frontale del viso è a bassa risoluzione.<br/>  |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                                   |
| Server minimo supportato<br/> | \[Windows Server 2016 solo app desktop\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Winbio \_ types.h (include Winbio.h)</dt> </dl> |



 

 





