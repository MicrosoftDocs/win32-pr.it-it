---
description: Rappresenta un attributo del nome file. Un file ha un attributo di nome file per ogni directory in cui viene immesso.
ms.assetid: 54458eee-b786-446c-80bd-213c13bdeb4a
title: FILE_NAME struttura
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILE_NAME
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9b09b9c58228c9028a5ac9d26d834bdc21a5c02201338767af84dc713bc3aa60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076145"
---
# <a name="file_name-structure"></a>Struttura FILE \_ NAME

\[Questa struttura è valida solo per la versione 3 dei volumi NTFS. potrebbe essere modificato nelle versioni future.\]

Rappresenta un attributo del nome file. Un file ha un attributo di nome file per ogni directory in cui viene immesso.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _FILE_NAME {
  FILE_REFERENCE ParentDirectory;
  UCHAR          Reserved[0x38];
  UCHAR          FileNameLength;
  UCHAR          Flags;
  WCHAR          FileName[1];
} FILE_NAME, *PFILE_NAME;
```



## <a name="members"></a>Members

<dl> <dt>

**ParentDirectory**
</dt> <dd>

Riferimento di file alla directory in cui viene indicizzato questo nome. Vedere [**INFORMAZIONI DI RIFERIMENTO SUL \_ SEGMENTO \_ MFT.**](mft-segment-reference.md)

</dd> <dt>

**Reserved**
</dt> <dd>

Riservato.

</dd> <dt>

**FileNameLength**
</dt> <dd>

Lunghezza del nome del file, in caratteri Unicode.

</dd> <dt>

**Flag**
</dt> <dd>

Flag del nome file.

<dl> <dt>

<span id="FILE_NAME_NTFS"></span><span id="file_name_ntfs"></span>**FILE \_ NOME \_ NTFS** (0x01)
</dt> <dt>

<span id="FILE_NAME_DOS"></span><span id="file_name_dos"></span>**FILE \_ NAME \_ DOS** (0x02)
</dt> </dl> </dd> <dt>

**FileName**
</dt> <dd>

Primo carattere del nome file.

</dd> </dl>

## <a name="remarks"></a>Commenti

Si noti che non esiste alcun file di intestazione associato per questa struttura.

Questa definizione di struttura è valida solo per la versione principale 3 e la versione secondaria 0 o 1, come segnalato da [**FSCTL \_ GET NTFS VOLUME \_ \_ \_ DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tabella file master](master-file-table.md)
</dt> </dl>

 

 
