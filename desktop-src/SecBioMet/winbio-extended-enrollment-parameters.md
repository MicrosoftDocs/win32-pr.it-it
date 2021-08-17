---
title: WINBIO_EXTENDED_ENROLLMENT_PARAMETERS struttura (Adapter \_ Winbio.h)
description: Contiene informazioni aggiuntive necessarie a un adattatore motore per creare un modello di registrazione.
ms.assetid: E8007316-0A9D-4F35-A266-273B2406D545
keywords:
- WINBIO_EXTENDED_ENROLLMENT_PARAMETERS struttura Windows'API Biometric Framework
- PWINBIO_EXTENDED_ENROLLMENT_PARAMETERS puntatore alla struttura Windows'API Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_ENROLLMENT_PARAMETERS
api_location:
- Winbio_adapter.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55173b5badfb8764cfc9c681f4ed92e2f0d1c50e5db09075185af9e5db2e6433
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910490"
---
# <a name="winbio_extended_enrollment_parameters-structure"></a>Struttura DEI PARAMETRI \_ DI \_ REGISTRAZIONE ESTESA \_ WINBIO

La **struttura WINBIO \_ EXTENDED ENROLLMENT \_ \_ PARAMETERS** contiene informazioni aggiuntive necessarie a un adattatore motore per creare un modello di registrazione.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _WINBIO_EXTENDED_ENROLLMENT_PARAMETERS {
  SIZE_T                   Size;
  WINBIO_BIOMETRIC_SUBTYPE SubFactor;
} WINBIO_EXTENDED_ENROLLMENT_PARAMETERS, *PWINBIO_EXTENDED_ENROLLMENT_PARAMETERS;
```



## <a name="members"></a>Members

<dl> <dt>

**Dimensioni**
</dt> <dd>

Dimensione (in byte) della **struttura WINBIO \_ EXTENDED ENROLLMENT \_ \_ PARAMETERS.**

</dd> <dt>

**Sottofactoring**
</dt> <dd>

Uno dei valori [**di WINBIO \_ BIOMETRIC \_ SUBTYPE Constants**](winbio-biometric-subtype-constants.md) che fornisce informazioni aggiuntive sulla registrazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il Windows Biometric Framework passa questa struttura al metodo [**EngineAdapterSetEnrollmentParameters**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_parameters_fn) durante un'operazione di registrazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                                              |
| Server minimo supportato<br/> | \[Windows Server 2016 solo app desktop\]<br/>                                                                     |
| Intestazione<br/>                   | <dl> <dt>Winbio \_ adapter.h (include Winbio \_ adapter.h)</dt> </dl> |



 

 





