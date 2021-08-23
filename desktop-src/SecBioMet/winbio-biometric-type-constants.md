---
title: WINBIO_BIOMETRIC_TYPE costanti (Winbio \_ types.h)
description: Tipi biometrici standard definiti dal National Institute of Standards and Technology Information (NISTIR) 6529-A, altrimenti noto come Common Biometric Exchange Formats Framework (CBEFF) Formato patrocinatore A.
ms.assetid: DCBDB5F9-FF81-44C1-B439-2B8C02483212
topic_type:
- apiref
api_name:
- WINBIO_STANDARD_TYPE_MASK
- WINBIO_NO_TYPE_AVAILABLE
- WINBIO_TYPE_MULTIPLE
- WINBIO_TYPE_FACIAL_FEATURES
- WINBIO_TYPE_VOICE
- WINBIO_TYPE_FINGERPRINT
- WINBIO_TYPE_IRIS
- WINBIO_TYPE_RETINA
- WINBIO_TYPE_HAND_GEOMETRY
- WINBIO_TYPE_SIGNATURE_DYNAMICS
- WINBIO_TYPE_KEYSTROKE_DYNAMICS
- WINBIO_TYPE_LIP_MOVEMENT
- WINBIO_TYPE_THERMAL_FACE_IMAGE
- WINBIO_TYPE_THERMAL_HAND_IMAGE
- WINBIO_TYPE_GAIT
- WINBIO_TYPE_SCENT
- WINBIO_TYPE_DNA
- WINBIO_TYPE_EAR_SHAPE
- WINBIO_TYPE_FINGER_GEOMETRY
- WINBIO_TYPE_PALM_PRINT
- WINBIO_TYPE_VEIN_PATTERN
- WINBIO_TYPE_FOOT_PRINT
- WINBIO_TYPE_OTHER
- WINBIO_TYPE_PASSWORD
- WINBIO_TYPE_ANY
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c1b6475433d2c0d1432e7501e6cbda46436c5a54fd13d5f254f79b678b3f7bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911070"
---
# <a name="winbio_biometric_type-constants"></a>Costanti DI TIPO \_ BIOMETRICO WINBIO \_

Le costanti seguenti rappresentano i tipi biometrici standard definiti dal National Institute of Standards and Technology Information (NISTIR) 6529-A, altrimenti noto come Common Biometric Exchange Formats Framework (CBEFF) Formato del patrocinatore A. Attualmente è supportata solo l'impronta digitale DEL TIPO **WINBIO. \_ \_**



| Costante                                                                                                                                                                                                            | Descrizione                                                                                                                              |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_STANDARD_TYPE_MASK"></span><span id="winbio_standard_type_mask"></span><dl> <dt>**MASCHERA DI TIPO STANDARD WINBIO \_ \_ \_**</dt> </dl>                 | Maschera di bit che specifica il set supportato di fattori biometrici.<br/>                                                                |
| <span id="WINBIO_NO_TYPE_AVAILABLE"></span><span id="winbio_no_type_available"></span><dl> <dt>**WINBIO \_ NESSUN \_ TIPO \_ DISPONIBILE**</dt> </dl>                    | Nessun tipo biometrico disponibile.<br/>                                                                                               |
| <span id="WINBIO_TYPE_MULTIPLE"></span><span id="winbio_type_multiple"></span><dl> <dt>**WINBIO \_ TYPE \_ MULTIPLE**</dt> </dl>                                 | Vengono specificati più tipi.<br/>                                                                                                 |
| <span id="WINBIO_TYPE_FACIAL_FEATURES"></span><span id="winbio_type_facial_features"></span><dl> <dt>**CARATTERISTICHE FACCIALI DI TIPO WINBIO \_ \_ \_**</dt> </dl>           | Le caratteristiche facciali vengono usate per determinare l'identità di un singolo utente.<br/>                                                          |
| <span id="WINBIO_TYPE_VOICE"></span><span id="winbio_type_voice"></span><dl> <dt>**WINBIO \_ TYPE \_ VOICE**</dt> </dl>                                          | I modelli di frequenza e volume nella voce di un singolo utente vengono usati per determinare l'identità di un singolo utente.<br/>              |
| <span id="WINBIO_TYPE_FINGERPRINT"></span><span id="winbio_type_fingerprint"></span><dl> <dt>**IMPRONTA DIGITALE DEL TIPO WINBIO \_ \_**</dt> </dl>                        | I modelli di impronta digitale vengono usati per determinare l'identità di un singolo utente.<br/>                                                     |
| <span id="WINBIO_TYPE_IRIS"></span><span id="winbio_type_iris"></span><dl> <dt>**IRIS DI TIPO WINBIO \_ \_**</dt> </dl>                                             | I modelli Iris vengono usati per determinare l'identità di un singolo utente. Questo valore è supportato a partire da Windows 10.<br/>            |
| <span id="WINBIO_TYPE_RETINA"></span><span id="winbio_type_retina"></span><dl> <dt>**RETINA DI TIPO WINBIO \_ \_**</dt> </dl>                                       | I modelli di vena nella retina vengono usati per determinare l'identità di un singolo utente.<br/>                                              |
| <span id="WINBIO_TYPE_HAND_GEOMETRY"></span><span id="winbio_type_hand_geometry"></span><dl> <dt>**GEOMETRIA MANUALE DI TIPO WINBIO \_ \_ \_**</dt> </dl>                 | La forma di una mano di una persona viene usata per determinare l'identità di un singolo utente.<br/>                                      |
| <span id="WINBIO_TYPE_SIGNATURE_DYNAMICS"></span><span id="winbio_type_signature_dynamics"></span><dl> <dt>**DINAMICA DELLA FIRMA DEL TIPO WINBIO \_ \_ \_**</dt> </dl>  | I modelli di forza usati dall'utente quando firmano il nome vengono usati per determinare l'identità di un singolo utente.<br/> |
| <span id="WINBIO_TYPE_KEYSTROKE_DYNAMICS"></span><span id="winbio_type_keystroke_dynamics"></span><dl> <dt>**WINBIO \_ TYPE \_ KEYSTROKE \_ DYNAMICS**</dt> </dl>  | I modelli di velocità ed errore nella digitazione da parte di un singolo utente vengono usati per determinare l'identità di un singolo utente.<br/>                  |
| <span id="WINBIO_TYPE_LIP_MOVEMENT"></span><span id="winbio_type_lip_movement"></span><dl> <dt>**SPOSTAMENTO LIP WINBIO \_ \_ \_**</dt> </dl>                    | Per determinare l'identità di un singolo utente vengono usate le modifiche nella bocca di un individuo che si verificano quando parla.<br/>      |
| <span id="WINBIO_TYPE_THERMAL_FACE_IMAGE"></span><span id="winbio_type_thermal_face_image"></span><dl> <dt>**IMMAGINE DEL VISO \_ \_ \_ TERMICO DI TIPO WINBIO \_**</dt> </dl> | Per determinare l'identità di un singolo utente vengono usati i modelli di temperatura di fronte a un singolo utente.<br/>                    |
| <span id="WINBIO_TYPE_THERMAL_HAND_IMAGE"></span><span id="winbio_type_thermal_hand_image"></span><dl> <dt>**IMMAGINE DELLA MANO \_ \_ TERMICA DI \_ TIPO \_ WINBIO**</dt> </dl> | I modelli di temperatura nella mano di un singolo utente vengono usati per determinare l'identità di un individuo.<br/>                    |
| <span id="WINBIO_TYPE_GAIT"></span><span id="winbio_type_gait"></span><dl> <dt>**GAIT DI TIPO WINBIO \_ \_**</dt> </dl>                                             | Modelli di spostamento che si verificano quando le singole spostamenti vengono usate per determinare l'identità di un singolo utente.<br/>            |
| <span id="WINBIO_TYPE_SCENT"></span><span id="winbio_type_scent"></span><dl> <dt>**WINBIO \_ TYPE \_ AROMI**</dt> </dl>                                          | Per determinare l'identità di un singolo utente viene usata l'insoddre di un individuo.<br/>                                                |
| <span id="WINBIO_TYPE_DNA"></span><span id="winbio_type_dna"></span><dl> <dt>**DNA DI TIPO WINBIO \_ \_**</dt> </dl>                                                | Le sequenze di acidi deossiribonucleici (DNA) vengono usate per determinare l'identità di un individuo.<br/>                                    |
| <span id="WINBIO_TYPE_EAR_SHAPE"></span><span id="winbio_type_ear_shape"></span><dl> <dt>**FORMA \_ DELL'ORECCHINO DI \_ TIPO WINBIO \_**</dt> </dl>                             | La forma di un orecchino dell'individuo viene usata per determinare l'identità di un individuo.<br/>                                     |
| <span id="WINBIO_TYPE_FINGER_GEOMETRY"></span><span id="winbio_type_finger_geometry"></span><dl> <dt>**GEOMETRIA DELLE \_ DITA \_ DI TIPO WINBIO \_**</dt> </dl>           | Le forme delle dita di un individuo vengono usate per determinare l'identità di un individuo.<br/>                               |
| <span id="WINBIO_TYPE_PALM_PRINT"></span><span id="winbio_type_palm_print"></span><dl> <dt>**STAMPA PALM DI TIPO WINBIO \_ \_ \_**</dt> </dl>                          | La forma del palmo viene usata per determinare l'identità di un singolo utente.<br/>                                                     |
| <span id="WINBIO_TYPE_VEIN_PATTERN"></span><span id="winbio_type_vein_pattern"></span><dl> <dt>**MODELLO \_ \_ VEIN DI TIPO WINBIO \_**</dt> </dl>                    | I modelli nelle vene sotto l'interfaccia della mano di un individuo vengono usati per determinare l'identità di un individuo.<br/>   |
| <span id="WINBIO_TYPE_FOOT_PRINT"></span><span id="winbio_type_foot_print"></span><dl> <dt>**STAMPA WINBIO \_ TYPE \_ FOOT \_**</dt> </dl>                          | La forma del piede viene usata per determinare l'identità di un individuo.<br/>                                                     |
| <span id="WINBIO_TYPE_OTHER"></span><span id="winbio_type_other"></span><dl> <dt>**TIPO DI WINBIO \_ \_ ALTRO**</dt> </dl>                                          | I dati biometrici supportati non sono definiti dalle costanti correnti.<br/>                                                         |
| <span id="WINBIO_TYPE_PASSWORD"></span><span id="winbio_type_password"></span><dl> <dt>**PASSWORD DI TIPO WINBIO \_ \_**</dt> </dl>                                 | I dati delle password vengono usati per determinare l'identità di un singolo utente.<br/>                                                             |
| <span id="WINBIO_TYPE_ANY"></span><span id="winbio_type_any"></span><dl> <dt>**TIPO WINBIO \_ \_ ANY**</dt> </dl>                                                | Qualsiasi tipo di dati viene usato per determinare l'identità di un singolo utente.<br/>                                                          |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                                                                                               |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                                                                                                  |
| Intestazione<br/>                   | <dl> <dt>Winbio \_ types.h (includere Winbio.h per le applicazioni client o Adapters.h Winbio \_ per gli adapter)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti dell'applicazione client](client-application-constants.md)
</dt> </dl>

 

 





