---
title: Struttura WINBIO_REGISTERED_FORMAT ( \_ tipi WINBIO. h)
description: Specifica un formato dati registrato come coppia proprietario/formato.
ms.assetid: a178840e-81cc-4dd3-9d80-a181fa7fa888
keywords:
- Struttura di WINBIO_REGISTERED_FORMAT Windows Biometric Framework API
- API Windows Biometric Framework puntatore alla struttura PWINBIO_REGISTERED_FORMAT
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
ms.openlocfilehash: 8f45293fe95627c7dfad4c9c51eb7fa74ad1738c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517806"
---
# <a name="winbio_registered_format-structure"></a>\_Struttura del \_ formato registrato WINBIO

La struttura del **\_ \_ formato registrato WINBIO** specifica un formato dati registrato come coppia proprietario/formato.

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

Valore proprietario assegnato a IBROLI (International Biometric Industry Association).

</dd> <dt>

**Tipo**
</dt> <dd>

Formato assegnato dal proprietario.

</dd> </dl>

## <a name="remarks"></a>Commenti

Poiché Windows supporta attualmente solo i lettori di impronte digitali, nella struttura del **\_ \_ formato registrato WINBIO** devono essere usati i valori seguenti.



| Costante                                    | Significato                                                                                                               |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| \_Proprietario del \_ formato ANSI 381 \_ \_ di WINBIO<br/> | InterNational Committee for Information Technology Standards (INCIs) Technical Committee M1 (biometria).<br/> |
| \_Tipo di \_ formato ANSI 381 \_ \_ di WINBIO<br/>  | ANSI INCIs 381 formato di interscambio dati basato su immagine Finger.<br/>                                                |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                                    |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>\_Tipi WinBio. h (includere WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture delle applicazioni client](client-application-structures.md)
</dt> <dt>

[**\_Costanti di \_ formato ANSI 381 di WINBIO \_**](winbio-ansi-381-format-constants.md)
</dt> <dt>

[**WINBIO \_ BDB \_ ANSI \_ 381 \_ intestazione**](winbio-bdb-ansi-381-header.md)
</dt> <dt>

[**\_intestazione WINBIO bir \_**](winbio-bir-header.md)
</dt> </dl>

 

 





