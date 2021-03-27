---
description: Questa classe è la classe del tipo di evento per gli eventi di I/O di file. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: a4ee38df-af75-4aec-89ec-5a1c39302c82
title: Classe FileIo_V1_Name
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
ms.openlocfilehash: 617e0abeed095099996079211107d0720017514a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057825"
---
# <a name="fileio_v1_name-class"></a>\_ \_ Classe nome FileIO V1

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

I tipi di membri della classe del **\_ \_ nome FileIO V1** sono i seguenti:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe del **\_ \_ nome FileIO V1** presenta queste proprietà.

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

**Windows Server 2003:** Per recuperare la lettera di unità per il percorso del nome file, usare il valore della proprietà **FileObject** per eseguire il mapping all'evento [DiskIo \_ TypeGroup1](diskio-typegroup1.md) corrispondente. Dall' \_ evento TypeGroup1 di DiskIo, usare i valori della proprietà **numerodisco** e **ByteOffset** per eseguire il mapping all'evento [SystemConfig LogDisk \_](systemconfig-logdisk.md) corrispondente (**ByteOffset** viene mappato a **startOffset**). La proprietà **DriveLetterString** contiene la lettera di unità.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**FileIo**](fileio.md)
</dt> </dl>

 

 




