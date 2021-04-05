---
description: Rappresenta un indirizzo nella tabella file master (MFT). L'indirizzo è contrassegnato con un numero di sequenza riutilizzato circolare che viene impostato al momento della validità del riferimento del segmento MFT.
ms.assetid: 59d83b95-83fb-4630-8ce4-f58441c748ab
title: Struttura MFT_SEGMENT_REFERENCE
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
ms.openlocfilehash: beabe7620dadd01b25b3556715b33e2f10c2c230
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125643"
---
# <a name="mft_segment_reference-structure"></a>Struttura di riferimento del \_ segmento MFT \_

\[Questa struttura è valida solo per la versione 3 dei volumi NTFS. potrebbe essere modificato nelle versioni future.\]

Rappresenta un indirizzo nella tabella file master (MFT). L'indirizzo è contrassegnato con un numero di sequenza riutilizzato circolare che viene impostato al momento della validità del riferimento del segmento MFT.

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

Parte superiore del numero di segmento.

</dd> <dt>

**SequenceNumber**
</dt> <dd>

Numero di sequenza diverso da zero. Il valore 0 è riservato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Si noti che non è presente alcun file di intestazione associato per questa struttura.

Questa definizione di struttura è valida solo per la versione principale 3 e secondaria 0 o 1, come indicato [**da \_ FSCTL \_ ottenere \_ \_ i dati del volume NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

Il tipo di dati di **\_ riferimento del file** è definito nel modo seguente.

``` syntax
typedef MFT_SEGMENT_REFERENCE FILE_REFERENCE, *PFILE_REFERENCE;
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tabella file master](master-file-table.md)
</dt> </dl>

 

 
