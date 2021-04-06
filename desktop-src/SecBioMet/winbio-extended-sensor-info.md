---
title: Struttura WINBIO_EXTENDED_SENSOR_INFO ( \_ tipi WINBIO. h)
description: Contiene informazioni sulle funzionalità e i requisiti di registrazione della scheda sensore per un'unità biometrica.
ms.assetid: 37D8BC57-F68D-487A-98B0-94D62CC091C2
keywords:
- Struttura di WINBIO_EXTENDED_SENSOR_INFO Windows Biometric Framework API
- API Windows Biometric Framework puntatore alla struttura PWINBIO_EXTENDED_SENSOR_INFO
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
ms.openlocfilehash: c535ef56eeade897aac3c1d0503477da406935b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963866"
---
# <a name="winbio_extended_sensor_info-structure"></a>\_ \_ Struttura info sensore esteso WINBIO \_

Contiene informazioni sulle funzionalità e i requisiti di registrazione della scheda sensore per un'unità biometrica.

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

Tipo di unità biometrica per la quale questa struttura contiene informazioni sulle funzionalità e i requisiti di registrazione della scheda del sensore. Se, ad esempio, il valore del membro **Factor** è **WINBIO \_ , \_** la struttura di **\_ informazioni sul \_ sensore \_ esteso WINBIO** si applica a un lettore di impronte digitali e contiene le informazioni rilevanti nella struttura **specifico. Fingerprint** .

</dd> <dt>

**Specifica**
</dt> <dd>

Informazioni sulle funzionalità e i requisiti di registrazione della scheda sensore per un'unità biometrica correlata a un fattore biometrico specifico.

<dl> <dt>

**Null**
</dt> <dd>

Riservato. Deve essere zero.

</dd> <dt>

**FacialFeatures**
</dt> <dd>

Informazioni sulle funzionalità e i requisiti di registrazione della scheda sensore per un'unità biometrica correlata alle funzionalità facciali.

<dl> <dt>

**FrameSize**
</dt> <dd>

Dimensioni del fotogramma della fotocamera, indicate come lunghezza e larghezza in pixel per i membri **destro** e **inferiore** della struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) . Il punto (0, 0) rappresenta l'angolo superiore sinistro del frame.

</dd> <dt>

**FrameOffset**
</dt> <dd>

Offset del fotogramma della fotocamera per la faccia dalla videocamera, in pixel. Il valore (0, 0) indica che il fotogramma della fotocamera per la superficie e la videocamera video si sovrappongono completamente.

</dd> <dt>

**MandatoryOrientation**
</dt> <dd>

Orientamento preferito per la fotocamera.

</dd> </dl> </dd> <dt>

**Impronta digitale**
</dt> <dd>

Informazioni sulle funzionalità e i requisiti di registrazione della scheda sensore per un'unità biometrica correlata ai modelli di impronta digitale.

<dl> <dt>

**Reserved**
</dt> <dd>

Riservato.

</dd> </dl> </dd> <dt>

**Iris**
</dt> <dd>

Informazioni sulle funzionalità e i requisiti di registrazione della scheda sensore per un'unità biometrica relativa ai modelli Iris.

<dl> <dt>

**FrameSize**
</dt> <dd>

Dimensioni del fotogramma della fotocamera, indicate come lunghezza e larghezza in pixel per i membri **destro** e **inferiore** della struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) . Il punto (0, 0) rappresenta l'angolo superiore sinistro del frame.

</dd> <dt>

**FrameOffset**
</dt> <dd>

Offset del fotogramma della fotocamera per l'iride dalla videocamera video, espresso in pixel. Il valore (0, 0) indica che il fotogramma della fotocamera per l'iride e la videocamera video si sovrappongono completamente.

</dd> <dt>

**MandatoryOrientation**
</dt> <dd>

Orientamento preferito per la fotocamera.

</dd> </dl> </dd> <dt>

**Chiamata vocale**
</dt> <dd>

Informazioni sulle funzionalità e i requisiti di registrazione della scheda sensore per un'unità biometrica relativa ai modelli vocali.

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



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Costanti della funzionalità WINBIO**](winbio-capability-constants.md)
</dt> <dt>

[**\_ \_ Costanti di tipo biometrico WINBIO**](winbio-biometric-type-constants.md)
</dt> <dt>

[**\_Costanti di orientamento WINBIO**](winbio-orientation-constants.md)
</dt> </dl>

 

