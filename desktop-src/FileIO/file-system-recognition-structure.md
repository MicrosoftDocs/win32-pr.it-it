---
description: Contiene le informazioni sul riconoscimento file system su disco archiviate nel settore di avvio dei volumi (zero del settore del disco logico).
ms.assetid: d9c19e01-ff82-4bbc-9eb6-aac9dc5c34ac
title: Struttura FILE_SYSTEM_RECOGNITION_STRUCTURE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILE_SYSTEM_RECOGNITION_STRUCTURE
api_type:
- NA
api_location: ''
ms.openlocfilehash: c542b2b9ee1cd1696c7c95797c7df20aa02180cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049777"
---
# <a name="file_system_recognition_structure-structure"></a>\_Struttura della \_ struttura di riconoscimento del file System \_

Contiene le informazioni sul riconoscimento file system su disco archiviate nel settore di avvio del volume (zero del settore del disco logico).

Si tratta di una struttura di dati definita internamente non disponibile in un'intestazione pubblica e viene fornita qui per file system sviluppatori che desiderano sfruttare file system il riconoscimento. Per ulteriori informazioni, vedere [riconoscimento del file System](file-system-recognition.md).

## <a name="syntax"></a>Sintassi


```C++
typedef struct _FILE_SYSTEM_RECOGNITION_STRUCTURE {
  UCHAR  Jmp[3];
  UCHAR  FsName[8];
  UCHAR  MustBeZero[5];
  ULONG  Identifier;
  USHORT Length;
  USHORT Checksum;
} FILE_SYSTEM_RECOGNITION_STRUCTURE;
```



## <a name="members"></a>Members

<dl> <dt>

**JMP**
</dt> <dd>

Istruzione JMP. Questo membro dati non è incluso nel valore contenuto nel membro dati di **checksum** .

</dd> <dt>

**FsName**
</dt> <dd>

Nome del file system. Si tratta di una sequenza di 8 caratteri ASCII che rappresenta il nome leggibile non localizzabile del file system in cui è formattato il volume.

Questa stringa si trova nella stessa posizione del nome del file system OEM su un disco con una normale struttura del blocco di parametri BIOS (BPB).

</dd> <dt>

**MustBeZero**
</dt> <dd>

Spazio riservato che contiene tutti gli zeri.

Questo membro dati si sovrappone a quanto normalmente sono i membri dati seguenti in un BPB:

-   **BytesPerSector**
-   **SectorsPerCluster**
-   **ReservedSectorCount**

Poiché questi membri dati sono impostati su zero, questo dovrebbe essere sufficiente per fare in modo che gli OSs precedenti concludano che non si tratta di un BPB valido e pertanto riconoscono il volume.

</dd> <dt>

**Identificatore**
</dt> <dd>

Identificatore della struttura. Deve contenere il valore 0x53525346 disposto in ordine dei byte little-endian.

A questo punto della struttura, i dati sono allineati a 16 byte.

</dd> <dt>

**Length**
</dt> <dd>

Numero di byte in questa struttura, dall'inizio alla fine, incluso il membro dati **JMP** .

</dd> <dt>

**Checksum**
</dt> <dd>

Checksum a due byte calcolato sui byte a partire dal membro dati **FsName** e terminando con l'ultimo byte di questa struttura, esclusi i membri dati **JMP** e **checksum** .

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>              |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Calcolo di un checksum di riconoscimento del file System](computing-a-file-system-recognition-checksum.md)
</dt> <dt>

[Riconoscimento del file System](file-system-recognition.md)
</dt> <dt>

[**\_ \_ informazioni sul riconoscimento del file System \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-file_system_recognition_information)
</dt> <dt>

[**\_riconoscimento del \_ file \_ System di query \_ FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition)
</dt> </dl>

 

