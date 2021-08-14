---
title: WINBIO_VERSION struttura (Winbio \_ types.h)
description: Contiene il numero di versione software di un componente del provider di servizi biometrici.
ms.assetid: b9d08e10-00db-4f3f-9e27-6063aafa4151
keywords:
- WINBIO_VERSION struttura Windows'API Biometric Framework
- PWINBIO_VERSION puntatore alla struttura Windows'API Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_VERSION
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de81dd3da7f37e473a65caaf3e4cd52c8fd2f6732dced45f43245cb4e4c5c905
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909116"
---
# <a name="winbio_version-structure"></a>Struttura WINBIO \_ VERSION

La **struttura WINBIO \_ VERSION** contiene il numero di versione software di un componente del provider di servizi biometrici.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _WINBIO_VERSION {
  DWORD MajorVersion;
  DWORD MinorVersion;
} WINBIO_VERSION, *PWINBIO_VERSION;
```



## <a name="members"></a>Members

<dl> <dt>

**MajorVersion**
</dt> <dd>

Valore **DWORD** che contiene il numero di versione principale.

</dd> <dt>

**MinorVersion**
</dt> <dd>

Valore **DWORD** che contiene il numero di versione secondaria.

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

[**SCHEMA DI WINBIO \_ BSP \_**](winbio-bsp-schema.md)
</dt> <dt>

[**SCHEMA UNITÀ \_ WINBIO \_**](winbio-unit-schema.md)
</dt> </dl>

 

 





