---
description: Struttura utilizzata dalla funzione SfcGetFiles.
ms.assetid: 958167e3-3eb3-406a-85bf-ffe2851a95a1
title: PPROTECT_FILE_ENTRY struttura (Sfcfiles.h)
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
ms.openlocfilehash: c9070290170febf08e532b071812600fb0ef8755302a4bd1603858659196d0c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053199"
---
# <a name="pprotect_file_entry-structure"></a>Struttura PPROTECT \_ FILE \_ ENTRY

\[Questa struttura è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Il supporto per questa struttura è stato rimosso in Windows Vista e Windows Server 2008. Usare invece le funzioni supportate elencate in [Funzioni WRP.](wfp-functions.md)\]

Struttura utilizzata dalla [**funzione SfcGetFiles.**](sfcgetfiles.md)

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

**Sourcefilename**
</dt> <dd>

Puntatore a un valore stringa contenente il nome file del file di origine. Sarà NULL **se** il file non viene rinominato durante l'installazione.

</dd> <dt>

**FileName**
</dt> <dd>

Puntatore al valore stringa contenente il nome file di destinazione e il percorso completo del file.

</dd> <dt>

**InfName**
</dt> <dd>

Puntatore al valore stringa contenente il nome file del file INF che fornisce informazioni sul layout. Questo parametro può essere **NULL quando** si usa il layout predefinito.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                 |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                        |
| Intestazione<br/>                   | <dl> <dt>Sfcfiles.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SfcGetFiles**](sfcgetfiles.md)
</dt> </dl>

 

 




