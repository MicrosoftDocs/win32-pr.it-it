---
description: La \_ struttura doc info \_ 3 descrive un documento che verrà stampato.
ms.assetid: 6e7b6727-da04-4f67-af77-6b51c68a4eb3
title: Struttura DOC_INFO_3 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOC_INFO_3
- _DOC_INFO_3A
- _DOC_INFO_3W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 85d1d0f6af2eece8f9bd58112347478ec384642a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311547"
---
# <a name="doc_info_3-structure"></a>\_Struttura doc info \_ 3

La struttura **doc \_ info \_ 3** descrive un documento che verrà stampato.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _DOC_INFO_3 {
  LPTSTR pDocName;
  LPTSTR pOutputFile;
  LPTSTR pDatatype;
  DWORD  dwFlags;
} DOC_INFO_3, *PDOC_INFO_3;
```



## <a name="members"></a>Members

<dl> <dt>

**pDocName**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome del documento.

</dd> <dt>

**pOutputFile**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome di un file di output.

</dd> <dt>

**pDatatype**
</dt> <dd>

Puntatore a una stringa con terminazione null che identifica il tipo di dati utilizzati per registrare il documento.

</dd> <dt>

**dwFlags**
</dt> <dd>

Bandiere. Attualmente può essere **null** o quanto segue.



| Contrassegno                 | Significato                                                                                                                                          |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| \_scrittura di MEMORYMAP \_ | Fa in modo che [**StartDocPrinter**](startdocprinter.md) non usi [**AddJob**](addjob.md) e [**ScheduleJob**](schedulejob.md) per la stampa locale. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

L' \_ impostazione di scrittura di MEMORYMAP \_ in **doc \_ info \_ 3** è un'ottimizzazione. Questo consente a GDI di mappare i file di spooling nell'applicazione e velocizzare la registrazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ \_ Info doc \_ 3W** (Unicode) e **\_ informazioni del documento \_ \_ 3A** (ANSI)<br/>                                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddJob**](addjob.md)
</dt> <dt>

[**ScheduleJob**](schedulejob.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> </dl>

 

 




