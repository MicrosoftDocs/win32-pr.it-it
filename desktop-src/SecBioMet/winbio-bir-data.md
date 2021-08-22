---
title: WINBIO_BIR_DATA struttura (Winbio \_ types.h)
description: Specifica le dimensioni, in byte, e l'offset di un blocco di informazioni biometriche.
ms.assetid: 2f73eb1f-f1a1-4831-a8f7-eec28aa51645
keywords:
- WINBIO_BIR_DATA struttura Windows'API Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_BIR_DATA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01978cf55d90e217aa50fb8fad696f6af90b33ab9e59975a901daa99db633181
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911045"
---
# <a name="winbio_bir_data-structure"></a>Struttura DEI DATI BIR WINBIO \_ \_

La **struttura WINBIO \_ BIR \_ DATA** specifica le dimensioni, in byte, e l'offset di un blocco di informazioni biometriche. Questa struttura viene usata dalla struttura [**WINBIO \_ BIR**](winbio-bir.md) per specificare dove si trovano le varie parti di un record di informazioni biometriche.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _WINBIO_BIR_DATA {
  ULONG Size;
  ULONG Offset;
} WINBIO_BIR_DATA;
```



## <a name="members"></a>Members

<dl> <dt>

**Dimensioni**
</dt> <dd>

Dimensioni, in byte, delle informazioni biometriche.

</dd> <dt>

**Offset**
</dt> <dd>

Offset, in byte dall'inizio della [**struttura \_ BIR WINBIO,**](winbio-bir.md) delle informazioni biometriche.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'uso di offset anziché puntatori consente di eseguire facilmente la serializzazione del BIR e di eseguire una conversione meno complessa tra ambienti a 32 e 64 bit o tra modalità utente e kernel.

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

[**WINBIO \_ BIR**](winbio-bir.md)
</dt> <dt>

[**INTESTAZIONE BIR WINBIO \_ \_**](winbio-bir-header.md)
</dt> </dl>

 

 





