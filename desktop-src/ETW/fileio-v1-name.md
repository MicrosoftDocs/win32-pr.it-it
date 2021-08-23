---
description: 'FileIo_V1_Name classe: questa classe è la classe del tipo di evento per gli eventi di I/O di file. La sintassi seguente è semplificata dal codice MOF.'
ms.assetid: a4ee38df-af75-4aec-89ec-5a1c39302c82
title: FileIo_V1_Name classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_V1_Name
- FileIo_V1_Name.FileObject
- FileIo_V1_Name.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: c9a2488bb8f225df94e530e1964f0721c064c256423fe3218feb54adece7d0a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582401"
---
# <a name="fileio_v1_name-class"></a>Classe FileIo \_ V1 \_ Name

Questa classe è la classe del tipo di evento per gli eventi di I/O di file.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType{0, 32}, EventTypeName{"Name", "FileCreate"}]
class FileIo_V1_Name : FileIo
{
  uint32 FileObject;
  string FileName;
};
```

## <a name="members"></a>Members

La **classe FileIo \_ V1 \_ Name** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe FileIo \_ V1 \_ Name** ha queste proprietà.

<dl> <dt>

FileName
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(2), StringTermination("NullTerminated"), Format("w")
</dt> </dl>

Percorso completo del file, senza includere la lettera di unità.

</dd> <dt>

Oggetto FileObject
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(1), Pointer
</dt> </dl>

Trovare la corrispondenza tra il valore di questo puntatore e il valore del puntatore **FileObject** in un evento [**DiskIo \_ TypeGroup1**](diskio-typegroup1.md) per determinare il tipo di operazione di I/O.

</dd> </dl>

## <a name="remarks"></a>Commenti

**Windows Server 2003:** Per recuperare la lettera di unità per il percorso del nome file, usare il valore della proprietà **FileObject** per eseguire il mapping all'evento [ \_ DiskIo TypeGroup1](diskio-typegroup1.md) corrispondente. Dall'evento DiskIo TypeGroup1 usare i valori delle proprietà DiskNumber e ByteOffset per eseguire il mapping all'evento \_ [SystemConfig \_ LogDisk](systemconfig-logdisk.md) corrispondente (**ByteOffset** esegue il mapping **a StartOffset**).   La **proprietà DriveLetterString** contiene la lettera di unità.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Fileio**](fileio.md)
</dt> </dl>

 

 




