---
title: WINBIO_REGISTERED_FORMAT struttura (Winbio \_ types.h)
description: Specifica un formato dati registrato come coppia proprietario/formato.
ms.assetid: a178840e-81cc-4dd3-9d80-a181fa7fa888
keywords:
- WINBIO_REGISTERED_FORMAT struttura Windows'API Biometric Framework
- PWINBIO_REGISTERED_FORMAT puntatore alla struttura Windows'API Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_REGISTERED_FORMAT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fcf871f3fc5f258de22e033e8a388968ab58c1a35e19829bf3d02a97ca60c53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909369"
---
# <a name="winbio_registered_format-structure"></a>Struttura WINBIO \_ REGISTERED \_ FORMAT

La **struttura WINBIO \_ REGISTERED \_ FORMAT** specifica un formato dati registrato come coppia proprietario/formato.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _WINBIO_REGISTERED_FORMAT {
  USHORT Owner;
  USHORT Type;
} WINBIO_REGISTERED_FORMAT, *PWINBIO_REGISTERED_FORMAT;
```



## <a name="members"></a>Members

<dl> <dt>

**Proprietario**
</dt> <dd>

Valore proprietario assegnato da IBIA (International Biometric Industry Association).

</dd> <dt>

**Tipo**
</dt> <dd>

Formato assegnato dal proprietario.

</dd> </dl>

## <a name="remarks"></a>Commenti

Poiché Windows attualmente supporta solo lettori di impronte digitali, nella struttura **WINBIO \_ REGISTERED \_ FORMAT** devono essere usati i valori seguenti.



| Costante                                    | Significato                                                                                                               |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| PROPRIETARIO DEL \_ FORMATO WINBIO ANSI \_ 381 \_ \_<br/> | Comitato tecnico M1 (biometria) del comitato internazionale per gli standard di tecnologia dell'informazione (INCITS).<br/> |
| TIPO DI \_ FORMATO WINBIO ANSI \_ 381 \_ \_<br/>  | Formato di interscambio dati anSI INCITS 381 basato su immagine del dito.<br/>                                                |



 

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

[**Costanti FORMAT DI WINBIO \_ ANSI \_ 381 \_**](winbio-ansi-381-format-constants.md)
</dt> <dt>

[**INTESTAZIONE WINBIO \_ BDB \_ ANSI \_ 381 \_**](winbio-bdb-ansi-381-header.md)
</dt> <dt>

[**INTESTAZIONE DI WINBIO \_ \_ BIR**](winbio-bir-header.md)
</dt> </dl>

 

 





