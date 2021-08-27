---
title: WINBIO_BSP_SCHEMA struttura (Winbio \_ types.h)
description: Descrive le funzionalità di un provider di servizi biometrici.
ms.assetid: d690c735-55a1-4e2c-8b39-d52a1972bf93
keywords:
- WINBIO_BSP_SCHEMA struttura Windows'API Biometric Framework
- PWINBIO_BSP_SCHEMA puntatore alla struttura Windows'API Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_BSP_SCHEMA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff46f5484addb0221d9e441df73ecca3e8283da88ee7849e4362314aa1c375e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080781"
---
# <a name="winbio_bsp_schema-structure"></a>Struttura dello \_ SCHEMA BSP WINBIO \_

La **struttura DELLO \_ \_ SCHEMA BSP WINBIO** descrive le funzionalità di un provider di servizi biometrici. Questa struttura viene usata dalla [**funzione WinBioEnumServiceProviders.**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders)

## <a name="syntax"></a>Sintassi


```C++
typedef struct _WINBIO_BSP_SCHEMA {
  WINBIO_BIOMETRIC_TYPE BiometricFactor;
  WINBIO_UUID           BspId;
  WINBIO_STRING         Description;
  WINBIO_STRING         Vendor;
  WINBIO_VERSION        Version;
} WINBIO_BSP_SCHEMA, *PWINBIO_BSP_SCHEMA;
```



## <a name="members"></a>Members

<dl> <dt>

**BiometricFactor**
</dt> <dd>

Tipo di misurazione biometrica usata da questo dispositivo. Attualmente deve essere **WINBIO \_ TYPE \_ FINGERPRINT.**

</dd> <dt>

**BspId**
</dt> <dd>

Valore che identifica in modo univoco questo componente del provider di servizi biometrici.

</dd> <dt>

**Descrizione**
</dt> <dd>

Stringa **Unicode con** terminazione NULL che contiene una descrizione del provider di servizi biometrici.

</dd> <dt>

**Fornitore**
</dt> <dd>

Stringa Unicode con terminazione **NULL** contenente il nome del fornitore che fornisce il provider di servizi biometrici.

</dd> <dt>

**Version**
</dt> <dd>

Struttura [**VERSION DI WINBIO \_**](winbio-version.md) che contiene la versione software del componente del provider di servizi biometrici.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                                    |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Winbio \_ types.h (include Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture delle applicazioni client](client-application-structures.md)
</dt> <dt>

[**WinBioEnumServiceProviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders)
</dt> </dl>

 

 





