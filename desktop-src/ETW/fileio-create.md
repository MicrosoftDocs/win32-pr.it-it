---
description: Questa classe è la classe del tipo di evento per l'evento di creazione del file. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 83465072-3dae-4a39-8a36-1512025b79df
title: Classe FileIo_Create
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
ms.openlocfilehash: 2f8a42e9dee1c49817d578ab73a221c013f69aef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977663"
---
# <a name="fileio_create-class"></a>Classe di creazione FileIO \_

Questa classe è la classe del tipo di evento per l'evento di creazione del file.

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

I tipi di membri della classe di **\_ creazione di FileIO** sono:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

Questa proprietà è presente nella classe **FileIO \_ create** .

<dl> <dt>

**CreateOptions**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (4)
</dt> </dl>

Valori passati nei parametri *createOptions* e *CreateDispositions* alla funzione [**NTCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) .

</dd> <dt>

**FileAttributes**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (5)
</dt> </dl>

Valore passato nel parametro *FileAttributes* alla funzione [**NTCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) .

</dd> <dt>

**FileObject**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (3), puntatore
</dt> </dl>

Identificatore che può essere usato per correlare le operazioni alla stessa istanza dell'oggetto file aperto tra gli eventi di creazione e chiusura di file.

</dd> <dt>

**IrpPtr**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (1), puntatore
</dt> </dl>

Pacchetto di richiesta IO. Questa proprietà identifica l'attività IO.

</dd> <dt>

**OpenPath**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (7), StringTermination ("NullTerminated"), Format ("w")
</dt> </dl>

Percorso del file.

</dd> <dt>

**ShareAccess**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (6)
</dt> </dl>

Valore passato nel parametro *ShareAccess* alla funzione [**NTCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) .

</dd> <dt>

**TTID**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (2), puntatore
</dt> </dl>

Identificatore del thread che sta creando il file.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**FileIo**](fileio.md)
</dt> </dl>

 

 
