---
title: Struttura WINBIO_BDB_ANSI_381_RECORD ( \_ tipi WINBIO. h)
description: Contiene informazioni su una singola impronta digitale o un esempio di Palma da un utente finale.
ms.assetid: e0b32d05-3e96-4b42-9e18-57d10513f224
keywords:
- Struttura di WINBIO_BDB_ANSI_381_RECORD Windows Biometric Framework API
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
ms.openlocfilehash: f30af31d88349dbe02066f231cdff21293aebe90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400282"
---
# <a name="winbio_bdb_ansi_381_record-structure"></a>\_Struttura di record WINBIO BDB \_ ANSI \_ 381 \_

La struttura di **\_ record WINBIO BDB \_ ANSI \_ 381 \_** contiene informazioni su una singola impronta digitale o un esempio di Palma da un utente finale. Una raccolta di queste strutture è inclusa in ogni struttura di [**\_ intestazione WINBIO BDB \_ ANSI \_ 381 \_**](winbio-bdb-ansi-381-header.md) .

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

Contiene il numero di byte nella struttura più il numero di byte dei dati dell'immagine di esempio.

</dd> <dt>

**HorizontalLineLength**
</dt> <dd>

Specifica il numero di pixel in una riga orizzontale dell'esempio.

</dd> <dt>

**VerticalLineLength**
</dt> <dd>

Specifica il numero di pixel in una riga verticale dell'esempio.

</dd> <dt>

**Position**
</dt> <dd>

Valore **del \_ \_ SOTTOtipo biometrico WINBIO** che specifica il dito o la Palma utilizzata per generare l'esempio biometrico. Per altre informazioni, vedere la sezione Osservazioni.

</dd> <dt>

**CountOfViews**
</dt> <dd>

Deve essere impostato su uno (1);

</dd> <dt>

**ViewNumber**
</dt> <dd>

Deve essere impostato su uno (1);

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

Il membro *position* specifica l'area della mano o della palma usata per creare l'esempio biometrico. Il Windows Biometric Framework (WBF) supporta attualmente solo l'acquisizione di impronte digitali e usa le costanti seguenti per rappresentare le informazioni sulla posizione.

-   WINBIO \_ ANSI \_ 381 \_ POS \_ sconosciuta
-   WINBIO \_ ANSI \_ 381 \_ POS \_ \_ pollice RH
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ - \_ dito indice
-   WINBIO \_ ANSI \_ 381 \_ POS \_ \_ secondo \_ dito medio
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ \_ anulare
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ piccolo \_ dito
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ Thumb
-   WINBIO \_ ANSI \_ 381 \_ POS \_ - \_ dito indice LH \_
-   WINBIO \_ ANSI \_ 381 \_ POS \_ - \_ dito medio SX \_
-   WINBIO \_ ANSI \_ 381 \_ POS \_ - \_ \_ dito sinistro
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ Little \_ Finger
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ quattro \_ dita
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ quattro \_ dita
-   WINBIO \_ ANSI \_ 381 \_ POS \_ due \_ pollici

> [!IMPORTANT]
>
> Non tentare di convalidare il valore specificato per il valore di *posizione* . Il servizio biometria di Windows convaliderà il valore fornito prima di passarlo all'implementazione. Se il valore è **WINBIO, non vi sono \_ \_ \_ informazioni** o **\_ sottotipi \_ di WINBIO**, quindi eseguire la convalida laddove appropriato.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                                    |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>\_Tipi WinBio. h (includere WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture delle applicazioni client](client-application-structures.md)
</dt> </dl>

 

 





