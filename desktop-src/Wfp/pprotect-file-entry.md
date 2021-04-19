---
description: Struttura utilizzata dalla funzione SfcGetFiles.
ms.assetid: 958167e3-3eb3-406a-85bf-ffe2851a95a1
title: Struttura PPROTECT_FILE_ENTRY (sfcfiles. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PPROTECT_FILE_ENTRY
api_type:
- HeaderDef
api_location:
- Sfcfiles.h
ms.openlocfilehash: 98cda570a3677560d51800d58822d93a942847c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312702"
---
# <a name="pprotect_file_entry-structure"></a>\_Struttura di \_ immissione file PPROTECT

\[Questa struttura è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Il supporto per questa struttura è stato rimosso in Windows Vista e Windows Server 2008. Usare invece le funzioni supportate elencate in [WRP Functions](wfp-functions.md) .\]

Struttura utilizzata dalla funzione [**SfcGetFiles**](sfcgetfiles.md) .

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PPROTECT_FILE_ENTRY {
  PWSTR SourceFileName;
  PWSTR FileName;
  PWSTR InfName;
} PPROTECT_FILE_ENTRY, *PPPROTECT_FILE_ENTRY;
```



## <a name="members"></a>Members

<dl> <dt>

**SourceFileName**
</dt> <dd>

Puntatore a un valore stringa contenente il nome del file di origine. Questo valore sarà **null** se il file non viene rinominato durante l'installazione.

</dd> <dt>

**FileName**
</dt> <dd>

Puntatore a un valore stringa contenente il nome file di destinazione più il percorso completo del file.

</dd> <dt>

**InfName**
</dt> <dd>

Puntatore a un valore stringa contenente il nome del file INF che fornisce informazioni sul layout. Questo parametro può essere **null** quando si usa il layout predefinito.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                 |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                        |
| Intestazione<br/>                   | <dl> <dt>Sfcfiles. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SfcGetFiles**](sfcgetfiles.md)
</dt> </dl>

 

 




