---
description: La classe del nome FileIO \_ V0 \_ è una versione precedente della classe del tipo di evento per gli eventi di I/O di file. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: dcbe37f2-6df0-41a5-b85f-dcd06cbd5901
title: Classe FileIo_V0_Name
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
ms.openlocfilehash: 6e88d1b9b5b36815b1a833062c30e804e4db744a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758426"
---
# <a name="fileio_v0_name-class"></a>FileIO \_ V0 \_ nome classe

La classe del **\_ \_ nome FileIO V0** è una versione precedente della classe del tipo di evento per gli eventi di I/O di file.

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

I tipi di membri della classe del **\_ \_ nome di FileIO V0** sono i seguenti:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe del **\_ \_ nome FileIO V0** ha queste proprietà.

<dl> <dt>

FileName
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (2), StringTermination ("NullTerminated"), Format ("w")
</dt> </dl>

Percorso completo del file, esclusa la lettera di unità.

</dd> <dt>

FileObject
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (1), puntatore
</dt> </dl>

Corrisponde al valore di questo puntatore al valore del puntatore **FileObject** in un evento [**DiskIo \_ TypeGroup1**](diskio-typegroup1.md) per determinare il tipo di operazione di i/O.

</dd> </dl>

## <a name="remarks"></a>Commenti

**Windows Server 2003:** Per recuperare la lettera di unità per il percorso del nome file, usare il valore della proprietà **FileObject** per eseguire il mapping all'evento [**DiskIo \_ TypeGroup1**](diskio-typegroup1.md) corrispondente. Dall'evento **DiskIo \_ TypeGroup1** usare i valori della proprietà **numerodisco** e **ByteOffset** per eseguire il mapping all'evento [**SystemConfig \_**](systemconfig-logdisk.md) LogDisk corrispondente. La proprietà **DriveLetterString** contiene la lettera di unità.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**FileIO \_ V0**](fileio-v0.md)
</dt> </dl>

 

 




