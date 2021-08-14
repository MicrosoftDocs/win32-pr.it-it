---
title: WINBIO_EXTENDED_ENROLLMENT_STATUS struttura (Winbio \_ types.h)
description: Contiene informazioni aggiuntive sullo stato di una registrazione in corso.
ms.assetid: 2FDDF4D3-6A3E-4DF5-ACA4-423F893C6F2B
keywords:
- WINBIO_EXTENDED_ENROLLMENT_STATUS struttura Windows'API Biometric Framework
- PWINBIO_EXTENDED_ENROLLMENT_STATUS puntatore alla struttura Windows'API Biometric Framework
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
ms.openlocfilehash: 16ab3736e3ad5b0bcf10bed1fb606d3e6283715a6b10c44dcb4923920597d5e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910446"
---
# <a name="winbio_extended_enrollment_status-structure"></a>Struttura DELLO STATO \_ DI \_ REGISTRAZIONE ESTESA \_ WINBIO

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

Stato della raccolta di esempio per il modello di registrazione. Per questo membro sono possibili i valori seguenti.



| Valore                                                                                                                                                                                                  | Significato                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <dt>**S \_ OK**</dt> </dl>                                                                     | La registrazione è pronta per essere salvata.<br/>                |
| <span id="WINBIO_E_INVALID_OPERATION"></span><span id="winbio_e_invalid_operation"></span><dl> <dt>**OPERAZIONE WINBIO \_ E \_ NON \_ VALIDA**</dt> </dl> | Nessuna registrazione in corso.<br/>                       |
| <span id="WINBIO_I_MORE_DATA"></span><span id="winbio_i_more_data"></span><dl> <dt>**ALTRI DATI DI WINBIO \_ I \_ \_**</dt> </dl>                         | Per completare il modello sono necessari altri esempi.<br/> |
| <span id="WINBIO_E_BAD_CAPTURE"></span><span id="winbio_e_bad_capture"></span><dl> <dt>**WINBIO \_ E \_ BAD \_ CAPTURE**</dt> </dl>                   | L'esempio più recente non è utilizzabile.<br/>               |



 

</dd> <dt>

**RejectDetail**
</dt> <dd>

Il motivo per cui l'esempio più recente è inutilizzabile, se il valore del membro **TemplateStatus** è **WINBIO \_ E BAD \_ \_ CAPTURE**.

</dd> <dt>

**PercentComplete**
</dt> <dd>

Stima migliore dell'adattatore motore per la percentuale di completamento del modello, come valore compreso tra 0 e 100.

</dd> <dt>

**Fattore**
</dt> <dd>

Tipo di unità biometrica per cui questa struttura contiene informazioni sulle funzionalità e sui requisiti di registrazione dell'adattatore motore. Ad esempio, se il valore del membro **Factor** è **WINBIO \_ TYPE \_ FINGERPRINT,** la struttura [**WINBIO \_ EXTENDED ENGINE \_ \_ INFO**](winbio-extended-engine-info.md) si applica a un lettore di impronta digitale e contiene le informazioni rilevanti nella **struttura Specifc.Fingerprint.**

</dd> <dt>

**Sottofactoring**
</dt> <dd>

Valore **\_ \_ SUBTYPE BIOMETRICO WINBIO** che fornisce informazioni aggiuntive sulla registrazione.

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

Informazioni sullo stato di una registrazione in corso per le caratteristiche facciali.

<dl> <dt>

**Boundingbox**
</dt> <dd>

Posizione all'interno del fotogramma della fotocamera del viso dell'utente da registrare, in pixel. Le dimensioni del fotogramma della fotocamera determinano il limite superiore per il numero di pixel per questa posizione. Ottenere la **proprietà WINBIO \_ PROPERTY EXTENDED SENSOR \_ \_ \_ INFO** per determinare le dimensioni del fotogramma della fotocamera. Un client che usa il monitoraggio della presenza deve eseguire l'operazione di ridimensionamento per eseguire il mapping della posizione al fotogramma della fotocamera.

</dd> <dt>

**Distanza**
</dt> <dd>

Distanza tra la posizione effettiva del viso e la distanza focale ideale per il viso. Questo valore è compreso tra -100 e 100. 0 indica la distanza ideale, i valori positivi indicano che la posizione effettiva del viso è troppo lontana e i valori negativi indicano che la posizione effettiva è troppo vicina.

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

Numero di esempi per il centro dell'impronta digitale necessaria per creare un nuovo modello di impronta digitale.

</dd> <dt>

**TopEdge**
</dt> <dd>

Numero di esempi per il bordo superiore dell'impronta digitale necessaria per creare un nuovo modello di impronta digitale.

</dd> <dt>

**BottomEdge**
</dt> <dd>

Numero di esempi per il bordo inferiore dell'impronta digitale necessaria per creare un nuovo modello di impronta digitale.

</dd> <dt>

**LeftEdge**
</dt> <dd>

Numero di esempi per il bordo sinistro dell'impronta digitale necessaria per creare un nuovo modello di impronta digitale.

</dd> <dt>

**RightEdge**
</dt> <dd>

Numero di esempi per il bordo destro dell'impronta digitale necessaria per creare un nuovo modello di impronta digitale.

</dd> </dl> </dd> <dt>

**Iris**
</dt> <dd>

Informazioni sullo stato di una registrazione in corso per i modelli iris.

<dl> <dt>

**EyeBoundingBox \_ 1**
</dt> <dd>

Posizione all'interno del fotogramma della fotocamera di una delle iris dell'utente da registrare, in pixel. Se il sistema di riconoscimento dell'iris monitora solo un occhio, questa posizione è dell'iris di quell'occhio. Se il sistema di riconoscimento dell'iris monitora entrambi gli occhi, ma nel frame della fotocamera è presente un solo occhio, questa posizione è dell'iris dell'occhio nel fotogramma della fotocamera. Se il sistema di riconoscimento dell'iris monitora entrambi gli occhi ed entrambi gli occhi sono nel frame della fotocamera, questa posizione è probabilmente dell'iris dell'occhio destro dell'individuo.

Le dimensioni del fotogramma della fotocamera determinano il limite superiore per il numero di pixel per questa posizione. Ottenere la **proprietà WINBIO \_ PROPERTY EXTENDED SENSOR \_ \_ \_ INFO** per determinare le dimensioni del fotogramma della fotocamera. Un client che usa il monitoraggio della presenza deve eseguire l'operazione di ridimensionamento per eseguire il mapping della posizione al fotogramma della fotocamera.

</dd> <dt>

**EyeBoundingBox \_ 2**
</dt> <dd>

Posizione all'interno del fotogramma della fotocamera di una delle iris dell'utente da registrare, in pixel. Se il sistema di riconoscimento dell'iris monitora solo un occhio o se nel fotogramma della fotocamera è presente un solo occhio, questo valore è vuoto. Se il sistema di riconoscimento dell'iris monitora entrambi gli occhi ed entrambi gli occhi sono nel frame della fotocamera, questa posizione è probabilmente dell'iris dell'occhio sinistro dell'individuo.

Le dimensioni del fotogramma della fotocamera determinano il limite superiore per il numero di pixel per questa posizione. Ottenere la **proprietà WINBIO \_ PROPERTY EXTENDED SENSOR \_ \_ \_ INFO** per determinare le dimensioni del fotogramma della fotocamera. Un client che usa il monitoraggio della presenza deve eseguire l'operazione di ridimensionamento per eseguire il mapping della posizione al fotogramma della fotocamera.

</dd> <dt>

**\_Epicentro 1**
</dt> <dd>

Posizione del centro di uno degli studenti della persona da registrare. Se il sistema di riconoscimento dell'iris monitora solo un occhio, questa posizione è al centro dell'area dell'occhio. Se il sistema di riconoscimento dell'iris monitora entrambi gli occhi, ma nella cornice della fotocamera è presente un solo occhio, questa posizione è del centro dell'oculare nel fotogramma della fotocamera. Se il sistema di riconoscimento dell'iris monitora entrambi gli occhi ed entrambi gli occhi sono nel frame della fotocamera, questa posizione è probabilmente del centro dell'occhio destro dell'individuo.

</dd> <dt>

**\_Epicentro 2**
</dt> <dd>

Posizione del centro di uno degli studenti della persona da registrare. Se il sistema di riconoscimento dell'iris monitora solo un occhio o se nel fotogramma della fotocamera è presente un solo occhio, questo valore è vuoto. Se il sistema di riconoscimento dell'iris monitora entrambi gli occhi e entrambi gli occhi sono nel frame della fotocamera, questa posizione è probabilmente del centro dell'occhio sinistro dell'individuo.

</dd> <dt>

**Distanza**
</dt> <dd>

Distanza tra la posizione effettiva dell'iris e la distanza focale ideale per l'iris. Questo valore è compreso tra -100 e 100. 0 indica la distanza ideale, i valori positivi indicano che la posizione effettiva dell'iris è troppo lontana e i valori negativi indicano che la posizione effettiva è troppo vicina.

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
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                                                                                              |
| Server minimo supportato<br/> | \[Windows Server 2016 solo app desktop\]<br/>                                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Winbio \_ types.h (includere Winbio.h per le applicazioni client o Winbio \_ adapters.h per gli adapter)</dt> </dl> |



 

 





