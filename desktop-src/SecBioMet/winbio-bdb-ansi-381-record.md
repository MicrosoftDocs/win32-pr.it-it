---
title: WINBIO_BDB_ANSI_381_RECORD struttura (Winbio \_ types.h)
description: Contiene informazioni su una singola impronta digitale o un campione di palmo di un utente finale.
ms.assetid: e0b32d05-3e96-4b42-9e18-57d10513f224
keywords:
- WINBIO_BDB_ANSI_381_RECORD struttura Windows'API Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_BDB_ANSI_381_RECORD
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15e30cd66348245aa3090fb21188d7d1cea347c1b28ee51243d2effd9b52609f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119480341"
---
# <a name="winbio_bdb_ansi_381_record-structure"></a>Struttura RECORD DI WINBIO \_ BDB \_ ANSI \_ 381 \_

La **struttura WINBIO \_ BDB \_ ANSI \_ 381 \_ RECORD** contiene informazioni su una singola impronta digitale o un campione di palmo di un utente finale. Una raccolta di queste strutture è inclusa in ogni [**struttura WINBIO \_ BDB \_ ANSI \_ 381 \_ HEADER.**](winbio-bdb-ansi-381-header.md)

## <a name="syntax"></a>Sintassi


```C++
typedef struct _WINBIO_BDB_ANSI_381_RECORD {
  ULONG                    BlockLength;
  USHORT                   HorizontalLineLength;
  USHORT                   VerticalLineLength;
  WINBIO_BIOMETRIC_SUBTYPE Position;
  UCHAR                    CountOfViews;
  UCHAR                    ViewNumber;
  UCHAR                    ImageQuality;
  UCHAR                    ImpressionType;
  UCHAR                    Reserved;
} WINBIO_BDB_ANSI_381_RECORD;
```



## <a name="members"></a>Members

<dl> <dt>

**BlockLength**
</dt> <dd>

Contiene il numero di byte in questa struttura più il numero di byte di dati immagine di esempio.

</dd> <dt>

**HorizontalLineLength**
</dt> <dd>

Specifica il numero di pixel in una riga orizzontale dell'esempio.

</dd> <dt>

**VerticalLineLength**
</dt> <dd>

Specifica il numero di pixel in una linea verticale dell'esempio.

</dd> <dt>

**Position**
</dt> <dd>

Valore **\_ \_ SUBTYPE BIOMETRICO WINBIO** che specifica il dito o il palmo usato per generare il campione biometrico. Per altre informazioni, vedere la sezione Osservazioni.

</dd> <dt>

**CountOfViews**
</dt> <dd>

Deve essere impostato su uno (1).

</dd> <dt>

**ViewNumber**
</dt> <dd>

Deve essere impostato su uno (1).

</dd> <dt>

**ImageQuality**
</dt> <dd>

Riservato. Deve essere 254 (0xFE).

</dd> <dt>

**ImpressionType**
</dt> <dd>

Riservato.

</dd> <dt>

**Reserved**
</dt> <dd>

Riservato. Deve essere impostato su zero (0).

</dd> </dl>

## <a name="remarks"></a>Commenti

Il *membro Position* specifica l'area della mano o del palmo usato per creare il campione biometrico. Il Windows Biometric Framework (WBF) attualmente supporta solo l'acquisizione di impronte digitali e usa le costanti seguenti per rappresentare le informazioni sulla posizione.

-   POS DI WINBIO \_ ANSI \_ 381 \_ \_ SCONOSCIUTO
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ THUMB
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ INDEX \_ FINGER
-   DITO MEDIO WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ \_
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ RING \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ LITTLE \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ THUMB
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ INDEX \_ FINGER
-   DITO MEDIO WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ \_
-   DITO AD ANELLO WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ \_
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ LITTLE \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS RH QUATTRO \_ \_ \_ DITA
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH QUATTRO \_ \_ DITA
-   WINBIO \_ ANSI \_ 381 \_ POS DUE \_ \_ POLLICI

> [!IMPORTANT]
>
> Non tentare di convalidare il valore fornito per il *valore Position.* Il Windows biometrica convaliderà il valore fornito prima di passarlo all'implementazione. Se il valore è **WINBIO \_ SUBTYPE \_ NO \_ INFORMATION** o **WINBIO \_ SUBTYPE \_ ANY,** convalidare dove appropriato.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                                    |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Winbio \_ types.h (include Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture delle applicazioni client](client-application-structures.md)
</dt> </dl>

 

 





