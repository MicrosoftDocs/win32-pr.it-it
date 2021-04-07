---
description: Rappresenta un attributo del nome di file. Un file ha un attributo di nome file per ogni directory in cui viene immesso.
ms.assetid: 54458eee-b786-446c-80bd-213c13bdeb4a
title: Struttura FILE_NAME
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
ms.openlocfilehash: 609725c21f0c0811a4222cd9dfd662b3e25673f3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049085"
---
# <a name="file_name-structure"></a>\_Struttura del nome file

\[Questa struttura è valida solo per la versione 3 dei volumi NTFS. potrebbe essere modificato nelle versioni future.\]

Rappresenta un attributo del nome di file. Un file ha un attributo di nome file per ogni directory in cui viene immesso.

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

Riferimento file alla directory che indicizza il nome. Vedere informazioni di [**\_ \_ riferimento sul segmento MFT**](mft-segment-reference.md).

</dd> <dt>

**Reserved**
</dt> <dd>

Riservato.

</dd> <dt>

**FileNameLength**
</dt> <dd>

Lunghezza del nome file, in caratteri Unicode.

</dd> <dt>

**Flag**
</dt> <dd>

Flag del nome file.

<dl> <dt>

<span id="FILE_NAME_NTFS"></span><span id="file_name_ntfs"></span>**File \_ NOME \_ NTFS** (0x01)
</dt> <dt>

<span id="FILE_NAME_DOS"></span><span id="file_name_dos"></span>**File \_ NOME \_ DOS** (0x02)
</dt> </dl> </dd> <dt>

**FileName**
</dt> <dd>

Primo carattere del nome file.

</dd> </dl>

## <a name="remarks"></a>Commenti

Si noti che non è presente alcun file di intestazione associato per questa struttura.

Questa definizione di struttura è valida solo per la versione principale 3 e secondaria 0 o 1, come indicato [**da \_ FSCTL \_ ottenere \_ \_ i dati del volume NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tabella file master](master-file-table.md)
</dt> </dl>

 

 
