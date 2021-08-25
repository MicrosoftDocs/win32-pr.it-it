---
description: Questa classe è la classe del tipo di evento per l'evento di creazione file. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 83465072-3dae-4a39-8a36-1512025b79df
title: FileIo_Create classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_Create
- FileIo_Create.IrpPtr
- FileIo_Create.TTID
- FileIo_Create.FileObject
- FileIo_Create.CreateOptions
- FileIo_Create.FileAttributes
- FileIo_Create.ShareAccess
- FileIo_Create.OpenPath
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6e0c4085225fe523dcabca87a15bced8bd1f093f0b3da89fa0582b5675cdfbbc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829951"
---
# <a name="fileio_create-class"></a>Classe FileIo \_ Create

Questa classe è la classe del tipo di evento per l'evento di creazione file.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType{64}, EventTypeName{"Create"}]
class FileIo_Create : FileIo
{
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 CreateOptions;
  uint32 FileAttributes;
  uint32 ShareAccess;
  string OpenPath;
};
```

## <a name="members"></a>Members

La **classe FileIo \_ Create** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe FileIo \_ Create** ha queste proprietà.

<dl> <dt>

**Createoptions**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(4)
</dt> </dl>

Valori passati nei *parametri CreateOptions* *e CreateDispositions* alla [**funzione NtCreateFile.**](/windows/win32/api/winternl/nf-winternl-ntcreatefile)

</dd> <dt>

**FileAttributes**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(5)
</dt> </dl>

Valore passato nel *parametro FileAttributes* alla [**funzione NtCreateFile.**](/windows/win32/api/winternl/nf-winternl-ntcreatefile)

</dd> <dt>

**Oggetto FileObject**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(3), Puntatore
</dt> </dl>

Identificatore che può essere usato per correlare le operazioni alla stessa istanza dell'oggetto file aperto tra gli eventi di creazione e chiusura di file.

</dd> <dt>

**IrpPtr**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(1), Pointer
</dt> </dl>

Pacchetto di richiesta I/O. Questa proprietà identifica l'attività di I/O.

</dd> <dt>

**OpenPath**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(7), StringTermination("NullTerminated"), Format("w")
</dt> </dl>

Percorso del file.

</dd> <dt>

**ShareAccess**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(6)
</dt> </dl>

Valore passato nel *parametro ShareAccess* alla [**funzione NtCreateFile.**](/windows/win32/api/winternl/nf-winternl-ntcreatefile)

</dd> <dt>

**TTID**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(2), Puntatore
</dt> </dl>

Identificatore di thread del thread che crea il file.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Fileio**](fileio.md)
</dt> </dl>

 

 
