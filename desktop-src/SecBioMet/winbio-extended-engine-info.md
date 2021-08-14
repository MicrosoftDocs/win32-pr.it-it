---
title: WINBIO_EXTENDED_ENGINE_INFO struttura (Winbio \_ types.h)
description: Contiene informazioni sulle funzionalità e sui requisiti di registrazione dell'adattatore motore per un'unità biometrica.
ms.assetid: 83586E04-24CA-4A39-836F-C80DB1508C71
keywords:
- WINBIO_EXTENDED_ENGINE_INFO struttura Windows'API Biometric Framework
- PWINBIO_EXTENDED_ENGINE_INFO puntatore alla struttura Windows'API Biometric Framework
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
ms.openlocfilehash: df59b10400729150a13f2a8a5476c46507867777f71641a01ea0c08e064b4c40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910517"
---
# <a name="winbio_extended_engine_info-structure"></a>Struttura DELLE INFORMAZIONI \_ SUL \_ MOTORE \_ ESTESO WINBIO

Contiene informazioni sulle funzionalità e sui requisiti di registrazione dell'adattatore motore per un'unità biometrica.

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

Tipo di unità biometrica per cui questa struttura contiene informazioni sulle funzionalità e sui requisiti di registrazione dell'adattatore motore. Ad esempio, se il valore del membro **Factor** è **WINBIO \_ TYPE \_ FINGERPRINT,** la struttura **WINBIO \_ EXTENDED ENGINE \_ \_ INFO** si applica a un lettore di impronta digitale e contiene le informazioni rilevanti nella **struttura Specifc.Fingerprint.**

</dd> <dt>

**Specifica**
</dt> <dd>

Informazioni sulle funzionalità e sui requisiti di registrazione dell'adattatore motore per un'unità biometrica correlata a un fattore biometrico specifico.

<dl> <dt>

**Null**
</dt> <dd>

Riservato. Deve essere zero.

</dd> <dt>

**Funzionalità del viso**
</dt> <dd>

Informazioni sulle funzionalità e i requisiti di registrazione dell'adattatore motore per un'unità biometrica correlata alle caratteristiche facciali.

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

Informazioni sulle funzionalità e i requisiti di registrazione dell'adattatore motore per un'unità biometrica correlata ai modelli di impronta digitale.

<dl> <dt>

**Capabilities**
</dt> <dd>

Riservato. Deve essere zero.

</dd> <dt>

**EnrollmentRequirements**
</dt> <dd>

Numero di esempi buoni necessari per creare un nuovo modello di impronta digitale.

<dl> <dt>

**GeneralSamples**
</dt> <dd>

Numero totale di campioni buoni necessari per creare un nuovo modello di impronta digitale.

</dd> <dt>

**Center**
</dt> <dd>

Numero di campioni per il centro dell'impronta digitale necessari per creare un nuovo modello di impronta digitale.

</dd> <dt>

**TopEdge**
</dt> <dd>

Numero di campioni per il bordo superiore dell'impronta digitale necessari per creare un nuovo modello di impronta digitale.

</dd> <dt>

**BottomEdge**
</dt> <dd>

Numero di campioni per il bordo inferiore dell'impronta digitale necessari per creare un nuovo modello di impronta digitale.

</dd> <dt>

**LeftEdge**
</dt> <dd>

Numero di campioni per il bordo sinistro dell'impronta digitale necessari per creare un nuovo modello di impronta digitale.

</dd> <dt>

**RightEdge**
</dt> <dd>

Numero di campioni per il bordo destro dell'impronta digitale necessari per creare un nuovo modello di impronta digitale.

</dd> </dl> </dd> </dl> </dd> <dt>

**Iris**
</dt> <dd>

Informazioni sulle funzionalità e i requisiti di registrazione dell'adattatore motore per un'unità biometrica correlata ai modelli iris.

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

Informazioni sulle funzionalità e sui requisiti di registrazione dell'adattatore motore per un'unità biometrica correlata ai modelli vocali.

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
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                                                                                              |
| Server minimo supportato<br/> | \[Windows Server 2016 solo app desktop\]<br/>                                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Winbio \_ types.h (includere Winbio.h per le applicazioni client o Winbio \_ adapters.h per gli adapter)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Costanti CAPABILITY WINBIO \_**](winbio-capability-constants.md)
</dt> <dt>

[**Costanti DI TIPO \_ BIOMETRICO WINBIO \_**](winbio-biometric-type-constants.md)
</dt> </dl>

 

 





