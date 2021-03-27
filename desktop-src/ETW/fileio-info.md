---
description: Questa classe è la classe del tipo di evento per l'evento di informazioni sul file. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 41ae1f8a-a90f-43d0-a848-a2c095f046d4
title: Classe FileIo_Info
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
ms.openlocfilehash: 985986132abe432e1adefb51939b8ace1aa48c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980370"
---
# <a name="fileio_info-class"></a>\_Classe info FileIO

Questa classe è la classe del tipo di evento per l'evento di informazioni sul file.

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

La **classe \_ info di FileIO** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ info del FileIO** contiene queste proprietà.

<dl> <dt>

**ExtraInfo**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (5), puntatore
</dt> </dl>

Per le richieste FileDispositionInformation, questo campo contiene la disposizione richiesta. Per le richieste FileEndOfFileInformation e FileAllocationInformation, questo campo contiene le dimensioni del file specificato.

</dd> <dt>

**FileKey**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (4), puntatore
</dt> </dl>

Per determinare il nome del file, trovare la corrispondenza con il valore di questa proprietà con la proprietà **FileObject** di un evento del [**\_ nome**](fileio-name.md) del FileIO.

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

**InfoClass**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (6)
</dt> </dl>

Classe di informazioni sui file richiesta.

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

**TTID**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (2), puntatore
</dt> </dl>

Identificatore del thread che sta eseguendo l'operazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Set information and query Information Events indica che gli attributi di file sono stati impostati o sottoposti a query. Quando viene emesso un comando FSCTL, viene registrato un evento di controllo file system (FSControl).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**FileIo**](fileio.md)
</dt> </dl>

 

 




