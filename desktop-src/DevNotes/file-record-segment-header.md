---
description: Rappresenta il segmento di record di file. Questa è l'intestazione per ogni segmento di record di file nella tabella del file master (MFT).
ms.assetid: 4548ad49-1924-4888-8966-c45f8e453c6f
title: FILE_RECORD_SEGMENT_HEADER struttura
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
ms.openlocfilehash: 0c9d7a3653ad965141e691546866f599d8615f5f12feb92fa25c861d7c429b74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119260601"
---
# <a name="file_record_segment_header-structure"></a>Struttura \_ FILE RECORD SEGMENT \_ \_ HEADER

\[Questa struttura è valida solo per la versione 3 dei volumi NTFS. potrebbe essere modificato nelle versioni future.\]

Rappresenta il segmento di record di file. Questa è l'intestazione per ogni segmento di record di file nella tabella del file master (MFT).

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

Intestazione multisettore definita dal gestore della cache. La [**struttura MULTI SECTOR \_ \_ HEADER**](multi-sector-header.md) contiene sempre la firma "FILE" e una descrizione della posizione e delle dimensioni della matrice della sequenza di aggiornamento.

</dd> <dt>

**Reserved1**
</dt> <dd>

Riservato.

</dd> <dt>

**Sequencenumber**
</dt> <dd>

Numero di sequenza. Questo valore viene incrementato ogni volta che viene liberato un segmento di record di file. è 0 se il segmento non viene usato. Il **campo SequenceNumber** di un riferimento al file deve corrispondere al contenuto di questo campo. Se non corrispondono, il riferimento al file non è corretto e probabilmente è obsoleto.

</dd> <dt>

**Riservato2**
</dt> <dd>

Riservato.

</dd> <dt>

**FirstAttributeOffset**
</dt> <dd>

Offset del primo record di attributo, in byte.

</dd> <dt>

**Flag**
</dt> <dd>

Flag di file.

<dl> <dt>

<span id="FILE_RECORD_SEGMENT_IN_USE"></span><span id="file_record_segment_in_use"></span>**FILE \_ SEGMENTO \_ RECORD \_ IN \_ USO** (0x0001)
</dt> <dt>

<span id="FILE_FILE_NAME_INDEX_PRESENT"></span><span id="file_file_name_index_present"></span>**FILE \_ INDICE \_ \_ DEI NOMI FILE \_ PRESENTE** (0x0002)
</dt> </dl> </dd> <dt>

**Riservato3**
</dt> <dd>

Riservato.

</dd> <dt>

**BaseFileRecordSegment**
</dt> <dd>

Riferimento di file al segmento di record del file di base per questo file. Se si tratta del record del file di base, il valore è 0. Vedere [**RIFERIMENTO AL SEGMENTO MFT \_ \_**](mft-segment-reference.md).

</dd> <dt>

**Riservato4**
</dt> <dd>

Riservato.

</dd> <dt>

**UpdateSequenceArray**
</dt> <dd>

Matrice della sequenza di aggiornamento per proteggere i trasferimenti a più fattori del segmento di record di file.

</dd> </dl>

## <a name="remarks"></a>Commenti

Si noti che non è presente alcun file di intestazione associato per questa struttura.

Questa definizione di struttura è valida solo per la versione principale 3 e la versione secondaria 0 o 1, come segnalato da [**FSCTL \_ GET NTFS VOLUME \_ \_ \_ DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tabella file master](master-file-table.md)
</dt> </dl>

 

 
