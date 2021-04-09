---
description: La \_ struttura della \_ struttura di riconoscimento del file System \_ , definita internamente da Windows e utilizzata da file System Recognition (FRS), contiene un valore di checksum che deve essere calcolato correttamente affinché il servizio FRS funzioni correttamente con una file System non riconosciuta specificata.
ms.assetid: 8f76784f-7d03-4874-ae7f-e8bdc42638c3
title: Calcolo di un checksum di riconoscimento del file System
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74cac3975d4e1845dd1ff4aa218526e942fda152
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968686"
---
# <a name="computing-a-file-system-recognition-checksum"></a><span data-ttu-id="d9969-103">Calcolo di un checksum di riconoscimento del file System</span><span class="sxs-lookup"><span data-stu-id="d9969-103">Computing a File System Recognition Checksum</span></span>

<span data-ttu-id="d9969-104">La struttura della [**\_ struttura di \_ riconoscimento \_ del file System**](file-system-recognition-structure.md) , definita internamente da Windows e utilizzata da [file System Recognition](file-system-recognition.md) (FRS), contiene un valore di checksum che deve essere calcolato correttamente affinché il servizio FRS funzioni correttamente con una file System non riconosciuta specificata.</span><span class="sxs-lookup"><span data-stu-id="d9969-104">The [**FILE\_SYSTEM\_RECOGNITION\_STRUCTURE**](file-system-recognition-structure.md) structure, defined internally by Windows and used by [file system recognition](file-system-recognition.md) (FRS), contains a checksum value that must be properly computed for FRS to work properly with a specified unrecognized file system.</span></span> <span data-ttu-id="d9969-105">Nell'esempio seguente viene eseguita questa operazione di calcolo.</span><span class="sxs-lookup"><span data-stu-id="d9969-105">The following example accomplishes this computation.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="d9969-106">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d9969-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9969-107">Riconoscimento del file System</span><span class="sxs-lookup"><span data-stu-id="d9969-107">File System Recognition</span></span>](file-system-recognition.md)
</dt> <dt>

[<span data-ttu-id="d9969-108">**struttura di riconoscimento del FILE \_ System \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d9969-108">**FILE\_SYSTEM\_RECOGNITION\_STRUCTURE**</span></span>](file-system-recognition-structure.md)
</dt> </dl>

 

 



