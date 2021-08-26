---
description: La classe FileIo V0 Name è una versione precedente della classe del tipo di evento per gli eventi \_ \_ di I/O di file. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: dcbe37f2-6df0-41a5-b85f-dcd06cbd5901
title: FileIo_V0_Name classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_V0_Name
- FileIo_V0_Name.FileObject
- FileIo_V0_Name.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 11a85c182511a866d3fb76f291b0a73ed0541fdee34b7e6f74c036b5446792db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041861"
---
# <a name="fileio_v0_name-class"></a>Classe FileIo \_ V0 \_ Name

La **classe FileIo \_ V0 \_ Name** è una versione precedente della classe del tipo di evento per gli eventi di I/O di file.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType(0), EventTypeName("Name")]
class FileIo_V0_Name : FileIo_V0
{
  uint32 FileObject;
  string FileName;
};
```

## <a name="members"></a>Members

La **classe FileIo \_ V0 \_ Name** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe FileIo \_ V0 \_ Name** ha queste proprietà.

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

**Windows Server 2003:** Per recuperare la lettera di unità per il percorso del nome file, usare il valore della proprietà **FileObject** per eseguire il mapping all'evento [**\_ DiskIo TypeGroup1**](diskio-typegroup1.md) corrispondente. **Dall'evento DiskIo \_ TypeGroup1** usare i valori delle proprietà **DiskNumber** e **ByteOffset** per eseguire il mapping all'evento [**SystemConfig \_ LogDisk**](systemconfig-logdisk.md) corrispondente. La **proprietà DriveLetterString** contiene la lettera di unità.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**FileIo \_ V0**](fileio-v0.md)
</dt> </dl>

 

 




