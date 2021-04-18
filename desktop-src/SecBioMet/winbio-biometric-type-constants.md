---
title: Costanti WINBIO_BIOMETRIC_TYPE (tipi WinBio \_ . h)
description: Tipi di biometria standard definiti da National Institute of Standards and Technology Information (NISTIR) 6529-A, noto anche come CBEFF (Common biometria Exchange formats Framework).
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
ms.openlocfilehash: f2d2ab5c41a3c2af26312c97a67d1179b50fd759
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301635"
---
# <a name="winbio_biometric_type-constants"></a>\_ \_ Costanti di tipo biometrico WINBIO

Le costanti seguenti rappresentano i tipi biometrici standard definiti da National Institute of Standards and Technology Information (NISTIR) 6529-A, altrimenti noto come il formato comune CBEFF (Biometric Exchange formats Framework) A. Attualmente è supportata solo l' **\_ \_ impronta digitale di tipo WINBIO** .



| Costante                                                                                                                                                                                                            | Descrizione                                                                                                                              |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_STANDARD_TYPE_MASK"></span><span id="winbio_standard_type_mask"></span><dl> <dt>**\_maschera di \_ tipo \_ standard WINBIO**</dt> </dl>                 | Maschera di maschera che specifica il set supportato di fattori biometrici.<br/>                                                                |
| <span id="WINBIO_NO_TYPE_AVAILABLE"></span><span id="winbio_no_type_available"></span><dl> <dt>**WINBIO \_ non \_ è \_ disponibile alcun tipo**</dt> </dl>                    | Nessun tipo di biometria disponibile.<br/>                                                                                               |
| <span id="WINBIO_TYPE_MULTIPLE"></span><span id="winbio_type_multiple"></span><dl> <dt>**WINBIO di \_ tipo \_ multiplo**</dt> </dl>                                 | Sono stati specificati più tipi.<br/>                                                                                                 |
| <span id="WINBIO_TYPE_FACIAL_FEATURES"></span><span id="winbio_type_facial_features"></span><dl> <dt>**\_ \_ funzionalità facciali del tipo WINBIO \_**</dt> </dl>           | Le funzionalità facciali vengono usate per determinare l'identità di un singolo utente.<br/>                                                          |
| <span id="WINBIO_TYPE_VOICE"></span><span id="winbio_type_voice"></span><dl> <dt>**WINBIO \_ tipo \_ voce**</dt> </dl>                                          | Per determinare l'identità di un singolo utente vengono usati i modelli di frequenza e volume nella voce di un utente.<br/>              |
| <span id="WINBIO_TYPE_FINGERPRINT"></span><span id="winbio_type_fingerprint"></span><dl> <dt>**\_impronta digitale di tipo WINBIO \_**</dt> </dl>                        | I modelli di impronta digitale vengono usati per determinare l'identità di un singolo utente.<br/>                                                     |
| <span id="WINBIO_TYPE_IRIS"></span><span id="winbio_type_iris"></span><dl> <dt>**WINBIO \_ tipo \_ Iris**</dt> </dl>                                             | I modelli Iris vengono usati per determinare l'identità di un singolo utente. Questo valore è supportato a partire da Windows 10.<br/>            |
| <span id="WINBIO_TYPE_RETINA"></span><span id="winbio_type_retina"></span><dl> <dt>**WINBIO di \_ tipo \_ retina**</dt> </dl>                                       | Per determinare l'identità di un utente, vengono usati i modelli di vena della retina.<br/>                                              |
| <span id="WINBIO_TYPE_HAND_GEOMETRY"></span><span id="winbio_type_hand_geometry"></span><dl> <dt>**\_geometria della \_ mano di tipo WINBIO \_**</dt> </dl>                 | La forma di una mano di un individuo viene utilizzata per determinare l'identità di un singolo utente.<br/>                                      |
| <span id="WINBIO_TYPE_SIGNATURE_DYNAMICS"></span><span id="winbio_type_signature_dynamics"></span><dl> <dt>**\_Dynamics della \_ firma del tipo WINBIO \_**</dt> </dl>  | I modelli di forza che il singolo utente utilizza quando firmano il nome vengono utilizzati per determinare l'identità di un singolo utente.<br/> |
| <span id="WINBIO_TYPE_KEYSTROKE_DYNAMICS"></span><span id="winbio_type_keystroke_dynamics"></span><dl> <dt>**\_dinamica della \_ sequenza di tasti di tipo WINBIO \_**</dt> </dl>  | I modelli di velocità e di errore nella digitazione da parte di un utente vengono usati per determinare l'identità di un singolo utente.<br/>                  |
| <span id="WINBIO_TYPE_LIP_MOVEMENT"></span><span id="winbio_type_lip_movement"></span><dl> <dt>**\_spostamento del \_ labbro di tipo WINBIO \_**</dt> </dl>                    | Le modifiche apportate alle labbra di un utente che si verificano quando vengono usate per determinare l'identità di un singolo utente.<br/>      |
| <span id="WINBIO_TYPE_THERMAL_FACE_IMAGE"></span><span id="winbio_type_thermal_face_image"></span><dl> <dt>**\_immagine della \_ \_ faccia termica del tipo \_ WINBIO**</dt> </dl> | Per determinare l'identità di un utente, vengono usati i modelli di temperatura in un singolo utente.<br/>                    |
| <span id="WINBIO_TYPE_THERMAL_HAND_IMAGE"></span><span id="winbio_type_thermal_hand_image"></span><dl> <dt>**\_immagine della \_ \_ mano termica del tipo \_ WINBIO**</dt> </dl> | Per determinare l'identità di un utente, vengono usati i modelli di temperatura a disposizione di un singolo utente.<br/>                    |
| <span id="WINBIO_TYPE_GAIT"></span><span id="winbio_type_gait"></span><dl> <dt>**\_andamento del tipo WINBIO \_**</dt> </dl>                                             | I modelli di movimento che si verificano quando i singoli percorsi vengono usati per determinare l'identità di un singolo utente.<br/>            |
| <span id="WINBIO_TYPE_SCENT"></span><span id="winbio_type_scent"></span><dl> <dt>**\_profumo del tipo WINBIO \_**</dt> </dl>                                          | Il profumo di un individuo viene usato per determinare l'identità di un singolo utente.<br/>                                                |
| <span id="WINBIO_TYPE_DNA"></span><span id="winbio_type_dna"></span><dl> <dt>**WINBIO di \_ tipo \_ DNA**</dt> </dl>                                                | Le sequenze acid (DNA) deossiribonucleico vengono usate per determinare l'identità di un singolo utente.<br/>                                    |
| <span id="WINBIO_TYPE_EAR_SHAPE"></span><span id="winbio_type_ear_shape"></span><dl> <dt>**\_ \_ forma Ear di tipo WINBIO \_**</dt> </dl>                             | La forma di un orecchio del singolo viene utilizzata per determinare l'identità di un singolo utente.<br/>                                     |
| <span id="WINBIO_TYPE_FINGER_GEOMETRY"></span><span id="winbio_type_finger_geometry"></span><dl> <dt>**WINBIO \_ digitare \_ la \_ geometria del dito**</dt> </dl>           | Le forme delle dita di una persona vengono usate per determinare l'identità di un singolo utente.<br/>                               |
| <span id="WINBIO_TYPE_PALM_PRINT"></span><span id="winbio_type_palm_print"></span><dl> <dt>**WINBIO \_ tipo \_ di \_ stampa Palm**</dt> </dl>                          | La forma della palma viene utilizzata per determinare l'identità di un singolo utente.<br/>                                                     |
| <span id="WINBIO_TYPE_VEIN_PATTERN"></span><span id="winbio_type_vein_pattern"></span><dl> <dt>**\_modello di \_ vena del tipo WINBIO \_**</dt> </dl>                    | I modelli nelle vene sotto l'interfaccia della mano di un individuo vengono usati per determinare l'identità di un singolo utente.<br/>   |
| <span id="WINBIO_TYPE_FOOT_PRINT"></span><span id="winbio_type_foot_print"></span><dl> <dt>**stampa del piè di WINBIO di \_ tipo \_ \_**</dt> </dl>                          | La forma del piede viene utilizzata per determinare l'identità di un singolo utente.<br/>                                                     |
| <span id="WINBIO_TYPE_OTHER"></span><span id="winbio_type_other"></span><dl> <dt>**WINBIO \_ tipo \_ altro**</dt> </dl>                                          | I dati biometrici supportati non sono definiti dalle costanti correnti.<br/>                                                         |
| <span id="WINBIO_TYPE_PASSWORD"></span><span id="winbio_type_password"></span><dl> <dt>**WINBIO \_ tipo di \_ password**</dt> </dl>                                 | I dati della password vengono usati per determinare l'identità di un singolo utente.<br/>                                                             |
| <span id="WINBIO_TYPE_ANY"></span><span id="winbio_type_any"></span><dl> <dt>**WINBIO \_ tipo \_ any**</dt> </dl>                                                | Qualsiasi tipo di dati viene utilizzato per determinare l'identità di un singolo utente.<br/>                                                          |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                                                                                               |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                                                                                                  |
| Intestazione<br/>                   | <dl> <dt>WinBio \_ types. h (includere WinBio. h per le applicazioni client o WinBio \_ Adapters. h per gli adapter)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti dell'applicazione client](client-application-constants.md)
</dt> </dl>

 

 





