---
description: Rappresenta una voce nell'elenco di attributi.
ms.assetid: daa0c97d-2ebe-4e14-b1f8-e4be3075b13e
title: ATTRIBUTE_LIST_ENTRY struttura
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ATTRIBUTE_LIST_ENTRY
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0c0154de52dbefa6d29278ca05e924db6f6c1d84b124fe21b3092e728a0d07fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956140"
---
# <a name="attribute_list_entry-structure"></a>Struttura ATTRIBUTE \_ LIST \_ ENTRY

\[Questa struttura è valida solo per la versione 3 dei volumi NTFS. potrebbe essere modificato nelle versioni future.\]

Rappresenta una voce nell'elenco di attributi.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _ATTRIBUTE_LIST_ENTRY {
  ATTRIBUTE_TYPE_CODE   AttributeTypeCode;
  USHORT                RecordLength;
  UCHAR                 AttributeNameLength;
  UCHAR                 AttributeNameOffset;
  VCN                   LowestVcn;
  MFT_SEGMENT_REFERENCE SegmentReference;
  USHORT                Reserved;
  WCHAR                 AttributeName[1];
} ATTRIBUTE_LIST_ENTRY, *PATTRIBUTE_LIST_ENTRY;
```



## <a name="members"></a>Members

<dl> <dt>

**AttributeTypeCode**
</dt> <dd>

Codice del tipo di attributo.



| Valore                                                                                                                                                                                                                                           | Significato                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_STANDARD_INFORMATION"></span><span id="_standard_information"></span><dl> <dt>**$STANDARD \_ Informazioni**</dt> <dt>0x10</dt> </dl> | Attributi di file (ad esempio di sola lettura e archivio), timestamp (ad esempio creazione e ultima modifica del file) e numero di collegamenti rigidi.<br/> |
| <span id="_ATTRIBUTE_LIST"></span><span id="_attribute_list"></span><dl> <dt>**$ATTRIBUTE \_ Elenco**</dt> <dt>0x20</dt> </dl>                   | Elenco di attributi che costituiscono il file e il riferimento al file del record del file MFT in cui si trova ogni attributo.<br/>     |
| <span id="_FILE_NAME"></span><span id="_file_name"></span><dl> <dt>**$FILE \_ Nome**</dt> <dt>0x30</dt> </dl>                                  | Nome del file, in caratteri Unicode.<br/>                                                                                     |
| <span id="_OBJECT_ID"></span><span id="_object_id"></span><dl> <dt>**$OBJECT \_ Id**</dt> <dt>0x40</dt> </dl>                                  | Identificatore di oggetto a 16 byte assegnato dal servizio di rilevamento dei collegamenti.<br/>                                                              |
| <span id="_VOLUME_NAME"></span><span id="_volume_name"></span><dl> <dt>**$VOLUME \_ Nome**</dt> <dt>0x60</dt> </dl>                            | Etichetta del volume. Presente nel file $Volume.<br/>                                                                                   |
| <span id="_VOLUME_INFORMATION"></span><span id="_volume_information"></span><dl> <dt>**$VOLUME \_ Informazioni**</dt> <dt>0x70</dt> </dl>       | Informazioni sul volume. Presente nel file $Volume.<br/>                                                                             |
| <span id="_DATA"></span><span id="_data"></span><dl> <dt>**$DATA**</dt> <dt>0x80</dt> </dl>                                                  | Contenuto del file.<br/>                                                                                                        |
| <span id="_INDEX_ROOT"></span><span id="_index_root"></span><dl> <dt>**$INDEX \_ Radice**</dt> <dt>0x90</dt> </dl>                               | Usato per implementare l'allocazione dei nomi file per directory di grandi dimensioni.<br/>                                                                     |
| <span id="_INDEX_ALLOCATION"></span><span id="_index_allocation"></span><dl> <dt>**$INDEX \_ ALLOCAZIONE**</dt> <dt>0xA0</dt> </dl>             | Usato per implementare l'allocazione dei nomi file per directory di grandi dimensioni.<br/>                                                                     |
| <span id="_BITMAP"></span><span id="_bitmap"></span><dl> <dt>**$BITMAP**</dt> <dt>0xB0</dt> </dl>                                            | Indice bitmap per una directory di grandi dimensioni.<br/>                                                                                            |
| <span id="_REPARSE_POINT"></span><span id="_reparse_point"></span><dl> <dt>**$REPARSE \_ Punto**</dt> <dt>0xC0</dt> </dl>                      | Dati del reparse point.<br/>                                                                                                          |



 

</dd> <dt>

**Recordlength**
</dt> <dd>

Dimensione della struttura , più il buffer dei nomi facoltativo, in byte.

</dd> <dt>

**AttributeNameLength**
</dt> <dd>

Dimensione del nome dell'attributo facoltativo, in caratteri. Se esiste un nome, questo valore è diverso da zero e la struttura è seguita immediatamente da una stringa Unicode del numero di caratteri specificato.

</dd> <dt>

**AttributeNameOffset**
</dt> <dd>

Riservato.

</dd> <dt>

**LowestVcn**
</dt> <dd>

Numero di cluster virtuale (VCN) più basso per questo attributo. Questo membro è zero, a meno che l'attributo non richieda più segmenti di record di file e a meno che questa voce non sia un riferimento a un segmento diverso dal primo. In questo caso, questo valore è il vcn più basso descritto dal segmento a cui si fa riferimento.

</dd> <dt>

**SegmentReference**
</dt> <dd>

Segmento della tabella del file master (MFT) in cui risiede l'attributo. Vedere [**INFORMAZIONI DI RIFERIMENTO SUL \_ SEGMENTO \_ MFT.**](mft-segment-reference.md)

</dd> <dt>

**Reserved**
</dt> <dd>

Riservato.

</dd> <dt>

**AttributeName**
</dt> <dd>

Inizio del nome dell'attributo facoltativo.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'elenco di attributi è un elenco ordinato di strutture **ATTRIBUTE \_ LIST \_ ENTRY** allineate a quadword. Questo elenco viene ordinato prima in base al codice del tipo di attributo e quindi in base al nome dell'attributo (se presente). Due attributi non possono avere lo stesso codice di tipo, lo stesso nome e la stessa vcn più bassa. Pertanto, può essere presente al massimo un attributo per ogni codice di tipo senza un nome.

Questa definizione di struttura è valida solo per la versione principale 3 e la versione secondaria 0 o 1, come segnalato da [**FSCTL \_ GET NTFS VOLUME \_ \_ \_ DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

Si noti che non esiste alcun file di intestazione associato per questa struttura.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tabella file master](master-file-table.md)
</dt> </dl>

 

 
