---
title: Struttura WINBIO_BIR_DATA ( \_ tipi WINBIO. h)
description: Specifica la dimensione, in byte, e l'offset di un blocco di informazioni biometriche.
ms.assetid: 2f73eb1f-f1a1-4831-a8f7-eec28aa51645
keywords:
- Struttura di WINBIO_BIR_DATA Windows Biometric Framework API
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
ms.openlocfilehash: 41ebf7b157c5bd806442cdc120350a89ce646f9e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400593"
---
# <a name="winbio_bir_data-structure"></a>\_ \_ Struttura dei dati WINBIO Bir

La **struttura \_ \_ dei dati WINBIO bir** specifica la dimensione, in byte, e l'offset di un blocco di informazioni biometriche. Questa struttura viene usata dalla struttura [**WINBIO \_ Bir**](winbio-bir.md) per specificare dove si trovano le varie parti di un record di informazioni biometriche.

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

Offset, in byte dall'inizio della struttura [**WINBIO \_ Bir**](winbio-bir.md) , delle informazioni biometriche.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'uso degli offset anziché dei puntatori consente una semplice serializzazione di BIR e per una conversione meno complessa tra gli ambienti 32 e 64 bit o tra l'utente e la modalità kernel.

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

[**WINBIO \_ Bir**](winbio-bir.md)
</dt> <dt>

[**\_intestazione WINBIO bir \_**](winbio-bir-header.md)
</dt> </dl>

 

 





