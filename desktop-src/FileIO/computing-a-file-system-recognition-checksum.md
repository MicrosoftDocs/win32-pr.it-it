---
description: La struttura FILE SYSTEM RECOGNITION STRUCTURE, definita internamente da Windows e usata dal riconoscimento \_ \_ file system (FRS), contiene un valore di checksum che deve essere calcolato correttamente per il corretto funzionamento di FRS con un file system \_ specificato.
ms.assetid: 8f76784f-7d03-4874-ae7f-e8bdc42638c3
title: Calcolo di un checksum di riconoscimento del file system
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce146fda589668d39f1f7ff4158384986fb719f2bbbee6ce0584ad9f1e540b08
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119329181"
---
# <a name="computing-a-file-system-recognition-checksum"></a>Calcolo di un checksum di riconoscimento del file system

La struttura [**FILE \_ SYSTEM RECOGNITION \_ \_ STRUCTURE,**](file-system-recognition-structure.md) definita internamente da Windows e usata dal riconoscimento [file system](file-system-recognition.md) (FRS), contiene un valore di checksum che deve essere calcolato correttamente per il corretto funzionamento di FRS con un valore di file system specificato. L'esempio seguente consente di eseguire questo calcolo.


```C++
typedef struct _FILE_SYSTEM_RECOGNITION_STRUCTURE {
  UCHAR  Jmp[3];
  UCHAR  FsName[8];
  UCHAR  MustBeZero[5];
  ULONG  Identifier;
  USHORT Length;
  USHORT Checksum;
} FILE_SYSTEM_RECOGNITION_STRUCTURE, *PFILE_SYSTEM_RECOGNITION_STRUCTURE;

USHORT ComputeFileSystemInformationChecksum (
    __in PFILE_SYSTEM_RECOGNITION_STRUCTURE Fsrs
    )

/*++

Routine Description:

    This routine computes the file record checksum.

Arguments:

    Fsrs - Pointer to the record.

Return Value:

    The checksum result.

--*/

{
    USHORT Checksum = 0;
    USHORT i;
    PUCHAR Buffer = (PUCHAR)Fsrs;
    USHORT StartOffset;

    //
    //  Skip the jump instruction
    //

    StartOffset = FIELD_OFFSET(FILE_SYSTEM_RECOGNITION_STRUCTURE, FsName);
    
    for (i = StartOffset; i < Fsrs->Length; i++) {

        //
        //  Skip the checksum field itself, which is a USHORT.
        //

        if ((i == FIELD_OFFSET(FILE_SYSTEM_RECOGNITION_STRUCTURE, Checksum)) ||
            (i == FIELD_OFFSET(FILE_SYSTEM_RECOGNITION_STRUCTURE, Checksum)+1)) {

            continue;
        }

        Checksum = ((Checksum & 1) ? 0x8000 : 0) + (Checksum >> 1) + Buffer[i];
    }

    return Checksum;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riconoscimento del file system](file-system-recognition.md)
</dt> <dt>

[**STRUTTURA DI RICONOSCIMENTO DEL FILE \_ \_ \_ SYSTEM**](file-system-recognition-structure.md)
</dt> </dl>

 

 



