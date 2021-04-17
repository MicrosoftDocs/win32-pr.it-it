---
title: Unione WINBIO_PRESENCE_PROPERTIES ( \_ tipi WINBIO. h)
description: Contiene i valori biometrici utilizzati dal Windows Biometric Framework per determinare la presenza di un singolo utente.
ms.assetid: 596CAA7F-35D2-442A-8041-BA1010DF5BAD
keywords:
- API Windows Biometric Framework di WINBIO_PRESENCE_PROPERTIES Union
- API Windows Biometric Framework PWINBIO_PRESENCE_PROPERTIES puntatore Unione
topic_type:
- apiref
api_name:
- WINBIO_PRESENCE_PROPERTIES
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0568008b870953c34205706acc90cb22a2c0e92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475664"
---
# <a name="winbio_presence_properties-union"></a>\_ \_ Unione proprietà presenza WINBIO

Contiene i valori biometrici utilizzati dal Windows Biometric Framework per determinare la presenza di un singolo utente.

## <a name="syntax"></a>Sintassi


```C++
typedef union _WINBIO_PRESENCE_PROPERTIES {
  struct {
    RECT BoundingBox;
    LONG Distance;
  } FacialFeatures;
  struct {
    RECT  EyeBoundingBox_1;
    RECT  EyeBoundingBox_2;
    POINT PupilCenter_1;
    POINT PupilCenter_2;
    LONG  Distance;
  } Iris;
} WINBIO_PRESENCE_PROPERTIES, *PWINBIO_PRESENCE_PROPERTIES;
```



## <a name="members"></a>Members

<dl> <dt>

**FacialFeatures**
</dt> <dd>

Valori per la posizione delle funzionalità facciali usate dal Windows Biometric Framework per determinare la presenza di un singolo utente.

<dl> <dt>

**BoundingBox**
</dt> <dd>

Posizione all'interno del frame della fotocamera della faccia del singolo, in pixel. La dimensione del fotogramma della fotocamera determina il limite superiore per il numero di pixel per questa posizione. Ottenere la **proprietà \_ WINBIO \_ Extended \_ Sensor \_ info** per determinare la dimensione del fotogramma della fotocamera. Un client che utilizza il monitoraggio della presenza deve eseguire l'operazione di ridimensionamento per eseguire il mapping della posizione al frame della fotocamera.

</dd> <dt>

**Distanza**
</dt> <dd>

Distanza tra la posizione effettiva della faccia e la distanza focale ideale per la superficie. Questo valore è compreso tra-100 e 100. 0 indica la distanza ideale, i valori positivi indicano che la posizione effettiva della faccia è troppo distante e i valori negativi indicano che la posizione effettiva è troppo vicina.

</dd> </dl> </dd> <dt>

**Iris**
</dt> <dd>

Valori per la posizione di Iris utilizzata dall'Windows Biometric Framework per determinare la presenza di un singolo utente.

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

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                                                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2016\]<br/>                                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>WinBio \_ types. h (includere WinBio. h per le applicazioni client o WinBio \_ Adapters. h per gli adapter)</dt> </dl> |



 

 





