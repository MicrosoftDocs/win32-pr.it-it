---
title: Struttura WINBIO_EXTENDED_ENROLLMENT_PARAMETERS (WinBio \_ Adapter. h)
description: Contiene informazioni aggiuntive necessarie per la creazione di un modello di registrazione da un adattatore del motore.
ms.assetid: E8007316-0A9D-4F35-A266-273B2406D545
keywords:
- Struttura di WINBIO_EXTENDED_ENROLLMENT_PARAMETERS Windows Biometric Framework API
- API Windows Biometric Framework puntatore alla struttura PWINBIO_EXTENDED_ENROLLMENT_PARAMETERS
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
ms.openlocfilehash: b4f041d131bcee540a75a131b4179947fbe8e394
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475665"
---
# <a name="winbio_extended_enrollment_parameters-structure"></a>WINBIO \_ \_ struttura dei parametri di registrazione estesa \_

La struttura dei **\_ \_ \_ parametri di registrazione estesa WINBIO** contiene informazioni aggiuntive necessarie a un adattatore del motore per creare un modello di registrazione.

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

Dimensioni (in byte) della struttura dei **\_ \_ \_ parametri di registrazione estesa WINBIO** .

</dd> <dt>

**Sottofattore**
</dt> <dd>

Uno dei valori [**\_ \_ costanti del SOTTOtipo biometrico WINBIO**](winbio-biometric-subtype-constants.md) che fornisce informazioni aggiuntive sulla registrazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il Windows Biometric Framework passa questa struttura al metodo [**EngineAdapterSetEnrollmentParameters**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_parameters_fn) durante un'operazione di registrazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2016\]<br/>                                                                     |
| Intestazione<br/>                   | <dl> <dt>WinBio \_ Adapter. h (include WinBio \_ Adapter. h)</dt> </dl> |



 

 





