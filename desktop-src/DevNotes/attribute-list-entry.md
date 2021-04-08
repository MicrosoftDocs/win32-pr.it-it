---
description: Rappresenta una voce nell'elenco di attributi.
ms.assetid: daa0c97d-2ebe-4e14-b1f8-e4be3075b13e
title: Struttura ATTRIBUTE_LIST_ENTRY
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
ms.openlocfilehash: 67ee65a22c9e880c76d3b250c4859077f471b018
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877245"
---
# <a name="attribute_list_entry-structure"></a>\_ \_ Struttura voce elenco attributi

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
| <span id="_STANDARD_INFORMATION"></span><span id="_standard_information"></span><dl> <dt>**$Standard \_**</dt> <dt>0x10</dt> informazioni </dl> | Attributi di file (ad esempio di sola lettura e di archivio), timestamp (ad esempio, creazione di file e Ultima modifica) e conteggio dei collegamenti reali.<br/> |
| <span id="_ATTRIBUTE_LIST"></span><span id="_attribute_list"></span><dl> <dt>**$Attribute \_ ELENCAre**</dt> <dt>0x20</dt> </dl>                   | Elenco di attributi che compongono il file e il riferimento al file del record del file MFT in cui si trova ogni attributo.<br/>     |
| <span id="_FILE_NAME"></span><span id="_file_name"></span><dl> <dt>**$File \_ NOME**</dt> <dt>0x30</dt> </dl>                                  | Nome del file, in caratteri Unicode.<br/>                                                                                     |
| <span id="_OBJECT_ID"></span><span id="_object_id"></span><dl> <dt>**$Object \_ ID**</dt> <dt>0x40</dt> </dl>                                  | Identificatore di oggetto a 16 byte assegnato dal servizio di rilevamento dei collegamenti.<br/>                                                              |
| <span id="_VOLUME_NAME"></span><span id="_volume_name"></span><dl> <dt>**$Volume \_ NOME**</dt> <dt>0x60</dt> </dl>                            | Etichetta del volume. Presente nel file di $Volume.<br/>                                                                                   |
| <span id="_VOLUME_INFORMATION"></span><span id="_volume_information"></span><dl> <dt>**$Volume \_**</dt> <dt>0x70</dt> informazioni </dl>       | Informazioni sul volume. Presente nel file di $Volume.<br/>                                                                             |
| <span id="_DATA"></span><span id="_data"></span><dl> <dt>**$Data**</dt> <dt>0x80</dt> </dl>                                                  | Contenuto del file.<br/>                                                                                                        |
| <span id="_INDEX_ROOT"></span><span id="_index_root"></span><dl> <dt>**$Index \_**</dt> <dt>0x90</dt> radice </dl>                               | Utilizzato per implementare l'allocazione di file per directory di grandi dimensioni.<br/>                                                                     |
| <span id="_INDEX_ALLOCATION"></span><span id="_index_allocation"></span><dl> <dt>**$Index \_**</dt> <dt>Messaggi 0XA0</dt> di allocazione </dl>             | Utilizzato per implementare l'allocazione di file per directory di grandi dimensioni.<br/>                                                                     |
| <span id="_BITMAP"></span><span id="_bitmap"></span><dl> <dt>**$Bitmap**</dt> <dt>0XB0</dt> </dl>                                            | Indice bitmap per una directory di grandi dimensioni.<br/>                                                                                            |
| <span id="_REPARSE_POINT"></span><span id="_reparse_point"></span><dl> <dt>**$REPARSE \_ PUNTO**</dt> <dt>0xC0</dt> </dl>                      | Dati di reparse point.<br/>                                                                                                          |



 

</dd> <dt>

**RecordLength**
</dt> <dd>

Dimensioni della struttura, più il buffer dei nomi facoltativo, in byte.

</dd> <dt>

**AttributeNameLength**
</dt> <dd>

Dimensioni del nome di attributo facoltativo, in caratteri. Se esiste un nome, questo valore è diverso da zero e la struttura viene seguita immediatamente da una stringa Unicode del numero di caratteri specificato.

</dd> <dt>

**AttributeNameOffset**
</dt> <dd>

Riservato.

</dd> <dt>

**LowestVcn**
</dt> <dd>

Il numero di cluster virtuale più basso (VCN) per questo attributo. Questo membro è zero a meno che l'attributo non richieda più segmenti di record di file e, a meno che questa voce non sia un riferimento a un segmento diverso da quello prima. In questo caso, questo valore è il VCN più basso descritto dal segmento a cui si fa riferimento.

</dd> <dt>

**SegmentReference**
</dt> <dd>

Segmento della tabella file master (MFT) in cui risiede l'attributo. Vedere informazioni di [**\_ \_ riferimento sul segmento MFT**](mft-segment-reference.md).

</dd> <dt>

**Reserved**
</dt> <dd>

Riservato.

</dd> <dt>

**AttributeName**
</dt> <dd>

Inizio del nome di attributo facoltativo.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'elenco degli attributi è un elenco ordinato di strutture di **\_ \_ voci dell'elenco di attributi** allineati a quadrupla. Questo elenco viene ordinato prima in base al codice del tipo di attributo e quindi in base al nome dell'attributo (se presente). Due attributi non possono avere lo stesso codice di tipo, nome e VCN più basso. Pertanto, può essere presente al massimo un attributo per ogni codice del tipo senza un nome.

Questa definizione di struttura è valida solo per la versione principale 3 e secondaria 0 o 1, come indicato [**da \_ FSCTL \_ ottenere \_ \_ i dati del volume NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

Si noti che non è presente alcun file di intestazione associato per questa struttura.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tabella file master](master-file-table.md)
</dt> </dl>

 

 
