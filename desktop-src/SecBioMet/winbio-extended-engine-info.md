---
title: Struttura WINBIO_EXTENDED_ENGINE_INFO ( \_ tipi WINBIO. h)
description: Contiene informazioni sulle funzionalità e i requisiti di registrazione della scheda del motore per un'unità biometrica.
ms.assetid: 83586E04-24CA-4A39-836F-C80DB1508C71
keywords:
- Struttura di WINBIO_EXTENDED_ENGINE_INFO Windows Biometric Framework API
- API Windows Biometric Framework puntatore alla struttura PWINBIO_EXTENDED_ENGINE_INFO
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_ENGINE_INFO
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 829bd0423ab6add41b17f59d308aea850c5b2f42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874546"
---
# <a name="winbio_extended_engine_info-structure"></a>\_ \_ Struttura informazioni motore esteso WINBIO \_

Contiene informazioni sulle funzionalità e i requisiti di registrazione della scheda del motore per un'unità biometrica.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _WINBIO_EXTENDED_ENGINE_INFO {
  WINBIO_CAPABILITIES   GenericEngineCapabilities;
  WINBIO_BIOMETRIC_TYPE Factor;
  union {
    ULONG32 Null;
    struct {
      WINBIO_CAPABILITIES Capabilities;
      struct {
        ULONG32 Null;
      } EnrollmentRequirements;
    } FacialFeatures;
    struct {
      WINBIO_CAPABILITIES Capabilities;
      struct {
        ULONG GeneralSamples;
        ULONG Center;
        ULONG TopEdge;
        ULONG BottomEdge;
        ULONG LeftEdge;
        ULONG RightEdge;
      } EnrollmentRequirements;
    } Fingerprint;
    struct {
      WINBIO_CAPABILITIES Capabilities;
      struct {
        ULONG32 Null;
      } EnrollmentRequirements;
    } Iris;
    struct {
      WINBIO_CAPABILITIES Capabilities;
      struct {
        ULONG32 Null;
      } EnrollmentRequirements;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_ENGINE_INFO, *PWINBIO_EXTENDED_ENGINE_INFO;
```



## <a name="members"></a>Members

<dl> <dt>

**GenericEngineCapabilities**
</dt> <dd>

Funzionalità generiche del componente motore connesso a un'unità biometrica specifica.

</dd> <dt>

**Fattore**
</dt> <dd>

Tipo di unità biometrica per la quale questa struttura contiene informazioni sulle funzionalità e i requisiti di registrazione dell'adattatore del motore. Se, ad esempio, il valore del membro **Factor** è **WINBIO \_ , \_** la struttura di **\_ informazioni del \_ motore \_ esteso WINBIO** si applica a un lettore di impronte digitali e contiene le informazioni rilevanti nella struttura **specifico. Fingerprint** .

</dd> <dt>

**Specifica**
</dt> <dd>

Informazioni sulle funzionalità e i requisiti di registrazione dell'adattatore del motore per un'unità biometrica correlata a un fattore biometrico specifico.

<dl> <dt>

**Null**
</dt> <dd>

Riservato. Deve essere zero.

</dd> <dt>

**FacialFeatures**
</dt> <dd>

Informazioni sulle funzionalità e i requisiti di registrazione dell'adattatore del motore per un'unità biometrica correlata alle funzionalità facciali.

<dl> <dt>

**Capabilities**
</dt> <dd>

Riservato. Deve essere zero.

</dd> <dt>

**EnrollmentRequirements**
</dt> <dd> <dl> <dt>

**Null**
</dt> <dd>

Riservato. Deve essere zero.

</dd> </dl> </dd> </dl> </dd> <dt>

**Impronta digitale**
</dt> <dd>

Informazioni sulle funzionalità e i requisiti di registrazione dell'adattatore del motore per un'unità biometrica relativa ai modelli di impronta digitale.

<dl> <dt>

**Capabilities**
</dt> <dd>

Riservato. Deve essere zero.

</dd> <dt>

**EnrollmentRequirements**
</dt> <dd>

Il numero di campioni validi necessari per creare un nuovo modello di impronta digitale.

<dl> <dt>

**GeneralSamples**
</dt> <dd>

Numero totale di campioni validi necessari per creare un nuovo modello di impronta digitale.

</dd> <dt>

**Center**
</dt> <dd>

Il numero di campioni validi per il centro dell'impronta digitale necessario per creare un nuovo modello di impronta digitale.

</dd> <dt>

**TopEdge**
</dt> <dd>

Il numero di campioni validi per il bordo superiore dell'impronta digitale necessario per creare un nuovo modello di impronta digitale.

</dd> <dt>

**BottomEdge**
</dt> <dd>

Il numero di campioni validi per il bordo inferiore dell'impronta digitale necessario per creare un nuovo modello di impronta digitale.

</dd> <dt>

**LeftEdge**
</dt> <dd>

Il numero di campioni validi per il bordo sinistro dell'impronta digitale necessaria per creare un nuovo modello di impronta digitale.

</dd> <dt>

**RightEdge**
</dt> <dd>

Il numero di campioni validi per il bordo destro dell'impronta digitale necessaria per creare un nuovo modello di impronta digitale.

</dd> </dl> </dd> </dl> </dd> <dt>

**Iris**
</dt> <dd>

Informazioni sulle funzionalità e i requisiti di registrazione dell'adattatore del motore per un'unità biometrica relativa ai modelli Iris.

<dl> <dt>

**Capabilities**
</dt> <dd>

Riservato. Deve essere zero.

</dd> <dt>

**EnrollmentRequirements**
</dt> <dd> <dl> <dt>

**Null**
</dt> <dd>

Riservato. Deve essere zero.

</dd> </dl> </dd> </dl> </dd> <dt>

**Chiamata vocale**
</dt> <dd>

Informazioni sulle funzionalità e sui requisiti di registrazione dell'adattatore del motore per un'unità biometrica relativa ai modelli vocali.

<dl> <dt>

**Capabilities**
</dt> <dd>

Riservato. Deve essere zero.

</dd> <dt>

**EnrollmentRequirements**
</dt> <dd> <dl> <dt>

**Null**
</dt> <dd>

Riservato. Deve essere zero.

</dd> </dl> </dd> </dl> </dd> </dl> </dd> </dl>

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
</dt> </dl>

 

 





