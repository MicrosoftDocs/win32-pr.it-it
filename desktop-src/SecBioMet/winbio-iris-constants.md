---
title: Costanti WINBIO_IRIS (tipi WinBio \_ . h)
description: Specificare i tipi per il riconoscimento Iris.
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
ms.openlocfilehash: b61e65505b8ef55b0fdc2dc9d8f5312e24856602
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477489"
---
# <a name="winbio_iris-constants"></a>\_Costanti Iris WINBIO

Le costanti seguenti sono valori **dei \_ \_ SOTTOtipi biometrici WINBIO** che possono essere usati per specificare i tipi per il riconoscimento Iris oltre ANSI gli inci 379-2004: "formato di interscambio immagini Iris", che non definisce alcun valore di occhio sinistro/destro:



| Costante/valore                                                                                                                                                                                                                                                                   | Descrizione                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_IRIS_TYPE_UNKNOWN_"></span><span id="winbio_iris_type_unknown_"></span><dl> <dt> **\_ Tipo Iris \_ WINBIO \_ sconosciuto**</dt> <dt>0</dt> </dl>                       | Il tipo di Iris è sconosciuto. <br/>                                                                                                                                 |
| <span id="WINBIO_IRIS_LEFT_EYE_"></span><span id="winbio_iris_left_eye_"></span><dl> <dt> **WINBIO \_ Iris \_ Left- \_ Eye**</dt> <dt>0xf5</dt> </dl>                               | Il tipo Iris è l'occhio sinistro. <br/>                                                                                                                            |
| <span id="WINBIO_IRIS_RIGHT_EYE_"></span><span id="winbio_iris_right_eye_"></span><dl> <dt> **WINBIO \_ Iris \_ a \_ destra**</dt> <dt>0XF6</dt> </dl>                            | Il tipo Iris è l'occhio destro. <br/>                                                                                                                           |
| <span id="WINBIO_IRIS_UNSPECIFIED_POS_01"></span><span id="winbio_iris_unspecified_pos_01"></span><dl> <dt>**WINBIO \_ IRIS non \_ specificato \_ POS \_ 01**</dt> <dt>0xf7</dt> </dl>    | Sottotipo associato a un primo modello utente quando solo un occhio è la cornice della fotocamera e non può essere determinato se è l'occhio sinistro o destro dell'utente.<br/>  |
| <span id="WINBIO_IRIS_UNSPECIFIED_POS_02_"></span><span id="winbio_iris_unspecified_pos_02_"></span><dl> <dt> **WINBIO \_ Iris non \_ specificato \_ POS \_ 02**</dt> <dt>0xF8</dt> </dl> | Sottotipo associato a un secondo modello utente quando solo un occhio è il fotogramma della fotocamera e non può essere determinato se è l'occhio sinistro o destro dell'utente.<br/> |
| <span id="WINBIO_IRIS_BOTH_EYES_"></span><span id="winbio_iris_both_eyes_"></span><dl> <dt> **WINBIO \_ Iris \_ entrambi \_ gli occhi**</dt> <dt>0xF9</dt> </dl>                             | Il tipo Iris è entrambi gli occhi. <br/>                                                                                                                               |
| <span id="WINBIO_IRIS_EITHER_EYE_"></span><span id="winbio_iris_either_eye_"></span><dl> <dt> **WINBIO \_ Iris \_ \_ occhio**</dt> <dt>0xFA</dt> </dl>                          | Il tipo di Iris è Eye. <br/>                                                                                                                              |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                                   |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2016\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>\_Tipi WinBio. h (includere WinBio. h)</dt> </dl> |



 

 





