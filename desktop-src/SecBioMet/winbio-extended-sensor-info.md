---
title: WINBIO_EXTENDED_SENSOR_INFO struttura (Winbio \_ types.h)
description: Contiene informazioni sulle funzionalità e sui requisiti di registrazione dell'adattatore del sensore per un'unità biometrica.
ms.assetid: 37D8BC57-F68D-487A-98B0-94D62CC091C2
keywords:
- WINBIO_EXTENDED_SENSOR_INFO struttura Windows'API Biometric Framework
- PWINBIO_EXTENDED_SENSOR_INFO puntatore alla struttura Windows'API Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_SENSOR_INFO
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd8c323b4f4e3847c399e314da22048f658fb68c3b07ecf82f71ce0ed327c368
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910419"
---
# <a name="winbio_extended_sensor_info-structure"></a>Struttura WINBIO \_ EXTENDED \_ SENSOR \_ INFO

Contiene informazioni sulle funzionalità e sui requisiti di registrazione dell'adattatore del sensore per un'unità biometrica.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _WINBIO_EXTENDED_SENSOR_INFO {
  WINBIO_CAPABILITIES   GenericSensorCapabilities;
  WINBIO_BIOMETRIC_TYPE Factor;
  union {
    ULONG32 Null;
    struct {
      RECT               FrameSize;
      POINT              FrameOffset;
      WINBIO_ORIENTATION MandatoryOrientation;
    } FacialFeatures;
    struct {
      ULONG32 Reserved;
    } Fingerprint;
    struct {
      RECT               FrameSize;
      POINT              FrameOffset;
      WINBIO_ORIENTATION MandatoryOrientation;
    } Iris;
    struct {
      ULONG32 Reserved;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_SENSOR_INFO, *PWINBIO_EXTENDED_SENSOR_INFO;
```



## <a name="members"></a>Members

<dl> <dt>

**GenericSensorCapabilities**
</dt> <dd>

Funzionalità generiche del componente sensore connesso a un'unità biometrica specifica.

</dd> <dt>

**Fattore**
</dt> <dd>

Tipo di unità biometrica per cui questa struttura contiene informazioni sulle funzionalità e sui requisiti di registrazione dell'adattatore del sensore. Ad esempio, se il valore del membro **Factor** è **WINBIO \_ TYPE \_ FINGERPRINT,** la struttura **WINBIO \_ EXTENDED SENSOR \_ \_ INFO** si applica a un lettore di impronta digitale e contiene le informazioni rilevanti nella **struttura Specifc.Fingerprint.**

</dd> <dt>

**Specifica**
</dt> <dd>

Informazioni sulle funzionalità e sui requisiti di registrazione dell'adattatore sensore per un'unità biometrica correlata a un fattore biometrico specifico.

<dl> <dt>

**Null**
</dt> <dd>

Riservato. Deve essere zero.

</dd> <dt>

**FacialFeatures**
</dt> <dd>

Informazioni sulle funzionalità e sui requisiti di registrazione dell'adattatore sensore per un'unità biometrica correlata alle caratteristiche facciali.

<dl> <dt>

**FrameSize**
</dt> <dd>

Dimensioni del frame della fotocamera, indicate come lunghezza e  larghezza in pixel dai membri destro **e** inferiore della struttura [**RECT.**](/previous-versions//dd162897(v=vs.85)) Il punto (0, 0) rappresenta l'angolo superiore sinistro del frame.

</dd> <dt>

**FrameOffset**
</dt> <dd>

Offset del fotogramma della fotocamera per il viso dalla videocamera, in pixel. Il valore (0, 0) indica che il fotogramma della fotocamera per il viso e la videocamera si sovrappongono completamente.

</dd> <dt>

**MandatoryOrientation**
</dt> <dd>

Orientamento preferito per la fotocamera.

</dd> </dl> </dd> <dt>

**Impronta digitale**
</dt> <dd>

Informazioni sulle funzionalità e sui requisiti di registrazione dell'adattatore sensore per un'unità biometrica correlata ai modelli di impronta digitale.

<dl> <dt>

**Reserved**
</dt> <dd>

Riservato.

</dd> </dl> </dd> <dt>

**Iris**
</dt> <dd>

Informazioni sulle funzionalità e sui requisiti di registrazione dell'adattatore sensore per un'unità biometrica correlata ai modelli iris.

<dl> <dt>

**FrameSize**
</dt> <dd>

Dimensioni del frame della fotocamera, indicate come lunghezza e  larghezza in pixel dai membri destro **e** inferiore della struttura [**RECT.**](/previous-versions//dd162897(v=vs.85)) Il punto (0, 0) rappresenta l'angolo superiore sinistro del frame.

</dd> <dt>

**FrameOffset**
</dt> <dd>

Offset del fotogramma della fotocamera per l'iris dalla videocamera, in pixel. Il valore (0, 0) indica che il fotogramma della fotocamera per l'iris e la videocamera si sovrappone completamente.

</dd> <dt>

**MandatoryOrientation**
</dt> <dd>

Orientamento preferito per la fotocamera.

</dd> </dl> </dd> <dt>

**Chiamata vocale**
</dt> <dd>

Informazioni sulle funzionalità e sui requisiti di registrazione dell'adattatore sensore per un'unità biometrica correlata ai modelli vocali.

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
| Intestazione<br/>                   | <dl> <dt>Winbio \_ types.h (includere Winbio.h per le applicazioni client o Adapters.h Winbio \_ per gli adapter)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Costanti DI \_ WINBIO CAPABILITY**](winbio-capability-constants.md)
</dt> <dt>

[**Costanti DI TIPO \_ BIOMETRICO WINBIO \_**](winbio-biometric-type-constants.md)
</dt> <dt>

[**Costanti \_ DI ORIENTAMENTO WINBIO**](winbio-orientation-constants.md)
</dt> </dl>

 

