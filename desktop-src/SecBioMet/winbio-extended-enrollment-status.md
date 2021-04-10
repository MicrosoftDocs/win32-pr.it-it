---
title: Struttura WINBIO_EXTENDED_ENROLLMENT_STATUS ( \_ tipi WINBIO. h)
description: Contiene informazioni aggiuntive sullo stato di una registrazione in corso.
ms.assetid: 2FDDF4D3-6A3E-4DF5-ACA4-423F893C6F2B
keywords:
- Struttura di WINBIO_EXTENDED_ENROLLMENT_STATUS Windows Biometric Framework API
- API Windows Biometric Framework puntatore alla struttura PWINBIO_EXTENDED_ENROLLMENT_STATUS
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_ENROLLMENT_STATUS
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 937e56e438feadc646329c673af4454cb39eaddd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119219"
---
# <a name="winbio_extended_enrollment_status-structure"></a>WINBIO \_ \_ \_ struttura dello stato di registrazione estesa

Contiene informazioni aggiuntive sullo stato di una registrazione in corso.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _WINBIO_EXTENDED_ENROLLMENT_STATUS {
  HRESULT                  TemplateStatus;
  WINBIO_REJECT_DETAIL     RejectDetail;
  ULONG                    PercentComplete;
  WINBIO_BIOMETRIC_TYPE    Factor;
  WINBIO_BIOMETRIC_SUBTYPE SubFactor;
  union {
    ULONG32 Null;
    struct {
      RECT BoundingBox;
      LONG Distance;
    } FacialFeatures;
    struct {
      ULONG GeneralSamples;
      ULONG Center;
      ULONG TopEdge;
      ULONG BottomEdge;
      ULONG LeftEdge;
      ULONG RightEdge;
    } Fingerprint;
    struct {
      RECT  EyeBoundingBox_1;
      RECT  EyeBoundingBox_2;
      POINT PupilCenter_1;
      POINT PupilCenter_2;
      LONG  Distance;
    } Iris;
    struct {
      ULONG32 Reserved;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_ENROLLMENT_STATUS, *PWINBIO_EXTENDED_ENROLLMENT_STATUS;
```



## <a name="members"></a>Members

<dl> <dt>

**TemplateStatus**
</dt> <dd>

Stato della raccolta di esempi per il modello di registrazione. Per questo membro sono possibili i valori seguenti.



| Valore                                                                                                                                                                                                  | Significato                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <dt>**\_OK**</dt> </dl>                                                                     | La registrazione è pronta per essere salvata.<br/>                |
| <span id="WINBIO_E_INVALID_OPERATION"></span><span id="winbio_e_invalid_operation"></span><dl> <dt>**\_operazione WINBIO E \_ non valida \_**</dt> </dl> | Nessuna registrazione in corso.<br/>                       |
| <span id="WINBIO_I_MORE_DATA"></span><span id="winbio_i_more_data"></span><dl> <dt>**WINBIO \_ \_ più \_ dati**</dt> </dl>                         | Per completare il modello sono necessari altri esempi.<br/> |
| <span id="WINBIO_E_BAD_CAPTURE"></span><span id="winbio_e_bad_capture"></span><dl> <dt>**WINBIO \_ E \_ acquisizione non valida \_**</dt> </dl>                   | L'esempio più recente non è utilizzabile.<br/>               |



 

</dd> <dt>

**RejectDetail**
</dt> <dd>

Il motivo per cui l'esempio più recente è inutilizzabile, se il valore del membro **TemplateStatus** è **WINBIO \_ E \_ Bad \_ Capture**.

</dd> <dt>

**PercentComplete**
</dt> <dd>

Stima migliore dall'adattatore del motore per la percentuale del modello completo, come valore compreso tra 0 e 100.

</dd> <dt>

**Fattore**
</dt> <dd>

Tipo di unità biometrica per la quale questa struttura contiene informazioni sulle funzionalità e i requisiti di registrazione dell'adattatore del motore. Se, ad esempio, il valore del membro **Factor** è **WINBIO \_ , \_** la struttura di [**\_ informazioni del \_ motore \_ esteso WINBIO**](winbio-extended-engine-info.md) si applica a un lettore di impronte digitali e contiene le informazioni rilevanti nella struttura **specifico. Fingerprint** .

</dd> <dt>

**Sottofattore**
</dt> <dd>

Valore **del \_ \_ SOTTOtipo biometrico WINBIO** che fornisce informazioni aggiuntive sulla registrazione.

</dd> <dt>

**Specifica**
</dt> <dd>

Informazioni sullo stato di una registrazione in corso per un fattore biometrico specifico.

<dl> <dt>

**Null**
</dt> <dd>

Riservato. Deve essere zero.

</dd> <dt>

**FacialFeatures**
</dt> <dd>

Informazioni sullo stato di una registrazione in corso per le funzionalità facciali.

<dl> <dt>

**BoundingBox**
</dt> <dd>

Posizione all'interno del frame della fotocamera della faccia del singolo oggetto da registrare, in pixel. La dimensione del fotogramma della fotocamera determina il limite superiore per il numero di pixel per questa posizione. Ottenere la **proprietà \_ WINBIO \_ Extended \_ Sensor \_ info** per determinare la dimensione del fotogramma della fotocamera. Un client che utilizza il monitoraggio della presenza deve eseguire l'operazione di ridimensionamento per eseguire il mapping della posizione al frame della fotocamera.

</dd> <dt>

**Distanza**
</dt> <dd>

Distanza tra la posizione effettiva della faccia e la distanza focale ideale per la superficie. Questo valore è compreso tra-100 e 100. 0 indica la distanza ideale, i valori positivi indicano che la posizione effettiva della faccia è troppo distante e i valori negativi indicano che la posizione effettiva è troppo vicina.

</dd> </dl> </dd> <dt>

**Impronta digitale**
</dt> <dd>

Informazioni sullo stato di una registrazione in corso per i modelli di impronta digitale.

<dl> <dt>

**GeneralSamples**
</dt> <dd>

Numero totale di campioni necessari per creare un nuovo modello di impronta digitale.

</dd> <dt>

**Center**
</dt> <dd>

Il numero di campioni per il centro dell'impronta digitale necessario per creare un nuovo modello di impronta digitale.

</dd> <dt>

**TopEdge**
</dt> <dd>

Il numero di campioni per il bordo superiore dell'impronta digitale necessario per creare un nuovo modello di impronta digitale.

</dd> <dt>

**BottomEdge**
</dt> <dd>

Il numero di campioni per il bordo inferiore dell'impronta digitale necessario per creare un nuovo modello di impronta digitale.

</dd> <dt>

**LeftEdge**
</dt> <dd>

Il numero di campioni per il bordo sinistro dell'impronta digitale necessario per creare un nuovo modello di impronta digitale.

</dd> <dt>

**RightEdge**
</dt> <dd>

Il numero di campioni per il bordo destro dell'impronta digitale necessario per creare un nuovo modello di impronta digitale.

</dd> </dl> </dd> <dt>

**Iris**
</dt> <dd>

Informazioni sullo stato di una registrazione in corso per i modelli Iris.

<dl> <dt>

**EyeBoundingBox \_ 1**
</dt> <dd>

Posizione all'interno del frame della fotocamera di uno degli Iris del singolo oggetto da registrare, in pixel. Se il sistema di riconoscimento Iris sta monitorando solo un occhio, questa posizione è l'iride di quell'occhio. Se il sistema di riconoscimento Iris monitora entrambi gli occhi, ma solo un occhio si trova nel fotogramma della fotocamera, questa posizione è l'iride dell'occhio nel frame della fotocamera. Se il sistema di riconoscimento Iris monitora entrambi gli occhi ed entrambi gli occhi si trovano nel frame della fotocamera, questa posizione è probabilmente l'iride dell'occhio destro del singolo utente.

La dimensione del fotogramma della fotocamera determina il limite superiore per il numero di pixel per questa posizione. Ottenere la **proprietà \_ WINBIO \_ Extended \_ Sensor \_ info** per determinare la dimensione del fotogramma della fotocamera. Un client che utilizza il monitoraggio della presenza deve eseguire l'operazione di ridimensionamento per eseguire il mapping della posizione al frame della fotocamera.

</dd> <dt>

**EyeBoundingBox \_ 2**
</dt> <dd>

Posizione all'interno del frame della fotocamera di uno degli Iris del singolo oggetto da registrare, in pixel. Se il sistema di riconoscimento Iris sta monitorando solo un occhio o se solo un occhio è nel frame della fotocamera, questo valore è vuoto. Se il sistema di riconoscimento Iris monitora entrambi gli occhi ed entrambi gli occhi si trovano nel fotogramma della fotocamera, questa posizione è probabilmente di Iris dell'occhio sinistro del singolo utente.

La dimensione del fotogramma della fotocamera determina il limite superiore per il numero di pixel per questa posizione. Ottenere la **proprietà \_ WINBIO \_ Extended \_ Sensor \_ info** per determinare la dimensione del fotogramma della fotocamera. Un client che utilizza il monitoraggio della presenza deve eseguire l'operazione di ridimensionamento per eseguire il mapping della posizione al frame della fotocamera.

</dd> <dt>

**PupilCenter \_ 1**
</dt> <dd>

Posizione del centro di uno degli alunni del singolo oggetto da registrare. Se il sistema di riconoscimento Iris sta monitorando solo un occhio, questa posizione è al centro della pupilla di quell'occhio. Se il sistema di riconoscimento Iris monitora entrambi gli occhi, ma solo un occhio si trova nel fotogramma della fotocamera, questa posizione è al centro della pupilla dell'occhio nel frame della fotocamera. Se il sistema di riconoscimento Iris monitora entrambi gli occhi ed entrambi gli occhi si trovano nel fotogramma della fotocamera, questa posizione è probabilmente al centro della pupilla dell'occhio destro della persona.

</dd> <dt>

**PupilCenter \_ 2**
</dt> <dd>

Posizione del centro di uno degli alunni del singolo oggetto da registrare. Se il sistema di riconoscimento Iris sta monitorando solo un occhio o se solo un occhio è nel frame della fotocamera, questo valore è vuoto. Se il sistema di riconoscimento Iris monitora entrambi gli occhi ed entrambi gli occhi si trovano nel fotogramma della fotocamera, questa posizione è probabilmente al centro della pupilla dell'occhio sinistro del singolo utente.

</dd> <dt>

**Distanza**
</dt> <dd>

Distanza tra la posizione effettiva dell'iride e la distanza focale ideale per l'Iris. Questo valore è compreso tra-100 e 100. 0 indica la distanza ideale, i valori positivi indicano che la posizione effettiva dell'Iris è troppo distante e i valori negativi indicano che la posizione effettiva è troppo vicina.

</dd> </dl> </dd> <dt>

**Chiamata vocale**
</dt> <dd>

Informazioni sullo stato di una registrazione in corso per i modelli vocali.

<dl> <dt>

**Reserved**
</dt> <dd>

Riservato.

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                                                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2016\]<br/>                                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>WinBio \_ types. h (includere WinBio. h per le applicazioni client o WinBio \_ Adapters. h per gli adapter)</dt> </dl> |



 

 





