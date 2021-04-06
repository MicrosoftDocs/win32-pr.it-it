---
title: Struttura WINBIO_EXTENDED_STORAGE_INFO ( \_ tipi WINBIO. h)
description: Contiene informazioni sulle funzionalità e i requisiti di registrazione dell'adattatore di archiviazione per un'unità biometrica.
ms.assetid: 7A648610-E947-4967-A9AF-C8A9C0B81D92
keywords:
- Struttura di WINBIO_EXTENDED_STORAGE_INFO Windows Biometric Framework API
- API Windows Biometric Framework puntatore alla struttura PWINBIO_EXTENDED_STORAGE_INFO
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
ms.openlocfilehash: 8ac2559717a2040cfb617e85e0a51495be1b5987
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963865"
---
# <a name="winbio_extended_storage_info-structure"></a>\_Struttura delle \_ informazioni di archiviazione estesa WINBIO \_

Contiene informazioni sulle funzionalità e i requisiti di registrazione dell'adattatore di archiviazione per un'unità biometrica.

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

Tipo di unità biometrica per la quale questa struttura contiene informazioni sulle funzionalità e i requisiti di registrazione dell'adattatore di archiviazione. Se, ad esempio, il valore del membro **Factor** è **WINBIO \_ , \_** la struttura delle **\_ informazioni di \_ archiviazione \_ estesa WINBIO** si applica a un lettore di impronte digitali e contiene le informazioni rilevanti nella struttura **specifico. Fingerprint** .

</dd> <dt>

**Specifica**
</dt> <dd>

Informazioni sulle funzionalità e i requisiti di registrazione dell'adattatore di archiviazione per un'unità biometrica correlata a un fattore biometrico specifico.

<dl> <dt>

**Null**
</dt> <dd>

Riservato. Deve essere zero.

</dd> <dt>

**FacialFeatures**
</dt> <dd>

Informazioni sulle funzionalità e i requisiti di registrazione dell'adattatore di archiviazione per un'unità biometrica correlata alle funzionalità facciali.

<dl> <dt>

**Capabilities**
</dt> <dd>

Funzionalità di riconoscimento facciali del componente di archiviazione connesso a un'unità biometrica specifica.

</dd> </dl> </dd> <dt>

**Impronta digitale**
</dt> <dd>

Informazioni sulle funzionalità e i requisiti di registrazione dell'adattatore di archiviazione per un'unità biometrica relativa ai modelli di impronta digitale.

<dl> <dt>

**Capabilities**
</dt> <dd>

Funzionalità di riconoscimento delle impronte digitali del componente di archiviazione connesso a un'unità biometrica specifica

</dd> </dl> </dd> <dt>

**Iris**
</dt> <dd>

Informazioni sulle funzionalità e i requisiti di registrazione dell'adattatore di archiviazione per un'unità biometrica relativa ai modelli Iris.

<dl> <dt>

**Capabilities**
</dt> <dd>

Funzionalità di riconoscimento Iris del componente di archiviazione connesso a un'unità biometrica specifica

</dd> </dl> </dd> <dt>

**Chiamata vocale**
</dt> <dd>

Informazioni sulle funzionalità e i requisiti di registrazione dell'adattatore di archiviazione per un'unità biometrica relativa ai modelli vocali.

<dl> <dt>

**Capabilities**
</dt> <dd>

Funzionalità di riconoscimento vocale del componente di archiviazione connesso a un'unità biometrica specifica

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                                                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2016\]<br/>                                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>WinBio \_ types. h (includere WinBio. h per le applicazioni client o WinBio \_ Adapters. h per gli adapter)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_ \_ Costanti di tipo biometrico WINBIO**](winbio-biometric-type-constants.md)
</dt> <dt>

[**\_Costanti della funzionalità WINBIO**](winbio-capability-constants.md)
</dt> </dl>

 

 





