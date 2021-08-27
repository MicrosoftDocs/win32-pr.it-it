---
description: Questa classe è la classe del tipo di evento per eventi di operazioni su file semplici. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 5b6374e0-b39a-4d5a-acbd-25b410f1ba52
title: FileIo_SimpleOp classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_SimpleOp
- FileIo_SimpleOp.IrpPtr
- FileIo_SimpleOp.TTID
- FileIo_SimpleOp.FileObject
- FileIo_SimpleOp.FileKey
api_type:
- NA
api_location: ''
ms.openlocfilehash: 246bf356786b1b884380faa1feaad11db4d3f406a296d3292c571ff02698f454
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130571"
---
# <a name="fileio_simpleop-class"></a>Classe FileIo \_ SimpleOp

Questa classe è la classe del tipo di evento per eventi di operazioni su file semplici.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType{65, 66, 73}, EventTypeName{"Cleanup", "Close", "Flush"}]
class FileIo_SimpleOp : FileIo
{
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 FileKey;
};
```

## <a name="members"></a>Members

La **classe FileIo \_ SimpleOp** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe FileIo \_ SimpleOp** ha queste proprietà.

<dl> <dt>

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

L'evento Cleanup viene registrato quando viene chiuso l'ultimo handle per il file. L'evento Close specifica che viene liberato un oggetto file. L'evento Flush specifica quando i buffer dei file vengono scaricati completamente su disco.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Fileio**](fileio.md)
</dt> </dl>

 

 




