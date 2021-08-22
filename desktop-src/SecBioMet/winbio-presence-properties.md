---
title: WINBIO_PRESENCE_PROPERTIES union (Winbio \_ types.h)
description: Contiene i valori biometrici usati dal Windows Biometric Framework per determinare che una persona era presente.
ms.assetid: 596CAA7F-35D2-442A-8041-BA1010DF5BAD
keywords:
- WINBIO_PRESENCE_PROPERTIES'Windows API Biometric Framework
- PWINBIO_PRESENCE_PROPERTIES puntatore di unione Windows'API Biometric Framework
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
ms.openlocfilehash: 6a3964883f5dcd5b00c6f3eb6929c9deec99e58db014d18e51a192180a4d11f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909656"
---
# <a name="winbio_presence_properties-union"></a>Unione delle PROPRIETÀ DI PRESENZA WINBIO \_ \_

Contiene i valori biometrici usati dal Windows Biometric Framework per determinare che una persona era presente.

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

Valori per la posizione delle caratteristiche facciali usate dal Windows Biometric Framework per determinare che una persona era presente.

<dl> <dt>

**Boundingbox**
</dt> <dd>

Posizione all'interno della cornice della fotocamera del viso dell'utente, in pixel. Le dimensioni del fotogramma della fotocamera determinano il limite superiore per il numero di pixel per questa posizione. Ottenere la **proprietà WINBIO \_ PROPERTY EXTENDED SENSOR \_ \_ \_ INFO** per determinare le dimensioni del fotogramma della fotocamera. Un client che usa il monitoraggio della presenza deve eseguire l'operazione di ridimensionamento per eseguire il mapping della posizione al fotogramma della fotocamera.

</dd> <dt>

**Distanza**
</dt> <dd>

Distanza tra la posizione effettiva del viso e la distanza focale ideale per il viso. Questo valore è compreso tra -100 e 100. 0 indica la distanza ideale, i valori positivi indicano che la posizione effettiva del viso è troppo lontana e i valori negativi indicano che la posizione effettiva è troppo vicina.

</dd> </dl> </dd> <dt>

**Iris**
</dt> <dd>

Valori per la posizione dell'iris usati Windows Biometric Framework per determinare che una persona era presente.

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

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                                                                                              |
| Server minimo supportato<br/> | \[Windows Server 2016 solo app desktop\]<br/>                                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Winbio \_ types.h (includere Winbio.h per le applicazioni client o Adapters.h Winbio \_ per gli adapter)</dt> </dl> |



 

 





