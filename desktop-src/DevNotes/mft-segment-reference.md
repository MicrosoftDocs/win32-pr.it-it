---
description: Rappresenta un indirizzo nella tabella del file master (MFT). L'indirizzo viene contrassegnato con un numero di sequenza riutilizzato in modo circolare impostato al momento della validità del riferimento al segmento MFT.
ms.assetid: 59d83b95-83fb-4630-8ce4-f58441c748ab
title: MFT_SEGMENT_REFERENCE struttura
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFT_SEGMENT_REFERENCE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0ef3ad4e727465b5ceb24c1ecc785f62b747da8113b8853bffc3431604089066
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117827087"
---
# <a name="mft_segment_reference-structure"></a>Struttura MFT \_ SEGMENT \_ REFERENCE

\[Questa struttura è valida solo per la versione 3 dei volumi NTFS. potrebbe essere modificato nelle versioni future.\]

Rappresenta un indirizzo nella tabella del file master (MFT). L'indirizzo viene contrassegnato con un numero di sequenza riutilizzato in modo circolare impostato al momento della validità del riferimento al segmento MFT.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _MFT_SEGMENT_REFERENCE {
  ULONG  SegmentNumberLowPart;
  USHORT SegmentNumberHighPart;
  USHORT SequenceNumber;
} MFT_SEGMENT_REFERENCE, *PMFT_SEGMENT_REFERENCE;
```



## <a name="members"></a>Members

<dl> <dt>

**SegmentNumberLowPart**
</dt> <dd>

Parte inferiore del numero di segmento.

</dd> <dt>

**SegmentNumberHighPart**
</dt> <dd>

Parte alta del numero di segmento.

</dd> <dt>

**Sequencenumber**
</dt> <dd>

Numero di sequenza diverso da zero. Il valore 0 è riservato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Si noti che non esiste alcun file di intestazione associato per questa struttura.

Questa definizione di struttura è valida solo per la versione principale 3 e la versione secondaria 0 o 1, come segnalato da [**FSCTL \_ GET NTFS VOLUME \_ \_ \_ DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

Il **tipo di dati FILE \_ REFERENCE** viene definito come segue.

``` syntax
typedef MFT_SEGMENT_REFERENCE FILE_REFERENCE, *PFILE_REFERENCE;
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tabella file master](master-file-table.md)
</dt> </dl>

 

 
