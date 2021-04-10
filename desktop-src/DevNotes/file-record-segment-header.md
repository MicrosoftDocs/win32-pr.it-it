---
description: Rappresenta il segmento di record del file. Si tratta dell'intestazione per ogni segmento di record di file nella tabella file master (MFT).
ms.assetid: 4548ad49-1924-4888-8966-c45f8e453c6f
title: Struttura FILE_RECORD_SEGMENT_HEADER
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILE_RECORD_SEGMENT_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: 293bb14dbaee0853aa1ef293502724458e02e26f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225535"
---
# <a name="file_record_segment_header-structure"></a>\_Struttura di \_ intestazione del segmento di record di file \_

\[Questa struttura è valida solo per la versione 3 dei volumi NTFS. potrebbe essere modificato nelle versioni future.\]

Rappresenta il segmento di record del file. Si tratta dell'intestazione per ogni segmento di record di file nella tabella file master (MFT).

## <a name="syntax"></a>Sintassi


```C++
typedef struct _FILE_RECORD_SEGMENT_HEADER {
  MULTI_SECTOR_HEADER   MultiSectorHeader;
  ULONGLONG             Reserved1;
  USHORT                SequenceNumber;
  USHORT                Reserved2;
  USHORT                FirstAttributeOffset;
  USHORT                Flags;
  ULONG                 Reserved3[2];
  FILE_REFERENCE        BaseFileRecordSegment;
  USHORT                Reserved4;
  UPDATE_SEQUENCE_ARRAY UpdateSequenceArray;
} FILE_RECORD_SEGMENT_HEADER, *PFILE_RECORD_SEGMENT_HEADER;
```



## <a name="members"></a>Members

<dl> <dt>

**MultiSectorHeader**
</dt> <dd>

Intestazione multisettore definita dal gestore della cache. La struttura dell' [**\_ \_ intestazione multisettore**](multi-sector-header.md) contiene sempre la firma "file" e una descrizione della posizione e della dimensione della matrice di sequenza di aggiornamento.

</dd> <dt>

**Reserved1**
</dt> <dd>

Riservato.

</dd> <dt>

**SequenceNumber**
</dt> <dd>

Numero di sequenza. Questo valore viene incrementato ogni volta che viene liberato un segmento di record di file; è 0 se il segmento non viene utilizzato. Il campo **SequenceNumber** di un riferimento a file deve corrispondere al contenuto di questo campo; Se non corrispondono, il riferimento al file è errato e probabilmente obsoleto.

</dd> <dt>

**Reserved2**
</dt> <dd>

Riservato.

</dd> <dt>

**FirstAttributeOffset**
</dt> <dd>

Offset del primo record di attributo, espresso in byte.

</dd> <dt>

**Flag**
</dt> <dd>

Flag del file.

<dl> <dt>

<span id="FILE_RECORD_SEGMENT_IN_USE"></span><span id="file_record_segment_in_use"></span>**File \_ \_Segmento \_ di record in \_ uso** (0x0001)
</dt> <dt>

<span id="FILE_FILE_NAME_INDEX_PRESENT"></span><span id="file_file_name_index_present"></span>**File \_ \_Indice nome \_ file \_ presente** (0x0002)
</dt> </dl> </dd> <dt>

**Reserved3**
</dt> <dd>

Riservato.

</dd> <dt>

**BaseFileRecordSegment**
</dt> <dd>

Un riferimento di file al segmento di record del file di base per il file. Se si tratta del record del file di base, il valore è 0. Vedere informazioni di [**\_ \_ riferimento sul segmento MFT**](mft-segment-reference.md).

</dd> <dt>

**Reserved4**
</dt> <dd>

Riservato.

</dd> <dt>

**UpdateSequenceArray**
</dt> <dd>

Matrice di sequenza di aggiornamento per proteggere i trasferimenti multisettore del segmento di record di file.

</dd> </dl>

## <a name="remarks"></a>Commenti

Si noti che non è presente alcun file di intestazione associato per questa struttura.

Questa definizione di struttura è valida solo per la versione principale 3 e secondaria 0 o 1, come indicato [**da \_ FSCTL \_ ottenere \_ \_ i dati del volume NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tabella file master](master-file-table.md)
</dt> </dl>

 

 
