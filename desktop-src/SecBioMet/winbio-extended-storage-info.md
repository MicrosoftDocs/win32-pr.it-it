---
title: WINBIO_EXTENDED_STORAGE_INFO struttura (Winbio \_ types.h)
description: Contiene informazioni sulle funzionalità e sui requisiti di registrazione dell'adattatore di archiviazione per un'unità biometrica.
ms.assetid: 7A648610-E947-4967-A9AF-C8A9C0B81D92
keywords:
- WINBIO_EXTENDED_STORAGE_INFO struttura Windows'API Biometric Framework
- PWINBIO_EXTENDED_STORAGE_INFO puntatore alla struttura Windows'API Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_STORAGE_INFO
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e8a9f133baf77a77d3db33001e996accc9574f86ad708037900a5db7c0c5e8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910382"
---
# <a name="winbio_extended_storage_info-structure"></a>Struttura DELLE INFORMAZIONI \_ \_ \_ SULL'ARCHIVIAZIONE ESTESA WINBIO

Contiene informazioni sulle funzionalità e sui requisiti di registrazione dell'adattatore di archiviazione per un'unità biometrica.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _WINBIO_EXTENDED_STORAGE_INFO {
  WINBIO_CAPABILITIES   GenericStorageCapabilities;
  WINBIO_BIOMETRIC_TYPE Factor;
  union {
    ULONG32 Null;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } FacialFeatures;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } Fingerprint;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } Iris;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_STORAGE_INFO, *PWINBIO_EXTENDED_STORAGE_INFO;
```



## <a name="members"></a>Members

<dl> <dt>

**GenericStorageCapabilities**
</dt> <dd>

Funzionalità generiche del componente di archiviazione connesso a un'unità biometrica specifica.

</dd> <dt>

**Fattore**
</dt> <dd>

Tipo di unità biometrica per cui questa struttura contiene informazioni sulle funzionalità e sui requisiti di registrazione della scheda di archiviazione. Ad esempio, se il valore del membro **Factor** è **WINBIO \_ TYPE \_ FINGERPRINT,** la struttura **WINBIO \_ EXTENDED STORAGE \_ \_ INFO** si applica a un lettore di impronta digitale e contiene le informazioni rilevanti nella **struttura Specifc.Fingerprint.**

</dd> <dt>

**Specifica**
</dt> <dd>

Informazioni sulle funzionalità e sui requisiti di registrazione dell'adattatore di archiviazione per un'unità biometrica correlata a un fattore biometrico specifico.

<dl> <dt>

**Null**
</dt> <dd>

Riservato. Deve essere zero.

</dd> <dt>

**Funzionalità del viso**
</dt> <dd>

Informazioni sulle funzionalità e i requisiti di registrazione dell'adattatore di archiviazione per un'unità biometrica correlata alle caratteristiche facciali.

<dl> <dt>

**Capabilities**
</dt> <dd>

Funzionalità di riconoscimento facciale del componente di archiviazione connesso a un'unità biometrica specifica.

</dd> </dl> </dd> <dt>

**Impronta digitale**
</dt> <dd>

Informazioni sulle funzionalità e sui requisiti di registrazione dell'adattatore di archiviazione per un'unità biometrica correlata ai modelli di impronta digitale.

<dl> <dt>

**Capabilities**
</dt> <dd>

Funzionalità di riconoscimento delle impronte digitali del componente di archiviazione connesso a un'unità biometrica specifica

</dd> </dl> </dd> <dt>

**Iris**
</dt> <dd>

Informazioni sulle funzionalità e sui requisiti di registrazione dell'adattatore di archiviazione per un'unità biometrica correlata ai modelli iris.

<dl> <dt>

**Capabilities**
</dt> <dd>

Funzionalità di riconoscimento dell'iris del componente di archiviazione connesso a un'unità biometrica specifica

</dd> </dl> </dd> <dt>

**Chiamata vocale**
</dt> <dd>

Informazioni sulle funzionalità e sui requisiti di registrazione dell'adattatore di archiviazione per un'unità biometrica correlata ai modelli vocali.

<dl> <dt>

**Capabilities**
</dt> <dd>

Funzionalità di riconoscimento vocale del componente di archiviazione connesso a un'unità biometrica specifica

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                                                                                              |
| Server minimo supportato<br/> | \[Windows Server 2016 solo app desktop\]<br/>                                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Winbio \_ types.h (includere Winbio.h per le applicazioni client o Winbio \_ adapters.h per gli adapter)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Costanti DI TIPO \_ BIOMETRICO WINBIO \_**](winbio-biometric-type-constants.md)
</dt> <dt>

[**Costanti CAPABILITY WINBIO \_**](winbio-capability-constants.md)
</dt> </dl>

 

 





