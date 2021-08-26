---
description: Questa classe è la classe del tipo di evento per l'evento di informazioni sui file. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 41ae1f8a-a90f-43d0-a848-a2c095f046d4
title: FileIo_Info classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_Info
- FileIo_Info.IrpPtr
- FileIo_Info.TTID
- FileIo_Info.FileObject
- FileIo_Info.FileKey
- FileIo_Info.ExtraInfo
- FileIo_Info.InfoClass
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8a77d135fa5140f5d8d51a26164cd96009f06bacee654d13bec8dbaa9dcd76a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042001"
---
# <a name="fileio_info-class"></a>Classe FileIo \_ Info

Questa classe è la classe del tipo di evento per l'evento di informazioni sui file.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType{69, 70, 71, 74, 75}, EventTypeName{"SetInfo", "Delete", "Rename", "QueryInfo", "FSControl"}]
class FileIo_Info : FileIo
{
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 FileKey;
  uint32 ExtraInfo;
  uint32 InfoClass;
};
```

## <a name="members"></a>Members

La **classe FileIo \_ Info** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe FileIo \_ Info** ha queste proprietà.

<dl> <dt>

**ExtraInfo**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(5), Puntatore
</dt> </dl>

Per le richieste FileDispositionInformation, questo campo contiene la disposizione richiesta. Per le richieste FileEndOfFileInformation e FileAllocationInformation, questo campo contiene le dimensioni del file specificate.

</dd> <dt>

**FileKey**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(4), Puntatore
</dt> </dl>

Per determinare il nome del file, associare il valore di questa proprietà alla **proprietà FileObject** di un [**evento FileIo \_ Name.**](fileio-name.md)

</dd> <dt>

**Oggetto FileObject**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(3), Puntatore
</dt> </dl>

Identificatore che può essere utilizzato per correlare le operazioni alla stessa istanza dell'oggetto file aperto tra gli eventi di creazione e chiusura di file.

</dd> <dt>

**InfoClass**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(6)
</dt> </dl>

Classe di informazioni sul file richiesta.

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

**TTID**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(2), Puntatore
</dt> </dl>

Identificatore di thread del thread che esegue l'operazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le informazioni sui set e gli eventi relativi alle query indicano che gli attributi del file sono stati impostati o sottoposti a query. Quando viene eseguito un comando FSCTL, viene registrato un evento di controllo file system (FSControl).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Fileio**](fileio.md)
</dt> </dl>

 

 




